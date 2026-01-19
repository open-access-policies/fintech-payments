# Tokenization Management Procedure (PAY-PROC-003)

### 1. Purpose

To define the operational procedures for managing tokenization services including token generation, vault operations, de-tokenization requests, and lifecycle management to protect cardholder data per PCI DSS 3.5.1.

### 2. Scope

This procedure applies to all tokenization operations including:

- Token generation and assignment
- Token vault administration
- De-tokenization request processing
- Token lifecycle management (expiration, revocation)
- Third-party tokenization service management

### 3. Overview

This procedure establishes the operational workflow for tokenization services per PCI DSS requirements. It covers token provisioning, controlled de-tokenization, and ongoing vault operations to ensure cardholder data protection and PCI DSS scope reduction.

### 4. Procedure

#### 4.1 Token Generation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Application System | Receives PAN requiring tokenization (e.g., during customer card-on-file registration). |
| **2** | Tokenization Service | Validates the request source is authorized. |
| **3** | Tokenization Service | Checks if a token already exists for this PAN/merchant combination. |
| **4** | Tokenization Service | If new, generates a cryptographically random token that cannot be reversed to derive PAN. |
| **5** | Tokenization Service | Stores the token-to-PAN mapping in the encrypted token vault. |
| **6** | Tokenization Service | Returns the token to the requesting application. |
| **7** | Application System | Stores the token in place of PAN for future use. |

#### 4.2 De-Tokenization Requests

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Authorized System | Initiates de-tokenization request with token and business reason. |
| **2** | Tokenization Service | Validates the requesting system is authorized for de-tokenization. |
| **3** | Tokenization Service | Verifies the request includes a valid business reason from approved list: |
| | | - Payment authorization |
| | | - Settlement processing |
| | | - Chargeback handling |
| | | - Fraud investigation |
| | | - Regulatory requirement |
| **4** | Tokenization Service | Logs the de-tokenization request including: |
| | | - Timestamp |
| | | - Requesting system/user |
| | | - Token identifier |
| | | - Business reason |
| **5** | Tokenization Service | Retrieves PAN from token vault and returns to authorized system. |
| **6** | Authorized System | Uses PAN only for approved purpose, does not store outside CDE. |

#### 4.3 Token Vault Administration

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Vault Administrator | Accesses vault administration interface using MFA. |
| **2** | Vault Administrator | For sensitive operations (bulk deletion, export), requires dual control with second administrator. |
| **3** | Vault Administrator | All administrative actions are logged with administrator identity and action details. |
| **4** | IT Security Team | Reviews vault administrative logs **[Frequency, e.g., weekly]** for anomalies. |
| **5** | Vault Administrator | Monitors vault capacity and performance. |

#### 4.4 Token Lifecycle Management

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Tokenization Service | Identifies tokens approaching expiration based on policy. |
| **2** | Application Team | Initiates token refresh process if continued use is required. |
| **3** | Tokenization Service | Generates new token, updates mapping, invalidates old token. |
| **4** | Tokenization Service | For revoked tokens, removes mapping from vault. |
| **5** | PCI Program Manager | Reviews token population **[Frequency, e.g., quarterly]** for optimization. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1, 4.2** | PCI DSS v4.0 | 3.5.1 |
| **4.2** | PCI DSS v4.0 | 10.2.1 |
| **4.3** | PCI DSS v4.0 | 3.6.1, 7.2.1 |
| **4.4** | PCI DSS v4.0 | 3.5.1 |
| **4.1-4.4** | PCI SSC | Tokenization Guidelines |
| **4.1-4.4** | SOC 2 TSC | CC6.1 |

### 6. Artifact(s)

- Token generation logs
- De-tokenization request logs
- Vault administration logs
- Token lifecycle reports
- Capacity monitoring reports

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **De-Tokenization** | The process of exchanging a token for its associated PAN value. |
| **Token** | A surrogate value that replaces sensitive data and has no exploitable value if compromised. |
| **Token Vault** | A secure database that stores the mapping between tokens and their corresponding PAN values. |
| **Dual Control** | A process that requires two or more authorized individuals to complete an action. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Tokenization Service** | Generate tokens, process de-tokenization requests, maintain vault security. |
| **Vault Administrator** | Perform vault administration, monitor capacity, execute lifecycle management. |
| **IT Security Team** | Monitor vault access logs, investigate anomalies, maintain vault security controls. |
| **Application Team** | Integrate with tokenization services, manage token lifecycle for applications. |
| **PCI Program Manager** | Ensure tokenization procedures meet PCI DSS requirements, maintain documentation. |

