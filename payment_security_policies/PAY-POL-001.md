# Cardholder Data Protection Policy (PAY-POL-001)

## 1. Objective

This policy establishes comprehensive requirements for protecting cardholder data (CHD) and sensitive authentication data (SAD) throughout the payment lifecycle, ensuring compliance with PCI DSS v4.0 Requirements 3 and 4. It defines the controls for storing, processing, transmitting, and disposing of payment card data to protect **[Company Name]**'s customers and maintain trust in payment systems.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, systems, and processes that store, process, or transmit cardholder data, including:

- All cardholder data (CHD): Primary Account Number (PAN), cardholder name, expiration date, service code
- All sensitive authentication data (SAD): Full track data, CVV2/CVC2/CAV2, PIN/PIN block
- All systems within the cardholder data environment (CDE)
- All connected systems that could impact the security of the CDE
- All third-party service providers (TPSPs) with access to CHD

## 3. Policy

**[Company Name]** shall protect all cardholder data in accordance with PCI DSS requirements, minimizing data storage, rendering stored PAN unreadable, and encrypting CHD during transmission.

### 3.1 Cardholder Data Minimization

Account data storage shall be minimized through implementation of data retention and disposal controls per PCI DSS 3.2.

**Storage Limitations:**
- Only store account data elements necessary for legitimate business purposes
- Limit storage amount and retention time to that required for legal, regulatory, and/or business requirements
- Document specific business justification for storage of each data element
- Identify all locations where account data is stored, processed, or transmitted

**Retention Requirements:**
- Define specific retention periods for each type of stored account data
- Verify quarterly that stored account data exceeding the defined retention period has been securely deleted or rendered unrecoverable
- Implement automated processes to delete data upon expiration of retention period where feasible

### 3.2 Sensitive Authentication Data Prohibition

Sensitive authentication data (SAD) shall not be stored after authorization per PCI DSS 3.3.

**Prohibited Storage:**
- Full track data from magnetic stripe or chip shall never be stored after authorization
- Card verification codes (CVV2/CVC2/CAV2/CID) shall never be stored after authorization
- PINs and PIN blocks shall never be stored after authorization

**Pre-Authorization Handling:**
- Any SAD stored electronically prior to authorization completion shall be encrypted using strong cryptography
- SAD shall be rendered unrecoverable immediately upon completion of the authorization process
- Logs, debugging output, and error reports shall not contain SAD

**Issuer Exception:**
- Issuers and companies supporting issuing services may store SAD only when:
  - There is a documented legitimate issuing business need
  - The data is secured with strong cryptography
  - CISO has approved the storage in writing

### 3.3 PAN Protection in Storage

Primary account numbers shall be rendered unreadable anywhere they are stored per PCI DSS 3.5.

**Acceptable Protection Methods:**
- One-way hashes based on strong cryptography of the entire PAN
- Truncation (hashing cannot be used to replace the truncated segment)
- Index tokens (tokenization systems meeting PCI SSC guidelines)
- Strong cryptography with associated key-management processes

**Additional Storage Requirements:**
- If hashed and truncated versions of the same PAN are present, additional controls prevent correlation to reconstruct the original PAN
- Key management follows OP-POL-001 (Encryption and Key Management Policy)
- Cryptographic operations comply with PCI DSS Requirements 3.6 and 3.7

### 3.4 PAN Display and Copy Controls

Access to displays of full PAN and the ability to copy PAN shall be restricted per PCI DSS 3.4.

**Display Masking Requirements:**
- PAN is masked when displayed to show maximum of BIN and last four digits
- Only personnel with documented legitimate business need can see more than BIN and last four digits
- Roles requiring access to full PAN are documented with business justification

**Copy and Relocation Controls:**
- Technical controls prevent copy and/or relocation of PAN when using remote-access technologies
- Only personnel with documented authorization and legitimate business need may copy PAN
- Authorized personnel and business justification are documented and reviewed annually

### 3.5 Protection of PAN in Transit

PAN shall be protected with strong cryptography during transmission per PCI DSS 4.2.

**Transmission Over Open, Public Networks:**
- Strong cryptography and security protocols safeguard PAN during transmission
- Only trusted keys and certificates are accepted
- Certificates are confirmed as valid and not expired or revoked
- Protocols support only secure versions or configurations without fallback to insecure versions
- Encryption strength is appropriate for the encryption methodology in use

**Approved Protocols:**
- TLS 1.2 or higher with strong cipher suites
- IPsec VPN with AES-256 encryption
- Other industry-approved protocols as approved by the CISO

**End-User Messaging:**
- PAN shall be secured with strong cryptography whenever sent via end-user messaging technologies (email, instant messaging, SMS, chat)
- Use of end-user messaging for PAN transmission requires documented business justification and CISO approval

### 3.6 Key Management for CHD Protection

Cryptographic keys used to protect stored cardholder data shall be secured per PCI DSS 3.6 and 3.7.

