# Encryption and Key Management Policy (OP-POL-001)

## 1. Objective

This policy establishes requirements for the secure configuration and use of encryption and key management at **[Company Name]** in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that cardholder data, sensitive authentication data, and customer financial information are protected through appropriate cryptographic controls throughout their lifecycle.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, contractors, and third parties who configure, access, or manage encryption services and encrypted information. It encompasses:

- All systems within the cardholder data environment (CDE) that store, process, or transmit cardholder data
- All systems processing nonpublic personal information (NPI) under GLBA
- All cloud-based and on-premises information systems, applications, databases, and storage services containing sensitive data
- All communication channels used to transmit cardholder data or customer financial information
- All cryptographic keys used to protect account data and customer information

## 3. Policy

**[Company Name]** shall implement encryption and key management controls to protect the confidentiality, integrity, and authenticity of cardholder data and customer financial information in accordance with PCI DSS, SOC 2, and GLBA requirements.

### 3.1 Cardholder Data Storage Minimization

Account data storage shall be kept to a minimum in accordance with PCI DSS Requirement 3.2.

- Cardholder data storage is limited to that which is required for business, legal, or regulatory purposes.

- Data retention and disposal policies define:
  - Coverage for all locations of stored account data
  - Specific retention requirements with documented business justification
  - Processes for secure deletion or rendering data unrecoverable when no longer needed
  - Quarterly verification that stored account data exceeding retention periods has been securely deleted

- Storage locations are inventoried and include backup systems, archive storage, removable media, and paper-based records.

### 3.2 Sensitive Authentication Data (SAD) Protection

Sensitive authentication data shall not be retained after authorization per PCI DSS Requirement 3.3.

- SAD is not stored after authorization, even if encrypted.

- SAD includes:
  - Full track data from the magnetic stripe or chip
  - Card verification codes (CVV2/CVC2/CAV2)
  - PINs and PIN blocks

- Any SAD stored electronically prior to completion of authorization is encrypted using strong cryptography per PCI DSS 3.3.2.

- SAD is rendered unrecoverable upon completion of the authorization process.

### 3.3 Primary Account Number (PAN) Protection at Rest

PAN shall be rendered unreadable anywhere it is stored per PCI DSS Requirement 3.5.

- PAN is protected using one of the following methods:
  - One-way hashes based on strong cryptography of the entire PAN
  - Truncation (hashing cannot replace truncated segments)
  - Index tokens (tokenization)
  - Strong cryptography with associated key management processes

- If hashed and truncated versions of the same PAN exist, controls prevent correlation to reconstruct the original PAN.

- Where tokenization is used, tokens cannot be reversed to obtain the original PAN without access to the tokenization system per PAY-POL-004 (Tokenization and Data Masking Policy).

### 3.4 PAN Display and Copy Restrictions

Access to displays of full PAN and ability to copy PAN is restricted per PCI DSS Requirement 3.4.

- PAN is masked when displayed (BIN and last four digits maximum) such that only personnel with legitimate business need can see more than the masked digits.

- A list of roles with access to full PAN is documented with business justification for each role.

- When using remote-access technologies, technical controls prevent copy and/or relocation of PAN except for personnel with documented authorization and legitimate business need per PCI DSS 3.4.2.

### 3.5 Encryption Requirements for Data at Rest

Strong cryptography shall be implemented for all sensitive data at rest.

**Cardholder Data:**
- All stored PAN is encrypted using AES-256 or equivalent strong cryptography per PCI DSS 3.5.1
- Encryption keys are managed in accordance with Section 3.8 of this policy

**Customer Financial Information (GLBA):**
- Customer information at rest is encrypted using strong cryptography per GLBA § 314.4(c)(3)
- Encryption is applied to databases, file storage, and backup systems containing NPI

**Cloud Environment:**
- Data at rest is encrypted using cloud provider encryption services (e.g., AWS S3 Server-Side Encryption, Azure Storage Service Encryption, GCP Cloud Storage encryption)
- Database encryption is implemented using cloud provider services (e.g., AWS RDS encryption, Azure SQL TDE, GCP Cloud SQL encryption)
- Customer-managed encryption keys (CMEK) are used for all production data containing cardholder data or confidential customer information
- Backup encryption is enabled for all cloud backup and archive services

### 3.6 Encryption Requirements for Data in Transit

Strong cryptography shall be implemented for all sensitive data in transit per PCI DSS Requirement 4.

**Cardholder Data Transmission:**
- Strong cryptography and security protocols protect PAN during transmission over open, public networks per PCI DSS 4.2.1:
  - Only trusted keys and certificates are accepted
  - Certificates are confirmed as valid and not expired or revoked
  - Protocols support only secure versions and do not fallback to insecure versions
  - Encryption strength is appropriate for the methodology in use

- PAN is secured with strong cryptography whenever sent via end-user messaging technologies (email, SMS, chat) per PCI DSS 4.2.2

