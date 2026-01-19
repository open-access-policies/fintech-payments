# Wire Transfer Compliance Procedure (FIN-PROC-005)

### 1. Purpose

To define the process for ensuring wire transfer compliance with BSA recordkeeping requirements, Travel Rule, OFAC screening, and security controls per FIN-POL-004.

### 2. Scope

This procedure applies to:

- All domestic wire transfers
- All international wire transfers
- Wire transfer initiation, approval, and release
- Compliance screening and monitoring

### 3. Overview

This procedure establishes the workflow for wire transfer processing with appropriate BSA/AML and OFAC controls, ensuring regulatory compliance and fraud prevention.

### 4. Procedure

#### 4.1 Wire Transfer Initiation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Customer / Authorized User | Submits wire transfer request with required information: |
| | | - Originator name and address |
| | | - Originator account number |
| | | - Beneficiary name and address |
| | | - Beneficiary account number |
| | | - Beneficiary bank details (SWIFT, ABA) |
| | | - Amount and currency |
| | | - Purpose of payment |
| **2** | Wire Operations | Verifies customer authorization: |
| | | - Customer identity verified |
| | | - Authorization matches account signature/authority |
| | | - Request within customer's wire limits |
| **3** | Wire Operations | For large or unusual wires, performs callback verification using known customer number. |

#### 4.2 Compliance Screening

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Screening System | Automatically screens wire against OFAC lists: |
| | | - Originator name |
| | | - Beneficiary name |
| | | - Beneficiary bank |
| | | - Message content |
| | | - Countries involved |
| **2** | Screening System | Flags potential matches or high-risk indicators. |
| **3** | Wire Operations | Holds flagged wires pending compliance review. |
| **4** | Compliance Analyst | Reviews flagged wires within **[Number, e.g., 4]** hours. |
| **5** | Compliance Analyst | Dispositions as: |
| | | - Cleared: Proceed with processing |
| | | - Blocked: OFAC block per FIN-PROC-003 |
| | | - Rejected: Return to customer |
| | | - Suspicious: Process and file SAR |

#### 4.3 Travel Rule Compliance

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Wire Operations | For wires of $3,000 or more, ensures required information is included: |
| | | - Originator name |
| | | - Originator address (or account number for domestic) |
| | | - Originator account number |
| | | - Beneficiary name |
| | | - Beneficiary account number |
| **2** | Wire Operations | Includes all required fields in wire message. |
| **3** | Wire Operations | For international wires, includes full beneficiary address. |
| **4** | Wire Operations | Retains transmittal order records for 5 years. |

#### 4.4 Wire Approval and Release

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Wire Operations | Prepares wire for release. |
| **2** | Wire Operations | For wires above **[$Amount, e.g., $50,000]**, obtains secondary approval. |
| **3** | Approver | Reviews wire details and approves. |
| **4** | Wire Operations | Releases wire through correspondent bank/Fed. |
| **5** | Wire System | Logs wire details for recordkeeping. |

#### 4.5 Monitoring and Suspicious Activity

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Transaction Monitoring | Monitors wire activity for patterns: |
| | | - High-risk corridors |
| | | - Unusual frequency |
| | | - Round-dollar amounts |
| | | - Rapid movement |
| **2** | Compliance Analyst | Investigates generated alerts. |
| **3** | Compliance Analyst | If suspicious, prepares SAR per FIN-PROC-002. |

#### 4.6 International Wire Enhanced Review

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Wire Operations | For international wires to high-risk countries: |
| | | - Reviews customer purpose for wire |
| | | - Verifies consistency with customer profile |
| | | - Documents review |
| **2** | Compliance Analyst | Reviews wires to FATF high-risk jurisdictions. |
| **3** | Wire Operations | Blocks wires to sanctioned countries per FIN-POL-003. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1-4.6** | BSA Recordkeeping | 31 CFR 1010.410 |
| **4.3** | Travel Rule | 31 CFR 1010.410(f) |
| **4.2** | OFAC Regulations | 31 CFR Parts 500-599 |
| **4.1-4.6** | FATF Recommendation 16 | Wire Transfer Rule |

### 6. Artifact(s)

- Wire transfer request documentation
- OFAC screening results
- Approval records
- Wire confirmation
- Travel Rule compliance documentation
- SAR filings (if applicable)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Travel Rule** | BSA requirement to include and transmit originator and beneficiary information with funds transfers. |
| **Transmittal Order** | The wire transfer instruction including all required information. |
| **Correspondent Bank** | An intermediary bank that processes wire transfers on behalf of other banks. |
| **SWIFT** | The global messaging network used for international wire transfers. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Wire Operations** | Process wires per procedure. Verify authorization. Apply Travel Rule. Hold flagged wires. |
| **Compliance Analyst** | Review OFAC hits. Investigate suspicious patterns. File SARs. |
| **Approver** | Approve high-value wires. Verify appropriateness. |
| **BSA/AML Officer** | Oversee wire compliance. Approve OFAC decisions. Monitor program effectiveness. |

