# Background Check Procedure (OP-PROC-006)

### 1. Purpose

To outline the formal process for conducting mandated background checks on all candidates for employment to verify their qualifications and identify any potential security risks, with enhanced screening for personnel with access to the cardholder data environment (CDE) or customer financial information per PCI DSS 12.7 and GLBA § 314.4(e).

### 2. Scope

This procedure applies to all prospective employees, contractors, and temporary staff who are extended a contingent offer of employment or engagement with the company. Enhanced screening applies to roles with:

- Access to the cardholder data environment (CDE)
- Access to customer financial information (NPI)
- Administrative or privileged system access
- BSA/AML compliance responsibilities
- Roles requiring access to encryption keys or cryptographic operations

### 3. Overview

This procedure ensures that all individuals with access to company information and systems undergo appropriate screening before their employment begins per PCI DSS 12.7.1 and GLBA § 314.4(e). It describes the steps for obtaining consent, conducting the check through an approved third-party provider, and reviewing the results to make a final hiring decision.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Human Resources (HR) | Extends a contingent offer of employment to the selected candidate. The offer explicitly states that employment is conditional upon successful completion of a background check. |
| **2** | HR | Determines screening level based on role: |
| | | - **Standard:** Criminal history, employment verification, education verification |
| | | - **Enhanced (CDE/NPI access):** Standard plus credit check, additional reference checks per PCI DSS 12.7.1 |
| | | - **Financial Role (BSA/AML):** Enhanced plus OFAC screening |
| **3** | Candidate | Provides written consent for the company to conduct a background check via the approved third-party screening provider. |
| **4** | Third-Party Provider | Conducts the background check in accordance with applicable laws (FCRA, state laws), including: |
| | | - Criminal history check |
| | | - Employment verification |
| | | - Education verification |
| | | - Credit check (for enhanced roles, where legally permitted) |
| | | - OFAC screening (for financial roles) |
| **5** | HR & Security Officer | Receive and review the background check report from the provider. |
| **6** | HR & Security Officer | If the report contains adverse findings, jointly review to determine if they pose an unacceptable risk and would disqualify the candidate. Consider: |
| | | - Nature and severity of findings |
| | | - Relevance to job responsibilities |
| | | - Time elapsed since the incident |
| | | - Role's access to CHD or NPI |
| **7** | HR | If the check is passed, confirms the final offer of employment. If not passed, follows legal requirements for adverse action (pre-adverse action notice, waiting period, final adverse action notice). |
| **8** | HR | Documents the completed background check in the candidate's confidential personnel file. For CDE roles, documents in PCI DSS compliance evidence. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC6.1 |
| **2, 4** | PCI DSS v4.0 | 12.7.1 |
| **2, 4** | GLBA Safeguards | § 314.4(e) |

### 6. Artifact(s)

- Completed background check report
- Candidate consent form
- Adverse action notices (if applicable)
- Documentation in confidential HR file
- PCI DSS compliance evidence (for CDE roles)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Contingent Offer** | An offer of employment dependent on successful fulfillment of conditions, such as a background check. |
| **Adverse Findings** | Information discovered during a background check that could negatively impact a hiring decision. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **OFAC Screening** | Verification against the Office of Foreign Assets Control sanctions lists. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Human Resources (HR)** | Manages the overall background check process, including determining screening level, making offers, obtaining consent, and maintaining records. |
| **Security Officer** | Reviews adverse findings to assess potential security risks, particularly for CDE and NPI access roles. |
| **PCI Program Manager** | Ensures background check documentation for CDE roles meets PCI DSS 12.7.1 requirements. |
| **Candidate** | Provides consent for the background check and accurate information. |
| **Third-Party Provider** | Conducts the background check in a legally compliant manner and provides a report. |

