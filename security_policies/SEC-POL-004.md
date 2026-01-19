# Data Classification and Handling Policy (SEC-POL-004)

## 1. Objective

This policy establishes a comprehensive framework for classifying, handling, and protecting **[Company Name]**'s information assets, with particular focus on cardholder data (CHD), sensitive authentication data (SAD), and customer financial information in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that appropriate security controls are applied consistently to protect against unauthorized disclosure and comply with regulatory requirements.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, including employees, contractors, and third parties who create, access, process, store, transmit, or dispose of company information. It encompasses:

- All cardholder data (CHD) and sensitive authentication data (SAD)
- All nonpublic personal information (NPI) under GLBA
- All information in any format (electronic, physical, or verbal) and at any location
- The entire information lifecycle from creation to secure disposal

## 3. Policy

All **[Company Name]** information shall be classified according to its sensitivity level and handled in accordance with established security controls that protect confidentiality and integrity per PCI DSS, SOC 2, and GLBA requirements.

### 3.1 Information Classification Framework

**[Company Name]** uses a four-tier classification system to categorize all information assets, with cardholder data as a distinct category due to PCI DSS requirements.

**Public:** Information that can be freely shared with the general public without risk to **[Company Name]** or its stakeholders.
- Examples: Marketing materials, public website content, published research, press releases
- Standard business handling requirements

**Internal:** Information intended for use within **[Company Name]** that should not be disclosed to external parties without authorization.
- Examples: Internal policies, business communications, system documentation, employee contact information
- Requires access controls and confidentiality agreements

**Confidential:** Sensitive information that could cause significant harm to **[Company Name]**, its customers, or business partners if disclosed without authorization.
- Examples: Financial records, strategic plans, proprietary technology, authentication credentials, internal audit reports
- Requires enhanced security controls, encryption, audit logging, and formal access approval

**Regulated Data:** Information subject to specific regulatory requirements including cardholder data (CHD) and customer financial information (NPI).
- Examples: Primary Account Numbers (PANs), customer account information, transaction records, customer financial profiles
- Requires all Confidential controls plus specific regulatory controls (PCI DSS, GLBA)

### 3.2 Cardholder Data Classification

Cardholder data and sensitive authentication data are subject to specific classification and handling requirements per PCI DSS.

**Cardholder Data (CHD):**
- Primary Account Number (PAN) - Must always be rendered unreadable when stored
- Cardholder Name - Protected when stored with PAN
- Expiration Date - Protected when stored with PAN
- Service Code - Protected when stored with PAN

**Sensitive Authentication Data (SAD):**
- Full track data from magnetic stripe or chip
- Card verification code (CVV2/CVC2/CAV2/CID)
- PIN/PIN Block

**Critical Requirement:** Sensitive authentication data must NOT be stored after authorization, even if encrypted, per PCI DSS 3.3.1. Any pre-authorization SAD is rendered unrecoverable upon completion of authorization.

### 3.3 Customer Financial Information Classification

Nonpublic personal information (NPI) under GLBA is classified as Regulated Data and subject to specific handling requirements.

**NPI Includes:**
- Personally identifiable financial information provided by a consumer
- Information resulting from any transaction with the consumer
- Information obtained in connection with providing a financial product or service

**Examples:**
- Account numbers and balances
- Social Security Numbers
- Credit history and scores
- Income and employment information
- Transaction history

### 3.4 Information Classification Responsibilities

Information classification shall be assigned by designated information owners and applied consistently throughout the information lifecycle.

- Information owners are responsible for initial classification, approving access requests, and ensuring data is handled according to this policy.

- Classification shall be assigned at the time of creation and documented appropriately.

- When information of different classification levels is combined, the resulting information shall be classified at the highest level of any component.

- Information owners shall review the classification of their information assets annually.

- The PCI Program Manager is responsible for classification of cardholder data and maintaining the account data inventory.

### 3.5 Handling Requirements by Classification Level

Specific security controls shall be implemented based on information classification levels.

**3.5.1 Public Information**
- Standard business handling requirements
- May be stored on company systems and transmitted via standard business channels
- Standard backup and archival procedures apply

**3.5.2 Internal Information**
- Access restricted to authorized **[Company Name]** workforce members
- Password-protected when stored on portable devices
- Transmitted via secure channels (encrypted email, secure file transfer)
- Stored on company-approved systems with appropriate access controls
- Covered by confidentiality agreements for third-party access

