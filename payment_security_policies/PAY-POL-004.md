# Tokenization and Data Masking Policy (PAY-POL-004)

## 1. Objective

This policy establishes **[Company Name]**'s requirements for implementing tokenization and data masking solutions to protect cardholder data (CHD) and reduce PCI DSS scope. It defines the standards for token generation, vault security, masking formats, and operational procedures to ensure that sensitive payment data is protected while maintaining business functionality.

## 2. Scope

This policy applies to:

- All tokenization systems used to protect cardholder data
- All data masking implementations for PAN and other sensitive data
- All systems that generate, store, use, or process tokens
- All applications that display masked or tokenized data
- All personnel responsible for tokenization and masking systems
- All third-party tokenization service providers

## 3. Policy

**[Company Name]** shall implement tokenization and data masking as primary methods for protecting cardholder data, reducing PCI DSS scope, and minimizing the risk of data compromise.

### 3.1 Tokenization Standards

Tokenization systems shall meet industry standards and PCI DSS requirements.

**Token Generation:**
- Tokens are generated using methods that cannot be reversed to derive the original PAN without access to the token vault
- Token generation uses cryptographically secure random number generation
- Tokens have no mathematical relationship to the original PAN
- Token format is distinguishable from live PANs to prevent processing errors

**Token Format Options:**
- Numeric tokens preserving PAN length for legacy system compatibility
- Format-preserving tokens maintaining first/last digit patterns where required
- Alphanumeric tokens for systems supporting expanded character sets
- Token format is documented and consistent within each use case

**Token Types:**
- Single-use tokens for one-time transactions
- Multi-use tokens for recurring payments and stored credentials
- Merchant-specific tokens bound to a single merchant
- Network tokens provided by payment networks

**PCI SSC Compliance:**
- Tokenization systems comply with PCI SSC Tokenization Product Security Guidelines
- Third-party tokenization solutions are validated against PCI SSC guidelines
- In-house tokenization solutions are reviewed against PCI SSC guidelines

### 3.2 Token Vault Security

The token vault (mapping database) shall be secured as part of the CDE per PCI DSS 3.5.

**Vault Architecture:**
- Token vault is isolated within a dedicated security zone
- Access to the vault is restricted to authorized systems and personnel
- Vault architecture supports high availability and disaster recovery
- Vault infrastructure meets all PCI DSS requirements

**Vault Access Controls:**
- Access to token-to-PAN mappings requires multi-factor authentication
- Role-based access limits who can view, modify, or delete mappings
- All vault access is logged with detailed audit trails
- Administrative access requires dual control for sensitive operations

**Vault Encryption:**
- Token mappings are encrypted at rest using AES-256 or equivalent
- Encryption keys are managed per OP-POL-001 (Encryption and Key Management Policy)
- Key-encrypting keys are stored separately from the vault
- Hardware Security Modules (HSMs) are used for vault key management where feasible

**Vault Operations:**
- Token vault backup follows CDE backup requirements
- Vault recovery procedures are tested annually
- Vault capacity and performance are monitored
- Token lifecycle management includes expiration and revocation

### 3.3 De-Tokenization Controls

De-tokenization (converting tokens back to PANs) shall be strictly controlled.

**De-Tokenization Authorization:**
- Only authorized systems and applications can request de-tokenization
- De-tokenization requests require authentication and authorization
- Business justification for de-tokenization is documented
- List of authorized de-tokenization use cases is maintained

**Approved De-Tokenization Scenarios:**
- Payment authorization and settlement
- Chargeback and dispute processing
- Customer service with documented business need
- Regulatory and legal requirements
- Fraud investigation

**De-Tokenization Logging:**
- All de-tokenization requests are logged with requestor identification
- Logs include timestamp, token, requestor system/user, and reason
- De-tokenization logs are retained for **[Number, e.g., 12]** months minimum
- Unusual de-tokenization patterns trigger alerts

**Restrictions:**
- Bulk de-tokenization is prohibited without CISO approval
- De-tokenized PANs are not stored outside the CDE
- De-tokenized PANs are used only for the approved purpose
- Applications minimize time that de-tokenized PANs are in memory

### 3.4 PAN Masking Standards

PAN masking shall protect full PAN while maintaining business utility per PCI DSS 3.4.

**Masking Format:**
- Maximum display: BIN (first six digits) and last four digits
- Standard mask format: ****-****-****-1234 or 123456******1234
- Masking character is consistent across applications (asterisk or X)
- Masked PAN is clearly distinguishable from truncated PAN

**Display Masking:**
- Web applications display masked PANs by default
- Customer service interfaces show masked PANs
- Reports and exports use masked PANs unless full PAN is required
- Print and paper documents use masked PANs

**Authorization for Full PAN Display:**
- Roles authorized to view full PAN are documented with business justification
- Access to full PAN requires documented approval
- List of authorized roles is reviewed **[Frequency, e.g., quarterly]**
- Full PAN display is logged

**Technical Implementation:**
- Masking is applied at the application layer before display
- Masking functions are centralized and reusable
- Applications cannot bypass masking controls
- Masking is validated through security testing

