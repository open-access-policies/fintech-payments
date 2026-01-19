# Data Retention and Disposal Policy (OP-POL-003)

## 1. Objective

This policy establishes requirements for the retention, archival, and secure disposal of **[Company Name]**'s information assets, with particular focus on cardholder data and customer financial information, in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that information is retained for appropriate periods to meet business, legal, and regulatory requirements while ensuring secure disposal when no longer needed.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, contractors, and third parties who create, process, store, or dispose of company information. It encompasses:

- All cardholder data (CHD) and sensitive authentication data (SAD)
- All customer financial information (nonpublic personal information)
- All information in any format (electronic, physical, audio, video)
- All storage media (databases, file systems, email, backup media, cloud storage, paper documents)
- All phases of the information lifecycle from creation through final disposition

## 3. Policy

**[Company Name]** implements systematic data retention and disposal practices that meet PCI DSS, SOC 2, and GLBA requirements while balancing business needs, legal obligations, and security considerations.

### 3.1 Account Data Storage Limitation

Account data storage is limited to that required for business, legal, or regulatory purposes per PCI DSS 3.2.1.

**Storage Limitation Requirements:**
- Data storage amount and retention time is limited to what is required
- Specific retention requirements are defined for each type of account data
- Business justification is documented for all stored account data
- Processes are in place to securely delete data when no longer needed

**Cardholder Data Retention:**
- PAN (masked or encrypted): Retained only for documented business, legal, or regulatory requirements
- Cardholder name, expiration date, service code: Retained only when necessary with documented justification

**Sensitive Authentication Data:**
- Full track data, CAV2/CVC2/CVV2/CID, PIN/PIN block: **NOT STORED** after authorization per PCI DSS 3.3.1
- Pre-authorization storage of SAD is minimized and rendered unrecoverable after authorization

### 3.2 Data Retention Schedule

A formal Data Retention Schedule defines retention periods for all information types.

**Schedule Maintenance:**
- Developed and maintained by **[Role Title, e.g., CISO]** in coordination with Legal
- Reviewed and updated at least annually
- Categorizes data types with specific retention periods
- Documents business, legal, and regulatory basis for each retention period

**Retention Categories:**

| **Data Category** | **Retention Period** | **Basis** |
|---|---|---|
| Cardholder data (transaction records) | **[Period, e.g., 7 years]** | PCI DSS, Card Brand Rules |
| Customer financial information (NPI) | **[Period, e.g., 7 years]** | GLBA, State Regulations |
| Audit logs and security records | 12 months minimum (3 months immediately available) | PCI DSS 10.5.1 |
| Penetration test and vulnerability scan results | 12 months | PCI DSS 11.4.1 |
| PCI DSS compliance documentation | 12 months | PCI DSS 12.10.2 |
| Financial and tax records | **[Period, e.g., 7 years]** | Tax regulations |
| Personnel records | **[Period, e.g., 7 years]** after separation | Employment law |
| Contracts and agreements | **[Period, e.g., 7 years]** after expiration | Legal requirements |
| Corporate governance records | Permanent | Corporate law |
| Operational backups | **[Period, e.g., 30 days]** | Business continuity |
| Monthly archives | **[Period, e.g., 12 months]** | Recovery requirements |

### 3.3 Quarterly Retention Review

Stored account data exceeding retention periods is securely deleted quarterly per PCI DSS 3.2.1.

**Quarterly Review Process:**
- Identify all locations where account data is stored
- Compare stored data against retention schedule
- Securely delete data exceeding defined retention periods
- Document deletion activities and verification

**Review Documentation:**
- Date of review
- Data types and locations reviewed
- Data identified for deletion
- Deletion method used
- Verification of successful deletion

### 3.4 Legal Hold and Litigation Support

Special procedures govern information retention when legal proceedings are anticipated or active.

**Legal Hold Procedures:**
- Legal hold notices issued immediately upon notification of potential litigation
- All relevant custodians notified and acknowledgment documented
- Automated deletion processes suspended for information subject to hold
- Legal hold inventory maintained documenting preserved information

**eDiscovery Support:**
- Information systems capable of identifying, preserving, and producing relevant information
- Search and collection capabilities maintained
- Chain of custody procedures followed for collected information

### 3.5 Secure Disposal Requirements

Information is securely disposed of when retention periods expire or when no longer needed per PCI DSS 3.2.1 and GLBA § 314.4(c)(6).

**Disposal Triggers:**
- Expiration of defined retention periods
- Completion of business processes requiring the information
- System decommissioning or migration activities
- Employee termination (personal information only)
- Contract termination with appropriate notice periods
- Legal hold release after litigation conclusion

**Disposal Authorization:**
- Disposal requires approval from information owner
- CDE data disposal requires PCI Program Manager notification
- Disposal of records subject to retention requirements requires Legal review

### 3.6 Secure Disposal Methods

Disposal methods correspond to information sensitivity and media type.

**Electronic Media Disposal:**

**Hard Disk Drives and SSDs:**
- Cryptographic erasure (destroying encryption keys)
- Secure overwriting using approved methods
- Degaussing (for magnetic media only)
- Physical destruction for Confidential/Regulated data or failed drives