**3.5.3 Confidential Information**
- Access granted only on a need-to-know basis with formal approval
- Encrypted when stored on laptops, mobile devices, or removable media using AES-256
- Transmitted only via encrypted channels (secure email, VPN, HTTPS)
- Stored on secure systems with enhanced access controls and audit logging
- Protected by multi-factor authentication for system access
- All access logged and monitored for unauthorized activity
- Requires appropriate agreements for third-party access
- Must be clearly labeled to indicate classification level
- Subject to data loss prevention (DLP) monitoring and controls

**3.5.4 Regulated Data (CHD and NPI)**

All Confidential handling requirements apply, plus:

**Storage Requirements (per PCI DSS 3.4, 3.5):**
- PAN is rendered unreadable anywhere it is stored using:
  - One-way hashes based on strong cryptography
  - Truncation (hashing cannot replace truncated segments)
  - Index tokens (tokenization)
  - Strong cryptography with associated key management
- Encryption uses AES-256 or equivalent
- Key management follows OP-POL-001 (Encryption and Key Management Policy)

**Display Requirements (per PCI DSS 3.4):**
- PAN is masked when displayed (BIN and last four digits maximum)
- Only personnel with documented business need can see full PAN
- List of roles with access to full PAN is maintained with business justification

**Copy/Relocation Requirements (per PCI DSS 3.4.2):**
- Technical controls prevent copy and/or relocation of PAN for remote-access technologies
- Only personnel with documented authorization and legitimate business need may copy PAN

**Storage Locations:**
- Stored only within the defined cardholder data environment (CDE)
- Cloud storage requires compliance with all PCI DSS requirements
- Backup media encrypted and securely stored
- Inventory of all storage locations is maintained

**Access Controls:**
- Access granted based on need-to-know and job responsibility
- Multi-factor authentication required for CDE access
- Access reviewed at least every six months
- All access logged and retained for one year minimum

### 3.6 Data Labeling and Marking

Information classification shall be clearly indicated through appropriate labeling mechanisms.

- Electronic documents shall include classification markings in headers, footers, or metadata when feasible
- Email communications containing Confidential or Regulated information shall include classification indicators
- Physical documents shall be marked with classification levels
- Storage media shall be labeled with the highest classification level of contained information
- Systems containing cardholder data shall be identified in the CDE inventory

### 3.7 Information Transmission

Information transmission methods shall align with classification and regulatory requirements.

**Public and Internal:** May be transmitted via standard business communication channels.

**Confidential:** Encrypted during transmission using TLS 1.2 or higher.

**Regulated Data (CHD) - per PCI DSS 4.2:**
- Strong cryptography protects PAN during transmission over open, public networks
- Only trusted keys and certificates are accepted
- Certificates are confirmed as valid and not expired or revoked
- Protocols support only secure versions (no fallback to insecure versions)
- PAN is secured with strong cryptography whenever sent via end-user messaging (email, SMS, chat)

**Customer Financial Information (NPI):**
- Encrypted in transit over external networks per GLBA § 314.4(c)(3)
- Internal transmission uses encryption where technically feasible

### 3.8 Data Retention and Disposal

Information shall be retained according to business and regulatory requirements and then securely disposed of per PCI DSS 3.2 and GLBA § 314.4(c)(6).

**Retention Requirements:**
- Retention schedules are established for each information type considering business, legal, and regulatory requirements
- Account data storage is limited to that required for business, legal, or regulatory purposes per PCI DSS 3.2.1
- Customer financial information is retained for minimum **[Number, e.g., 7]** years per regulatory requirements

**Retention Documentation:**
- Specific retention requirements are defined for each type of account data
- Business justification is documented for storage
- Data locations are identified in the data inventory

**Disposal Requirements (per PCI DSS 3.2.1 and GLBA § 314.4(c)(6)):**
- Quarterly verification that stored account data exceeding retention periods has been securely deleted
- Secure disposal methods are used:
  - Electronic media: Cryptographic erasure, degaussing, or physical destruction
  - Physical documents: Cross-cut shredding or secure destruction
- Disposal activities are documented
- Third-party disposal services provide certificates of destruction
- Customer information no longer needed is securely disposed of within two years of last use per GLBA

### 3.9 Account Data Inventory

An inventory of all cardholder data and sensitive authentication data locations shall be maintained per PCI DSS 12.5.1.

