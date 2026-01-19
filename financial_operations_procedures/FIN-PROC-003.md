# OFAC Screening Procedure (FIN-PROC-003)

### 1. Purpose

To define the process for screening customers, transactions, and counterparties against OFAC sanctions lists, ensuring prohibited transactions are blocked and reported per OFAC requirements and FIN-POL-003.

### 2. Scope

This procedure applies to:

- All customer onboarding screening
- All transaction screening
- All vendor and partner screening
- All periodic rescreening activities
- Match handling and escalation

### 3. Overview

This procedure establishes the screening workflow per OFAC compliance requirements. It covers initial screening, list updates, match review, escalation, blocking actions, and required reporting.

### 4. Procedure

#### 4.1 Screening Configuration

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Compliance Team | Configures screening system to check against: |
| | | - OFAC SDN List |
| | | - OFAC Consolidated Sanctions List |
| | | - Sectoral Sanctions Identifications (SSI) List |
| | | - Other lists based on risk assessment |
| **2** | Compliance Team | Sets screening parameters: |
| | | - Match threshold/sensitivity |
| | | - Fields to screen (name, address, country, etc.) |
| | | - Screening triggers |
| **3** | IT Team | Ensures list updates are applied within 24 hours of OFAC publication. |

#### 4.2 Customer Onboarding Screening

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Onboarding System | Automatically screens new customer against OFAC lists before account opening. |
| **2** | Screening System | Returns results: No match, Potential match, or True match. |
| **3** | Compliance Analyst | If potential match, reviews within **[Number, e.g., 24]** hours (Section 4.4). |
| **4** | Onboarding System | If no match and no pending review, proceeds with onboarding. |
| **5** | Onboarding System | If match pending review, holds account activation. |

#### 4.3 Transaction Screening

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Transaction System | For wire transfers and high-risk transactions, screens: |
| | | - Originator name and address |
| | | - Beneficiary name and address |
| | | - Intermediary banks |
| | | - Payment details/message |
| **2** | Screening System | Flags transactions with potential matches. |
| **3** | Operations Team | Holds flagged transactions pending compliance review. |
| **4** | Compliance Analyst | Reviews matches within **[Number, e.g., 4]** hours for wire transfers. |
| **5** | Operations Team | Upon clearance, releases transaction. Upon block, rejects transaction. |

#### 4.4 Match Review Process

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Compliance Analyst | Reviews potential match details: |
| | | - Name similarity |
| | | - Date of birth (if available) |
| | | - Address/country match |
| | | - Other identifying information |
| **2** | Compliance Analyst | Compares against SDN entry details: |
| | | - Full name and aliases |
| | | - Date of birth |
| | | - Nationality/citizenship |
| | | - Address |
| | | - ID numbers |
| **3** | Compliance Analyst | Determines disposition: |
| | | - **False Positive:** Customer is clearly not the listed party |
| | | - **True Match:** Customer matches SDN criteria |
| | | - **Inconclusive:** Cannot determine; escalate |
| **4** | Compliance Analyst | Documents rationale for disposition decision. |
| **5** | Compliance Analyst | If false positive, clears and allows transaction/onboarding. |
| **6** | Compliance Analyst | If true match or inconclusive, escalates to BSA/AML Officer. |

#### 4.5 True Match / Block Actions

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | BSA/AML Officer | Confirms true match determination. |
| **2** | BSA/AML Officer | Orders immediate blocking action: |
| | | - Block account |
| | | - Reject transaction |
| | | - Freeze funds in blocked account |
| **3** | Operations Team | Executes blocking action. Does NOT notify customer. |
| **4** | Compliance Team | Places blocked funds in interest-bearing blocked account. |
| **5** | BSA/AML Officer | Files blocking report with OFAC within 10 business days. |
| **6** | Compliance Team | Maintains blocked property records. |
| **7** | BSA/AML Officer | Files annual report of blocked property by September 30. |

#### 4.6 Periodic Rescreening

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Screening System | Upon OFAC list updates, automatically rescreens: |
| | | - All active customers |
| | | - All active counterparties |
| **2** | Compliance Team | Reviews any new potential matches. |
| **3** | Compliance Team | Conducts periodic batch rescreening **[Frequency, e.g., monthly]** as backup. |
| **4** | Compliance Team | Documents rescreening completion. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1-4.6** | OFAC Regulations | 31 CFR Parts 500-599 |
| **4.5** | OFAC Reporting | 31 CFR 501.603 |
| **4.1-4.6** | OFAC Framework | Compliance Commitments |

### 6. Artifact(s)

- Screening results
- Match disposition documentation
- Blocking action records
- OFAC blocking reports (filed)
- Annual blocked property report
- Rescreening logs

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **SDN (Specially Designated National)** | An individual or entity designated by OFAC whose property must be blocked. |
| **False Positive** | A screening match that, upon review, is determined not to be the actual sanctioned party. |
| **True Match** | A screening match that is confirmed to be an SDN or other blocked person. |
| **Blocking** | Freezing of property in which an SDN has an interest. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Compliance Analyst** | Review potential matches. Document dispositions. Prepare blocking reports. |
| **BSA/AML Officer** | Approve true match determinations. Authorize blocking actions. File OFAC reports. |
| **Operations Team** | Execute blocking actions. Hold transactions pending review. |
| **IT Team** | Maintain screening system. Apply list updates. |