**Removable Media (USB, optical, tape):**
- Physical destruction for cardholder data or customer NPI
- Secure overwriting for less sensitive information (if reusing media)

**Mobile Devices:**
- Factory reset combined with encryption
- Physical destruction of storage for Confidential/Regulated data
- Remote wipe verification for lost or stolen devices

**Cloud Data:**
- Cryptographic erasure using customer-managed keys
- Verification of deletion from all storage tiers and backups
- Certificate of deletion from cloud provider where available

**Physical Document Disposal:**
- Cross-cut shredding with particle size **[Size, e.g., 4mm x 32mm]** or smaller
- Incineration or pulping for bulk destruction
- Secure destruction containers prior to final destruction

### 3.7 Cardholder Data Disposal

Cardholder data is rendered unrecoverable when no longer needed per PCI DSS 9.4.6 and 9.4.7.

**Hard-Copy Materials with CHD:**
- Cross-cut shredded, incinerated, or pulped so data cannot be reconstructed
- Materials stored in secure containers prior to destruction

**Electronic Media with CHD:**
- Media destroyed, or
- Cardholder data rendered unrecoverable using industry-accepted secure deletion methods

**Verification:**
- Disposal methods verified to render data unrecoverable
- Destruction witnessed or documented for Regulated data
- Certificates of destruction obtained from third-party disposal vendors

### 3.8 Third-Party Disposal Services

External disposal services meet **[Company Name]** security requirements.

**Vendor Requirements:**
- Security assessment and approval before engagement
- Appropriate certifications (e.g., NAID AAA, R2, e-Stewards)
- Insurance coverage for data breaches
- Signed confidentiality and security agreements

**Vendor Oversight:**
- Certificates of destruction obtained and validated
- Performance monitoring and contract compliance reviews
- Audit rights exercised periodically

### 3.9 Disposal Documentation and Verification

All disposal activities are documented and verified.

**Documentation Requirements:**
- Description of information or systems disposed
- Disposal method used and justification
- Date and time of disposal activities
- Personnel involved in disposal process
- Verification of successful disposal
- Certificates of destruction from third-party vendors

**Record Retention:**
- Disposal records retained for at least **[Period, e.g., 3 years]**
- Records available for audit and compliance review

### 3.10 Customer Information Disposal

Customer information under GLBA is disposed of per regulatory requirements.

**GLBA Disposal Requirements:**
- Customer information no longer needed is securely disposed
- Disposal occurs within **[Period, e.g., 2 years]** of last use where appropriate
- Disposal methods prevent unauthorized access or reconstruction
- Disposal applies to information in any format

### 3.11 Data Retention Governance

Formal governance ensures consistent application of retention and disposal policies.

**Program Oversight:**
- **[Role Title, e.g., CISO]** responsible for overall program oversight
- Annual review of Data Retention Schedule and this policy
- Compliance monitoring and reporting
- Exception management with documented approval

**Training:**
- Workforce members trained on retention and disposal requirements
- Role-specific training for personnel handling data disposal
- Annual refresher training

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 3.2.1, 3.3.1 |
| 3.2 | PCI DSS v4.0 | 3.2.1 |
| 3.2 | GLBA Safeguards | § 314.4(c)(6) |
| 3.3 | PCI DSS v4.0 | 3.2.1 |
| 3.5 | PCI DSS v4.0 | 3.2.1 |
| 3.5 | SOC 2 TSC | CC6.5 |
| 3.5 | GLBA Safeguards | § 314.4(c)(6) |
| 3.7 | PCI DSS v4.0 | 9.4.6, 9.4.7 |
| 3.10 | GLBA Safeguards | § 314.4(c)(6) |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Account Data** | Cardholder data and/or sensitive authentication data. |
| **Cardholder Data (CHD)** | At minimum, the full Primary Account Number (PAN). May also include cardholder name, expiration date, and service code. |
| **Cryptographic Erasure** | Data destruction method that renders data unrecoverable by destroying encryption keys. |
| **Customer Information** | Any record containing nonpublic personal information about a customer (per GLBA). |
| **Legal Hold** | Suspension of normal records disposal to preserve information relevant to litigation. |
| **Media Sanitization** | Process of removing information from storage media such that recovery is not feasible. |
| **Retention Schedule** | Documented plan specifying how long different types of records should be kept. |
| **Secure Deletion** | Method of data destruction that makes recovery of deleted data infeasible. |
| **Sensitive Authentication Data (SAD)** | Full track data, card verification codes, and PINs/PIN blocks—must not be stored after authorization. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own data retention policy. Develop and maintain retention schedule. Oversee disposal program. Ensure regulatory compliance. |
| **Legal/Compliance Team** | Establish legal retention requirements. Issue legal hold notices. Support eDiscovery. Ensure compliance with applicable laws. |
| **PCI Program Manager** | Ensure cardholder data retention meets PCI DSS. Coordinate quarterly retention reviews. Verify secure disposal of CHD. |
| **IT Department** | Implement secure disposal technologies. Verify disposal completion. Manage disposal vendors. Ensure security of disposal processes. |
| **Information Owners** | Determine business retention requirements. Approve disposal activities. Participate in retention reviews. |
| **All Workforce Members** | Comply with retention requirements. Participate in legal holds. Properly dispose of information. Report disposal violations. |