**Customer Financial Information:**
- Customer information in transit over external networks is encrypted per GLBA § 314.4(c)(3)
- Internal network transmission of NPI uses encryption where technically feasible

**Protocol Requirements:**
- TLS 1.2 or higher is required for all encrypted transmissions
- SSL and early TLS versions (TLS 1.0, 1.1) are not permitted
- Only strong cipher suites are enabled; weak ciphers are disabled
- Certificate pinning is implemented for mobile applications processing cardholder data

### 3.7 Encryption Algorithm Standards

Approved encryption algorithms shall be used for all cryptographic operations.

**Approved Algorithms:**
| **Use Case** | **Algorithm** | **Minimum Key Length** |
|---|---|---|
| Symmetric encryption (data at rest) | AES | 256 bits |
| Symmetric encryption (data in transit) | AES-GCM | 256 bits |
| Asymmetric encryption | RSA | 2048 bits |
| Asymmetric encryption (preferred) | ECDSA | 256 bits (P-256 curve) |
| Hashing (integrity) | SHA-256 or higher | N/A |
| Hashing (passwords) | bcrypt, scrypt, or Argon2 | N/A |
| Key derivation | PBKDF2, HKDF | N/A |

**Prohibited Algorithms:**
- DES, 3DES (except for legacy card-present transactions)
- MD5, SHA-1 (for cryptographic purposes)
- RC4
- Any algorithm with known vulnerabilities

### 3.8 Cryptographic Key Management

Cryptographic keys used to protect stored account data shall be secured per PCI DSS Requirements 3.6 and 3.7.

**Key Protection Requirements (per PCI DSS 3.6.1):**
- Access to keys is restricted to the fewest number of custodians necessary
- Key-encrypting keys are at least as strong as the data-encrypting keys they protect
- Key-encrypting keys are stored separately from data-encrypting keys
- Keys are stored securely in the fewest possible locations and forms

**Key Lifecycle Management (per PCI DSS 3.7):**

| **Lifecycle Phase** | **Requirement** | **PCI DSS Reference** |
|---|---|---|
| Generation | Strong cryptographic key generation using approved methods | 3.7.1 |
| Distribution | Secure distribution to authorized custodians only | 3.7.2 |
| Storage | Secure storage using HSM, vault, or encrypted container | 3.7.3 |
| Rotation | Key changes at end of defined cryptoperiod (annual or per vendor guidance) | 3.7.4 |
| Retirement | Retirement, replacement, or destruction when cryptoperiod ends, integrity weakened, or compromise suspected | 3.7.5 |
| Manual Operations | Split knowledge and dual control for manual cleartext key operations | 3.7.6 |
| Substitution Prevention | Controls to prevent unauthorized key substitution | 3.7.7 |
| Custodian Acknowledgment | Formal acknowledgment by key custodians of responsibilities | 3.7.8 |

**Cryptoperiod Requirements:**
- Data encryption keys: Annual rotation or per application vendor guidance
- Key-encrypting keys: Rotation every **[Number, e.g., 2]** years
- TLS/SSL certificates: Annual renewal or upon algorithm deprecation
- Emergency rotation upon suspected or confirmed compromise

### 3.9 Cloud Key Management Services

Cloud-native key management services shall be used to manage cryptographic keys for cloud-hosted systems.

**Required Cloud Key Management Services:**
- **AWS:** AWS Key Management Service (AWS KMS) for Customer Managed Keys (CMK)
- **Azure:** Azure Key Vault for customer-managed encryption keys
- **Google Cloud:** Google Cloud Key Management Service (Cloud KMS) for Customer-Managed Encryption Keys (CMEK)
- **Multi-cloud:** HashiCorp Vault or equivalent for cross-cloud key management when required

**Cloud Key Management Requirements:**
- Customer-managed keys are used for all production data containing cardholder data or customer financial information
- Key rotation is configured within cloud provider console with automated annual rotation
- Access control is managed through cloud provider IAM with least privilege principles
- Audit logging is enabled for all key management activities using cloud provider audit services
- Key storage and processing occurs in approved geographic regions

### 3.10 Hardware Security Modules (HSMs)

HSMs shall be used for high-value cryptographic operations where required.

- HSMs are used for:
  - PIN encryption and decryption operations
  - Card verification value (CVV) generation and validation
  - Key injection and key management for payment terminals
  - High-volume transaction processing encryption

- HSMs are validated to FIPS 140-2 Level 3 or higher, or PCI PTS HSM requirements.

- HSM access is restricted to authorized personnel with documented approval.

### 3.11 Access Control and Monitoring

Access to encryption systems and key management services shall be strictly controlled and monitored.

**Access Requirements:**
- All access managed through IAM with role-based access controls
- Multi-factor authentication required for all access to key management services
- Separation of duties between key administration and data administration roles
- Access reviews conducted quarterly for key management system access