**Inventory Requirements:**
- All locations where account data is stored, processed, or transmitted are documented
- All system components in the CDE are identified
- Data flow diagrams document movement of account data
- Inventory is reviewed and validated at least annually per PCI DSS 12.5.2

**Data Discovery:**
- Periodic scans are conducted to identify unauthorized storage of PAN
- If stored PAN is detected outside the CDE, incident response procedures apply per PCI DSS 12.10.7

### 3.10 Mobile Device and Remote Access

Appropriate controls apply to information access via mobile devices and remote locations.

- Mobile devices accessing Regulated Data shall be enrolled in mobile device management (MDM) systems
- Remote access to cardholder data or customer financial information requires VPN and multi-factor authentication
- Personal devices used for business purposes shall comply with approved security requirements
- Lost or stolen devices shall be reported immediately and remotely wiped if containing sensitive information
- Cardholder data and customer NPI may not be stored locally on personal devices

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1, 3.4 | SOC 2 TSC | CC6.1 |
| 3.2 | PCI DSS v4.0 | 3.2.1, 3.3.1, 3.3.2, 3.3.3 |
| 3.3 | GLBA Safeguards | § 314.4(c)(3) |
| 3.5.4 | PCI DSS v4.0 | 3.4.1, 3.4.2, 3.5.1 |
| 3.5.4 | GLBA Safeguards | § 314.4(c)(1), § 314.4(c)(3) |
| 3.5.4 | SOC 2 TSC | CC6.1, C1.1 |
| 3.6 | PCI DSS v4.0 | 12.5.1 |
| 3.7 | PCI DSS v4.0 | 4.2.1, 4.2.2 |
| 3.7 | SOC 2 TSC | CC6.7 |
| 3.7 | GLBA Safeguards | § 314.4(c)(3) |
| 3.8 | PCI DSS v4.0 | 3.2.1 |
| 3.8 | SOC 2 TSC | CC6.5 |
| 3.8 | GLBA Safeguards | § 314.4(c)(6) |
| 3.9 | PCI DSS v4.0 | 12.5.1, 12.5.2, 12.10.7 |
| 3.10 | PCI DSS v4.0 | 8.4.3 |
| 3.10 | GLBA Safeguards | § 314.4(c)(5) |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data (CHD)** | At minimum, the full Primary Account Number (PAN). May also include cardholder name, expiration date, and service code. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Customer Information** | Any record containing nonpublic personal information about a customer, whether in paper, electronic, or other form (per GLBA). |
| **Data Loss Prevention (DLP)** | Technology and processes designed to detect and prevent unauthorized transmission of sensitive information. |
| **Information Owner** | The person responsible for the business content and context of information, including classification and access decisions. |
| **Mobile Device Management (MDM)** | Software that manages, monitors, and secures mobile devices across the organization. |
| **Nonpublic Personal Information (NPI)** | Personally identifiable financial information and any list, description, or grouping of consumers derived from such information. |
| **Primary Account Number (PAN)** | Unique payment card number (typically 15-16 digits) that identifies the issuer and cardholder account. |
| **Sensitive Authentication Data (SAD)** | Security-related information including full track data, card verification codes (CVV2/CVC2/CAV2), and PINs/PIN blocks. |
| **Tokenization** | The process of replacing sensitive data with non-sensitive placeholders (tokens) that have no exploitable value. |
| **Truncation** | The practice of permanently removing a segment of the PAN so that only part of the number is stored. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Information Owners** | Classify information assets, approve access requests, conduct periodic classification reviews, and ensure appropriate handling. |
| **Chief Information Security Officer (CISO)** | Develop and maintain classification policies, oversee compliance, and investigate classification violations. |
| **PCI Program Manager** | Maintain account data inventory. Ensure cardholder data handling meets PCI DSS requirements. Validate data flow diagrams. Coordinate data discovery activities. |
| **IT Security Team** | Implement technical controls for each classification level. Conduct data discovery scans. Monitor for unauthorized data storage. Manage DLP systems. |
| **IT Department** | Provide secure storage and transmission capabilities. Implement encryption controls. Execute secure disposal procedures. |
| **All Workforce Members** | Follow classification and handling requirements. Properly label information. Report suspected violations or data loss. Never store SAD after authorization. |
| **Managers/Supervisors** | Ensure their teams understand and comply with classification requirements. Approve access requests within their authority. |

