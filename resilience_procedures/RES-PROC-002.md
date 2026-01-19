# Data Breach Risk Assessment Procedure (RES-PROC-002)

### 1. Purpose

To guide the Security Officer and Incident Response Team through the formal risk assessment process to determine if a security incident qualifies as a notifiable data breach requiring customer, regulatory, and payment brand notification per PCI DSS 12.10.1 and GLBA requirements.

### 2. Scope

This procedure applies to any security incident involving the potential compromise of:

- Cardholder data (CHD) or sensitive authentication data (SAD)
- Customer financial information (NPI)
- Sensitive company or customer data

### 3. Overview

This procedure details the steps for conducting a formal risk assessment to determine the probability that sensitive data has been compromised and whether breach notification requirements apply under PCI DSS, GLBA, and applicable state laws.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Security Officer / IRT | Determine if the security incident involves: |
| | | - Cardholder data (PAN, cardholder name, expiration, service code) |
| | | - Sensitive authentication data (SAD) |
| | | - Customer financial information (NPI) |
| | | - Other sensitive data |
| **2** | Security Officer / IRT | Gather all available facts about the incident: |
| | | - What data was potentially accessed/exfiltrated |
| | | - How many records affected |
| | | - Time period of exposure |
| | | - Systems and data stores involved |
| | | - Whether data was encrypted and keys were also compromised |
| **3** | Security Officer / IRT | Assess the probability that sensitive data has been compromised by evaluating: |
| | | - Nature and sensitivity of the data involved |
| | | - Whether data was actually acquired, viewed, or exfiltrated |
| | | - Identity of the unauthorized person (internal vs external, targeted vs opportunistic) |
| | | - Whether encryption or other protections were in place and effective |
| | | - Extent to which risk has been mitigated |
| **4** | PCI Program Manager | For cardholder data incidents, assess: |
| | | - Whether incident triggers payment brand notification requirements |
| | | - Need for PCI Forensic Investigator (PFI) engagement |
| | | - Impact on PCI DSS compliance status |
| **5** | Privacy Officer | For NPI incidents, assess breach notification requirements under: |
| | | - GLBA Safeguards Rule |
| | | - State breach notification laws (based on affected individuals' residency) |
| | | - Contractual notification requirements |
| **6** | Legal Counsel | Review risk assessment findings and provide guidance on: |
| | | - Legal notification obligations |
| | | - Timing of notifications |
| | | - Content of notification communications |
| | | - Regulatory reporting requirements |
| **7** | Security Officer | Document the complete risk assessment findings and the final determination on the Data Breach Risk Assessment form, including: |
| | | - Summary of incident |
| | | - Data types and volume affected |
| | | - Risk factors assessed |
| | | - Determination (notifiable breach or not) |
| | | - Notification plan (if applicable) |
| **8** | Incident Commander | Execute notification plan if breach is determined to be notifiable. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC7.3, CC7.4 |
| **4** | PCI DSS v4.0 | 12.10.1, 12.10.5 |
| **5** | GLBA Safeguards | § 314.4(h) |

### 6. Artifact(s)

- Completed Data Breach Risk Assessment form
- Evidence supporting assessment conclusions
- Notification plan and execution records
- Regulatory filings (if applicable)
- Payment brand notification records (if applicable)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Sensitive Data** | Customer information, cardholder data, financial data, personal information, or confidential business information requiring protection under applicable regulations. |
| **Data Breach** | The unauthorized acquisition, access, use, or disclosure of sensitive data that compromises its security, confidentiality, or integrity. |
| **CHD** | Cardholder Data - at minimum, the full Primary Account Number (PAN). |
| **SAD** | Sensitive Authentication Data - full track data, card verification codes, and PINs/PIN blocks. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |
| **PFI** | PCI Forensic Investigator - a qualified forensic investigator approved by PCI SSC. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Security Officer** | Leads the breach risk assessment process. Documents findings and determination. |
| **Incident Response Team (IRT)** | Provides technical details and context about the security incident. |
| **PCI Program Manager** | Assesses CHD incidents for payment brand notification requirements and PFI engagement. |
| **Privacy Officer** | Assesses NPI incidents for GLBA and state law notification requirements. |
| **Legal Counsel** | Provides legal guidance on notification obligations and regulatory reporting. |
| **Incident Commander** | Executes the notification plan for confirmed breaches. |