### 3.5 Truncation vs. Masking

Truncation and masking are distinct and shall be implemented correctly.

**Truncation:**
- Truncation permanently removes digits; truncated data cannot be restored
- Truncated PANs may be stored without encryption (only BIN and last 4)
- Truncation is applied before storage
- Truncated data is not considered full PAN for PCI DSS scope

**Masking:**
- Masking conceals digits for display but full PAN remains in the system
- Masked PANs can be "unmasked" if system stores full PAN
- Masking is applied at display time
- Systems storing full PAN remain in CDE scope

**Correlation Controls:**
- If hashed and truncated versions of the same PAN exist, controls prevent correlation
- Multiple truncation formats of the same PAN have correlation controls
- Risk assessment addresses correlation of tokenized, hashed, and truncated data

### 3.6 Network Tokenization

Payment network tokens shall be implemented according to payment brand specifications.

**Network Token Support:**
- EMVCo-specification network tokens are supported where available
- Token Service Provider (TSP) integration follows payment network requirements
- Network token lifecycle management is implemented
- Token requestor registration is maintained with payment networks

**Use Cases:**
- Stored credentials for recurring payments
- Card-on-file for e-commerce
- Digital wallet provisioning
- In-app payments

**Benefits and Requirements:**
- Network tokens may provide liability shift and improved authorization rates
- Token provisioning flows are secured
- Token cryptograms are validated
- Token updates (PAR) are processed appropriately

### 3.7 Tokenization Service Provider Management

Third-party tokenization providers shall meet security requirements.

**Provider Requirements:**
- Provider is PCI DSS compliant (validated with current AOC)
- Provider meets PCI SSC Tokenization Product Security Guidelines
- Provider has appropriate SOC 2 Type II attestation
- Provider supports required token formats and use cases

**Contractual Requirements:**
- Service agreement defines security responsibilities
- Provider acknowledges responsibility for CHD security per PCI DSS 12.8.2
- Service level agreements address availability and performance
- Incident notification requirements are documented

**Ongoing Monitoring:**
- Provider compliance status is verified annually
- Provider security incidents are monitored
- Provider changes affecting security are assessed
- Provider performance is monitored against SLAs

### 3.8 Scope Reduction

Tokenization shall be implemented to reduce PCI DSS scope effectively.

**Scope Reduction Principles:**
- Tokens used in place of PANs remove systems from CDE scope
- Token vault remains in scope as it can access PANs
- Systems with de-tokenization capability remain in scope
- Connected systems are assessed for scope impact

**Scope Documentation:**
- Tokenization boundaries are documented in network diagrams
- Data flow diagrams show token flows vs. PAN flows
- Scope reduction from tokenization is validated during assessments
- Changes to tokenization affecting scope are documented

**Segmentation:**
- Token vault is segmented from out-of-scope systems
- Segmentation effectiveness is tested per PCI DSS 11.4.5
- Network controls restrict access to token vault
- Monitoring detects unauthorized access attempts

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 3.5.1 |
| 3.1 | PCI SSC | Tokenization Product Security Guidelines |
| 3.2 | PCI DSS v4.0 | 3.5.1, 3.6.1, 3.7.1-3.7.8 |
| 3.2 | SOC 2 TSC | CC6.1 |
| 3.3 | PCI DSS v4.0 | 3.4.2, 10.2.1 |
| 3.4 | PCI DSS v4.0 | 3.4.1 |
| 3.5 | PCI DSS v4.0 | 3.5.1 |
| 3.6 | EMVCo | Token Service Specification |
| 3.7 | PCI DSS v4.0 | 12.8.1-12.8.5 |
| 3.8 | PCI DSS v4.0 | 12.5.1, 11.4.5 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **De-Tokenization** | The process of exchanging a token for its associated PAN value. |
| **Format-Preserving Token** | A token that maintains the same format (length and character type) as the original data. |
| **Masking** | Concealing a portion of data during display while the original data remains stored in the system. |
| **Network Token** | A token generated by a payment network's Token Service Provider to replace a PAN for specific use cases. |
| **Token** | A surrogate value that replaces sensitive data and has no exploitable value if compromised. |
| **Token Service Provider (TSP)** | An entity that provides token generation, vault services, and de-tokenization capabilities. |
| **Token Vault** | A secure database that stores the mapping between tokens and their corresponding PAN values. |
| **Truncation** | Permanently removing a portion of data so it cannot be reconstructed; distinct from masking. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Approve tokenization architecture. Authorize de-tokenization exceptions. Oversee tokenization security. |
| **PCI Program Manager** | Ensure tokenization meets PCI DSS requirements. Document scope reduction. Coordinate with QSA. |
| **IT Security Team** | Manage token vault security. Configure access controls. Monitor de-tokenization activity. Conduct security testing. |
| **Development Team** | Implement tokenization in applications. Integrate with token services. Implement masking controls. |
| **Operations Team** | Operate token vault infrastructure. Manage backups and recovery. Monitor performance. |
| **Application Owners** | Ensure applications use tokenization appropriately. Document token use cases. Maintain token format requirements. |