**Key Protection Requirements:**
- Access to keys is restricted to the fewest number of custodians necessary
- Key-encrypting keys are at least as strong as the data-encrypting keys they protect
- Key-encrypting keys are stored separately from data-encrypting keys
- Keys are stored securely in the fewest possible locations and forms

**Key Lifecycle Management:**
- Keys are generated using strong cryptographic methods
- Keys are distributed securely
- Keys are stored securely (HSM preferred for production keys)
- Key changes occur at the end of defined cryptoperiods
- Retired or compromised keys are destroyed or securely archived
- Key custodians formally acknowledge their responsibilities

Detailed key management requirements are defined in OP-POL-001 (Encryption and Key Management Policy) and OP-PROC-001 (Cryptographic Key Management Procedure).

### 3.7 Tokenization Standards

When tokenization is used to protect CHD, the following standards apply per PCI DSS 3.5.1.

**Tokenization Requirements:**
- Tokenization systems comply with PCI SSC Tokenization Product Security Guidelines
- Token generation uses methods that cannot be reversed to derive the original PAN
- Token mapping data is stored only within the CDE
- Token vault security meets all applicable PCI DSS requirements
- De-tokenization is restricted to authorized systems and personnel

**Hybrid Approaches:**
- When multiple protection methods are used (tokenization, truncation, hashing), controls prevent correlation to reconstruct the original PAN

### 3.8 Third-Party Service Provider Requirements

Third-party service providers with access to cardholder data shall meet specific security requirements per PCI DSS 12.8.

**TPSP Requirements:**
- Maintain a list of all TPSPs with access to CHD
- Written agreements acknowledge the TPSP's responsibility for CHD security
- Established process for engaging TPSPs, including security due diligence
- Monitor TPSP PCI DSS compliance status annually
- Document shared PCI DSS responsibilities

**Shared Responsibility:**
- Clearly document which PCI DSS requirements are managed by **[Company Name]** vs. TPSP
- Responsibility matrix is reviewed annually and updated as needed
- TPSP compliance is validated annually via AOC or on-site assessment

### 3.9 Account Data Inventory

An inventory of all account data locations shall be maintained per PCI DSS 12.5.

**Inventory Requirements:**
- All locations where account data is stored, processed, or transmitted
- All system components in the CDE
- Data flow diagrams documenting movement of CHD
- Inventory is reviewed and validated at least annually

**Data Discovery:**
- Quarterly scans identify unauthorized storage of PAN
- If unauthorized PAN storage is detected, incident response procedures apply per RES-POL-001
- Findings are documented and remediated with root cause analysis

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 3.2.1 |
| 3.1 | SOC 2 TSC | CC6.5 |
| 3.2 | PCI DSS v4.0 | 3.3.1, 3.3.2, 3.3.3 |
| 3.3 | PCI DSS v4.0 | 3.5.1 |
| 3.3 | SOC 2 TSC | CC6.1 |
| 3.4 | PCI DSS v4.0 | 3.4.1, 3.4.2 |
| 3.5 | PCI DSS v4.0 | 4.2.1, 4.2.2 |
| 3.5 | SOC 2 TSC | CC6.7 |
| 3.6 | PCI DSS v4.0 | 3.6.1, 3.7.1-3.7.8 |
| 3.7 | PCI DSS v4.0 | 3.5.1 |
| 3.8 | PCI DSS v4.0 | 12.8.1-12.8.5 |
| 3.9 | PCI DSS v4.0 | 12.5.1, 12.5.2 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data (CHD)** | At minimum, the full Primary Account Number (PAN). May also include cardholder name, expiration date, and service code. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Cryptoperiod** | The time span during which a cryptographic key can be used for its defined purpose. |
| **Primary Account Number (PAN)** | Unique payment card number (typically 15-16 digits) that identifies the issuer and cardholder account. |
| **Sensitive Authentication Data (SAD)** | Security-related information including full track data, card verification codes (CVV2/CVC2/CAV2), and PINs/PIN blocks. |
| **Strong Cryptography** | Cryptography based on industry-tested and accepted algorithms with minimum key length of AES-128, TDES, RSA-2048, or ECC-224. |
| **Tokenization** | The process of replacing sensitive data with non-sensitive placeholders (tokens) that have no exploitable value. |
| **Third-Party Service Provider (TPSP)** | A business entity that is not a payment brand and provides services to merchants or other entities that involve storing, processing, or transmitting CHD. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Approve data protection controls. Authorize exceptions. Oversee compliance with this policy. |
| **PCI Program Manager** | Maintain account data inventory. Ensure cardholder data handling meets PCI DSS requirements. Coordinate TPSP compliance monitoring. |
| **IT Security Team** | Implement technical controls for CHD protection. Conduct data discovery scans. Monitor for unauthorized data storage. Manage encryption systems. |
| **Development Team** | Ensure applications handle CHD per this policy. Never store SAD after authorization. Implement tokenization and encryption. |
| **Operations Team** | Maintain secure data transmission. Execute secure disposal procedures. Manage backup encryption. |
| **All Workforce Members with CHD Access** | Handle CHD only as authorized. Never store SAD after authorization. Report suspected violations immediately. |