**Monitoring and Logging:**
- Comprehensive logging enabled for all key management activities
- Automated alerts configured for unauthorized key access attempts
- Log retention for at least one year with three months immediately available per PCI DSS 10.7
- Monthly review of key access logs

### 3.12 Service Provider Key Sharing

Where **[Company Name]** shares cryptographic keys with customers or receives keys from third parties, additional controls apply per PCI DSS 3.7.9.

- Guidance on secure transmission, storage, and updating of shared keys is documented and provided to customers/partners.

- Key sharing agreements document responsibilities for key protection.

- Shared keys comply with all requirements of this policy.

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 3.2.1 |
| 3.1 | GLBA Safeguards | § 314.4(c)(6) |
| 3.2 | PCI DSS v4.0 | 3.3.1, 3.3.2, 3.3.3 |
| 3.3 | PCI DSS v4.0 | 3.5.1 |
| 3.3 | SOC 2 TSC | CC6.1 |
| 3.4 | PCI DSS v4.0 | 3.4.1, 3.4.2 |
| 3.5 | PCI DSS v4.0 | 3.5.1 |
| 3.5 | SOC 2 TSC | CC6.1, C1.1 |
| 3.5 | GLBA Safeguards | § 314.4(c)(3) |
| 3.6 | PCI DSS v4.0 | 4.1.1, 4.2.1, 4.2.2 |
| 3.6 | SOC 2 TSC | CC6.1, CC6.7 |
| 3.6 | GLBA Safeguards | § 314.4(c)(3) |
| 3.7 | PCI DSS v4.0 | 3.5.1 |
| 3.7 | SOC 2 TSC | CC6.1 |
| 3.8 | PCI DSS v4.0 | 3.6.1, 3.7.1-3.7.8 |
| 3.8 | SOC 2 TSC | CC6.1 |
| 3.9 | PCI DSS v4.0 | 3.6.1, 3.7.3 |
| 3.9 | SOC 2 TSC | CC6.1, CC6.6 |
| 3.10 | PCI DSS v4.0 | 3.6.1 |
| 3.11 | PCI DSS v4.0 | 10.2, 10.4.1 |
| 3.11 | SOC 2 TSC | CC6.1, CC7.2 |
| 3.12 | PCI DSS v4.0 | 3.7.9 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data (CHD)** | At minimum, the full Primary Account Number (PAN). May also include cardholder name, expiration date, and service code. |
| **Cryptoperiod** | The time span during which a cryptographic key can be used for its defined purpose. |
| **Customer-Managed Encryption Keys (CMEK)** | Encryption keys that are created and managed by the customer within cloud provider key management services. |
| **Data-Encrypting Key (DEK)** | A cryptographic key used to encrypt data directly. |
| **Dual Control** | A process that requires two or more people to perform a key management function, where no single person can access the authentication factors of another. |
| **Hardware Security Module (HSM)** | A physical computing device that safeguards and manages cryptographic keys and provides cryptographic processing. |
| **Key-Encrypting Key (KEK)** | A cryptographic key used to encrypt other cryptographic keys for secure storage or transmission. |
| **Key Custodian** | An individual assigned responsibility for managing cryptographic keys or key components. |
| **Primary Account Number (PAN)** | Unique payment card number (typically 15-16 digits) that identifies the issuer and cardholder account. |
| **Sensitive Authentication Data (SAD)** | Security-related information including full track data, card verification codes (CVV2/CVC2/CAV2), and PINs/PIN blocks. |
| **Split Knowledge** | A method where two or more people separately have key components, with each knowing only their own component. |
| **Strong Cryptography** | Cryptography based on industry-tested algorithms with key lengths providing effective security for the data's sensitivity and intended use. |
| **Tokenization** | The process of replacing sensitive data with non-sensitive placeholders (tokens) that have no exploitable value. |
| **Truncation** | The practice of permanently removing a segment of the PAN so that only part of the number is stored. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own, review, and update this policy annually. Oversee encryption and key management program. Ensure compliance with PCI DSS, SOC 2, and GLBA requirements. |
| **IT Security Team** | Implement and maintain encryption controls. Configure and monitor key management systems. Respond to encryption-related security events. Conduct quarterly verification of data retention compliance. |
| **Cloud Operations Team** | Configure cloud encryption services and cloud-native key management. Implement security benchmarks. Monitor cloud encryption controls and key access. |
| **Key Custodians** | Manage cryptographic keys in accordance with assigned responsibilities. Maintain split knowledge and dual control for manual key operations. Acknowledge key custodian responsibilities formally. |
| **PCI Program Manager** | Ensure encryption controls meet PCI DSS requirements. Coordinate with QSA on encryption-related assessment activities. Maintain documentation for PCI compliance. |
| **Application Development Team** | Implement application-level encryption using approved algorithms. Integrate with key management services. Ensure no hard-coded keys or credentials in source code. |
| **All Workforce Members** | Handle encrypted data and systems in accordance with policy requirements. Report suspected encryption or key management issues. Never attempt to bypass encryption controls. |

