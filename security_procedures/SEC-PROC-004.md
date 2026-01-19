# Risk Assessment Procedure (SEC-PROC-004)

### 1. Purpose

To establish a systematic process for conducting annual and ad-hoc risk assessments to identify, analyze, and evaluate risks to the organization's information assets, with specific focus on risks to cardholder data, customer financial information, and payment processing operations.

### 2. Scope

This procedure applies to all information assets and processes within the scope of the Information Security Management System (ISMS), including:

- Cardholder data environment (CDE) systems
- Systems processing nonpublic personal information (NPI)
- Payment processing systems and supporting infrastructure
- Third-party service providers handling sensitive data
- Business processes involving cardholder data or customer financial information

Risk assessments are performed annually and on an ad-hoc basis when significant changes occur, per PCI DSS 12.3.1 and GLBA § 314.4(b).

### 3. Overview

This procedure details the methodology for conducting risk assessments meeting PCI DSS, SOC 2, and GLBA requirements. It covers the identification of assets, threats, and vulnerabilities; the analysis of likelihood and impact; the calculation of risk levels; and the documentation of results in the risk register and a formal report for management and Board reporting.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Risk Assessment Team | Identifies and documents critical information assets and their owners, including: |
| | | - CDE system components per PCI DSS 12.5.1 |
| | | - Systems storing or processing NPI |
| | | - Payment processing systems |
| **2** | Risk Assessment Team | Identifies potential threats and vulnerabilities associated with each asset, including payment-specific threats (fraud, card skimming, unauthorized access to CHD). |
| **3** | Risk Assessment Team | Analyzes the likelihood of a threat exploiting a vulnerability and the potential impact to the organization, considering: |
| | | - Financial impact |
| | | - Regulatory impact (PCI DSS, GLBA violations) |
| | | - Reputational impact |
| | | - Operational impact |
| **4** | Risk Assessment Team | Calculates the overall risk level for each identified threat/vulnerability pair based on predefined risk criteria (per SEC-POL-003). |
| **5** | Risk Assessment Team | Develops risk treatment recommendations: |
| | | - Accept (with documented justification) |
| | | - Mitigate (with control recommendations) |
| | | - Transfer (via insurance or contract) |
| | | - Avoid (eliminate the risk source) |
| **6** | Risk Assessment Team | Documents results in the risk register, including identified risks, risk levels, and recommended treatments. |
| **7** | CISO / Security Officer | Compiles a formal Risk Assessment Report summarizing key findings and recommendations. |
| **8** | Executive Management | Reviews and approves risk treatment decisions, especially for high-risk items affecting the CDE or NPI. |
| **9** | Qualified Individual | Reports risk assessment results to the Board of Directors per GLBA § 314.4(i). |

**Targeted Risk Analysis (per PCI DSS 12.3.1):**
For PCI DSS requirements that allow flexibility in frequency (e.g., log reviews, vulnerability scans), conduct targeted risk analyses to determine appropriate frequencies based on:
- Asset criticality
- Threat landscape
- Historical incident data
- Regulatory requirements

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC3.1, CC3.2, CC3.3 |
| **1-8** | PCI DSS v4.0 | 12.3.1, 12.3.2 |
| **1-9** | GLBA Safeguards | § 314.4(b) |

### 6. Artifact(s)

- Asset inventory with data classification
- Threat and vulnerability assessment documentation
- Updated risk register
- Formal Risk Assessment Report
- Board reporting documentation
- Targeted risk analysis records (for PCI DSS)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Risk Register** | A log of identified risks, their characteristics, risk levels, treatment decisions, and status. |
| **Targeted Risk Analysis** | A risk analysis performed for a specific PCI DSS requirement to determine appropriate frequency of an activity. |
| **Risk Treatment** | The process of selecting and implementing measures to modify risk (accept, mitigate, transfer, avoid). |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Risk Assessment Team** | Conducts the risk assessment activities as outlined in this procedure. |
| **CISO / Security Officer** | Oversees the risk assessment process and is responsible for the final report. |
| **Asset Owners** | Provide necessary information about their assets for the risk assessment. |
| **PCI Program Manager** | Ensures CDE-related risks are properly assessed and documented for PCI DSS compliance. |
| **Qualified Individual** | Ensures risk assessment results are reported to the Board per GLBA requirements. |
| **Executive Management** | Approves risk treatment decisions for high-risk items. |

