# Disciplinary Action for Security Policy Violations Procedure (OP-PROC-008)

### 1. Purpose

To describe the formal process for documenting violations of information security policies and applying consistent, fair, and appropriate disciplinary actions, with enhanced requirements for violations involving cardholder data or customer financial information per PCI DSS 12.1.4.

### 2. Scope

This procedure applies to all members of the workforce, including employees, contractors, and temporary staff, who are found to be in violation of the company's established information security policies, including:

- Information Security Policy
- Acceptable Use Policy
- Data Classification and Handling Policy
- PCI DSS compliance requirements
- GLBA/NPI handling requirements

### 3. Overview

This procedure ensures that security policy violations are handled in a structured and predictable manner per PCI DSS 12.1.4. It outlines the steps for identifying a violation, conducting an investigation, determining a commensurate disciplinary action in consultation with Human Resources, and formally documenting the outcome. Violations involving cardholder data or customer financial information may trigger additional reporting requirements.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Manager or Security Officer | Identifies a potential violation of an information security policy through a report, an audit finding, or a security alert. Notes whether violation involves: |
| | | - Cardholder data (CHD) or sensitive authentication data (SAD) |
| | | - Customer financial information (NPI) |
| | | - CDE systems |
| **2** | Security Officer & Manager | Conduct an investigation to gather facts and evidence related to the potential violation. This may involve reviewing logs, interviewing individuals, and analyzing data. |
| **3** | Security Officer, Manager, & HR | Review the findings of the investigation to confirm whether a policy violation occurred. |
| **4** | Manager & HR | In consultation with the Security Officer, determine the appropriate disciplinary action. The sanction is commensurate with: |
| | | - Severity of the violation |
| | | - Impact on data security (especially CHD/NPI) |
| | | - Whether violation was intentional or negligent |
| | | - Employee's history |
| **5** | Manager & HR | Formally document the violation and the resulting sanction using a standard disciplinary action form. The documentation is stored in the employee's confidential HR file. |
| **6** | Manager | Communicates the decision and the sanction to the employee. |
| **7** | Security Officer | For violations involving CHD or NPI: Assesses whether the violation constitutes a security incident requiring escalation per RES-PROC-001. |
| **8** | PCI Program Manager | For CHD-related violations: Documents the violation and response for PCI DSS compliance evidence. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC1.2, CC1.4 |
| **1-8** | PCI DSS v4.0 | 12.1.4 |
| **1-8** | GLBA Safeguards | § 314.4(e) |

### 6. Artifact(s)

- Formal disciplinary action form or memo
- Investigation findings documentation
- Evidence collection records
- HR personnel file documentation
- PCI DSS compliance records (for CHD-related violations)
- Incident report cross-reference (if applicable)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Sanction** | A penalty or disciplinary action imposed for violating a policy or rule. |
| **Commensurate** | Corresponding in size, extent, amount, or degree; proportionate. |
| **CHD** | Cardholder Data - at minimum, the full Primary Account Number (PAN). May also include cardholder name, expiration date, and service code. |
| **SAD** | Sensitive Authentication Data - full track data, card verification codes, and PINs/PIN blocks. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Manager** | Responsible for identifying and reporting potential violations and for communicating disciplinary actions. |
| **Security Officer** | Responsible for investigating potential security policy violations and assessing incident escalation needs. |
| **Human Resources (HR)** | Responsible for ensuring the sanction process is fair, consistent, and legally compliant, and for maintaining official records. |
| **PCI Program Manager** | Ensures CHD-related violations are documented for PCI DSS compliance. |

