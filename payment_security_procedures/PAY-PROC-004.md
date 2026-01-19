# Payment Brand Notification Procedure (PAY-PROC-004)

### 1. Purpose

To define the process for notifying payment brands (Visa, Mastercard, etc.), acquiring banks, and engaging a PCI Forensic Investigator (PFI) when a suspected or confirmed cardholder data breach occurs per PCI DSS 12.10.5.

### 2. Scope

This procedure applies to all suspected or confirmed security incidents involving:

- Potential compromise of cardholder data (CHD)
- Potential compromise of sensitive authentication data (SAD)
- Unauthorized access to the cardholder data environment (CDE)
- Attacks that may have exposed payment card data

### 3. Overview

This procedure establishes the notification workflow when a cardholder data incident is suspected or confirmed. It coordinates with incident response (RES-PROC-001) and data breach assessment (RES-PROC-002) procedures to ensure timely notification to payment brands and regulatory compliance.

### 4. Procedure

#### 4.1 Initial Assessment and Escalation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Incident Commander | Upon suspicion of CHD compromise, notifies PCI Program Manager immediately. |
| **2** | PCI Program Manager | Reviews incident details to determine if cardholder data may be affected: |
| | | - Type of data potentially exposed |
| | | - Estimated number of accounts affected |
| | | - Time period of exposure |
| | | - Systems involved |
| **3** | PCI Program Manager | Confirms whether incident involves the CDE or CHD per RES-PROC-002 data breach assessment. |
| **4** | PCI Program Manager | If CHD is potentially compromised, notifies CISO and Legal Counsel. |
| **5** | CISO | Determines notification tier based on severity: |
| | | - Tier 1: Confirmed breach with large-scale exposure |
| | | - Tier 2: Confirmed breach with limited exposure |
| | | - Tier 3: Suspected breach under investigation |

#### 4.2 Acquiring Bank Notification

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Notifies acquiring bank within **[Number, e.g., 24]** hours of confirmed or suspected CHD breach. |
| **2** | PCI Program Manager | Provides initial incident summary: |
| | | - Date and time of discovery |
| | | - Nature of suspected compromise |
| | | - Preliminary scope assessment |
| | | - Containment actions taken |
| **3** | PCI Program Manager | Documents notification including: |
| | | - Contact name and title |
| | | - Date and time of notification |
| | | - Information provided |
| | | - Next steps agreed |
| **4** | PCI Program Manager | Coordinates with acquiring bank on payment brand notification requirements. |

#### 4.3 Payment Brand Notification

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Identifies which payment brands are affected based on compromised card data. |
| **2** | PCI Program Manager | Initiates notification to each affected payment brand per their incident response procedures: |
| | | - **Visa:** What To Do If Compromised (WTDIC) program |
| | | - **Mastercard:** Account Data Compromise (ADC) program |
| | | - **American Express:** Global Data Security program |
| | | - **Discover:** Data Compromise Program |
| **3** | PCI Program Manager | Submits required notification forms with: |
| | | - Entity information |
| | | - Incident description |
| | | - Preliminary card count by BIN range |
| | | - Containment status |
| **4** | PCI Program Manager | Documents all brand communications and retains for compliance records. |

#### 4.4 PCI Forensic Investigator (PFI) Engagement

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | CISO / PCI Program Manager | Determines if PFI engagement is required based on: |
| | | - Payment brand requirements |
| | | - Acquiring bank direction |
| | | - Incident severity |
| **2** | PCI Program Manager | Selects a PFI from the PCI SSC approved list. |
| **3** | Legal Counsel | Reviews and approves PFI engagement letter (consider privilege protection). |
| **4** | PCI Program Manager | Provides PFI with: |
| | | - Scope of investigation |
| | | - System access requirements |
| | | - Evidence preservation status |
| | | - Chain of custody documentation |
| **5** | IT Security Team | Supports PFI investigation by: |
| | | - Providing system access |
| | | - Preserving evidence |
| | | - Answering technical questions |
| | | - Collecting requested data |
| **6** | PFI | Conducts investigation and provides reports to payment brands and entity. |
| **7** | PCI Program Manager | Reviews PFI findings and coordinates remediation activities. |

#### 4.5 Ongoing Communication

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Provides status updates to acquiring bank and payment brands per agreed schedule. |
| **2** | PCI Program Manager | Reports on: |
| | | - Investigation progress |
| | | - Updated scope assessment |
| | | - Remediation status |
| | | - Containment effectiveness |
| **3** | PCI Program Manager | Upon investigation completion, submits final reports to all parties. |
| **4** | PCI Program Manager | Coordinates any required re-validation of PCI DSS compliance. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1-4.5** | PCI DSS v4.0 | 12.10.5 |
| **4.1** | PCI DSS v4.0 | 12.10.1 |
| **4.4** | PCI SSC | PFI Program |
| **4.1-4.5** | Card Network Rules | Visa, Mastercard, etc. |
| **4.1-4.5** | SOC 2 TSC | CC7.4, CC7.5 |

### 6. Artifact(s)

- Incident notification log
- Payment brand notification forms
- Acquiring bank communication records
- PFI engagement letter and reports
- Status update communications
- Final incident report

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Acquiring Bank** | The financial institution that processes payment card transactions on behalf of a merchant. |
| **PCI Forensic Investigator (PFI)** | A qualified forensic investigator approved by PCI SSC to conduct investigations of cardholder data compromises. |
| **Payment Brand** | A card network such as Visa, Mastercard, American Express, Discover, or JCB. |
| **Account Data Compromise** | A security incident resulting in the unauthorized access to or exposure of cardholder data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Incident Commander** | Escalate CHD incidents to PCI Program Manager. Coordinate overall incident response. |
| **PCI Program Manager** | Lead payment brand notification process. Coordinate PFI engagement. Maintain documentation. |
| **CISO** | Approve notification decisions. Authorize PFI engagement. Oversee remediation. |
| **Legal Counsel** | Advise on notification requirements. Review PFI engagement. Protect privilege where appropriate. |
| **IT Security Team** | Support PFI investigation. Preserve evidence. Implement containment. |
| **Finance/Treasury** | Manage acquiring bank relationships. Process any fines or assessments. |

