# Cryptographic Key Management Procedure (OP-PROC-001)

### 1. Purpose

To provide the technical steps for the secure generation, distribution, storage, rotation, and destruction of cryptographic keys used to protect cardholder data, customer financial information, and other sensitive data per PCI DSS Requirements 3.6 and 3.7.

### 2. Scope

This procedure applies to all cryptographic keys used to protect company and customer data, including:

- Keys used for cardholder data encryption (CHD/PAN)
- Keys used for customer financial information encryption (NPI)
- Data-encrypting keys (DEKs) and key-encrypting keys (KEKs)
- TLS/SSL certificates
- HSM-managed keys
- Cloud KMS keys (AWS KMS, Azure Key Vault, GCP Cloud KMS)

### 3. Overview

This procedure outlines the secure lifecycle management of cryptographic keys in accordance with PCI DSS 3.7. It ensures that all key management actions are performed securely through approved key management services, with split knowledge and dual control for manual operations, and that all activities are logged for audit purposes.

### 4. Procedure

#### 4.1 Key Generation (per PCI DSS 3.7.1)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Key Custodian / Cloud Operations Team | Create new keys using approved methods: |
| | | - Cloud KMS (AWS KMS, Azure Key Vault, GCP Cloud KMS) for cloud environments |
| | | - Hardware Security Module (HSM) for high-value operations |
| | | - Approved cryptographic libraries for application keys |
| **2** | Key Custodian | Ensure key configuration meets policy requirements: |
| | | - AES-256 for symmetric encryption |
| | | - RSA-2048+ or ECDSA P-256+ for asymmetric encryption |
| **3** | Automated (Cloud Service/HSM) | Key generation event is automatically logged with key identifier, generation time, and responsible user/role. |

#### 4.2 Key Distribution (per PCI DSS 3.7.2)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Key Custodian | Distribute keys only to authorized custodians or systems using secure methods: |
| | | - Encrypted transmission (TLS 1.2+) |
| | | - Split knowledge for manual distribution |
| | | - Secure key injection for HSMs/payment terminals |
| **2** | Key Custodian | Verify recipient identity before distribution. |
| **3** | Automated | Log all key distribution events. |

#### 4.3 Key Storage (per PCI DSS 3.7.3)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Automated (Cloud Service/HSM) | All cryptographic keys are securely stored in approved key management services. |
| **2** | Cloud Operations Team | Implement strict IAM access controls, limiting administrative access to authorized key custodians only. |
| **3** | IT Security Team | Ensure key-encrypting keys (KEKs) are stored separately from data-encrypting keys (DEKs) per PCI DSS 3.6.1. |

#### 4.4 Key Rotation (per PCI DSS 3.7.4, 3.7.5)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Cloud Operations Team / Key Custodian | Configure automated key rotation: |
| | | - Data-encrypting keys: Annual rotation |
| | | - Key-encrypting keys: Rotation per policy (e.g., every 2 years) |
| | | - TLS certificates: Annual renewal |
| **2** | Automated (Cloud Service) | Cloud service generates new backing key and associates with the key identifier. Old key retained for decryption of existing data. |
| **3** | IT Security Team | Emergency rotation triggered immediately upon: |
| | | - Known or suspected key compromise |
| | | - Key custodian termination or role change |
| **4** | Automated | Rotation event is logged with old/new key identifiers and timestamp. |

#### 4.5 Key Destruction (per PCI DSS 3.7.5)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Key Custodian | When a key is no longer required, submit key destruction request with business justification. |
| **2** | IT Security Team | Verify no data remains encrypted with the key to be destroyed. |
| **3** | Cloud Operations Team | Schedule key for deletion using cloud provider's key management service (mandatory 7-30 day waiting period). |
| **4** | Automated (Cloud Service) | Key is permanently and irreversibly deleted after waiting period. |
| **5** | Automated | Key destruction event is logged. |

#### 4.6 Manual Key Operations (per PCI DSS 3.7.6)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Key Custodians (minimum 2) | For any manual cleartext key operations, implement split knowledge and dual control. |
| **2** | Key Custodians | Each custodian knows only their portion of the key or process. |
| **3** | Key Custodians | Document manual operations with witness signatures. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1** | PCI DSS v4.0 | 3.7.1 |
| **4.2** | PCI DSS v4.0 | 3.7.2 |
| **4.3** | PCI DSS v4.0 | 3.6.1, 3.7.3 |
| **4.4** | PCI DSS v4.0 | 3.7.4, 3.7.5 |
| **4.5** | PCI DSS v4.0 | 3.7.5 |
| **4.6** | PCI DSS v4.0 | 3.7.6 |
| **4.1-4.6** | SOC 2 TSC | CC6.1, CC6.7 |

### 6. Artifact(s)

- Key generation, rotation, and destruction logs from cloud KMS/HSM
- Key custodian acknowledgment forms per PCI DSS 3.7.8
- Manual key operation documentation with witness signatures
- Key inventory showing all active keys and their cryptoperiods

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Cloud Key Management Service (KMS)** | A managed service offered by a cloud provider for creation and control of encryption keys. |
| **Customer-Managed Key (CMK)** | An encryption key within a cloud KMS that is created, owned, and managed by the customer. |
| **Data-Encrypting Key (DEK)** | A cryptographic key used to encrypt data directly. |
| **Key-Encrypting Key (KEK)** | A cryptographic key used to encrypt other cryptographic keys. |
| **Hardware Security Module (HSM)** | A physical computing device that safeguards and manages cryptographic keys. |
| **Split Knowledge** | A method where two or more people separately have key components, with each knowing only their own component. |
| **Dual Control** | A process requiring two or more people to perform a key management function. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Key Custodians** | Execute key lifecycle operations. Maintain split knowledge. Acknowledge responsibilities per PCI DSS 3.7.8. |
| **Cloud Operations Team** | Configure cloud KMS services. Implement key rotation automation. Manage IAM policies for key access. |
| **IT Security Team** | Oversee key management program. Verify compliance. Review key access logs monthly. |
| **PCI Program Manager** | Ensure key management meets PCI DSS requirements. Maintain compliance evidence for QSA review. |

