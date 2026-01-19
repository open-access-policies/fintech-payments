# Acceptable Use Violation Response Procedure (AC-PROC-001)

### 1. Purpose

To define the process for investigating, documenting, and responding to reported violations of the acceptable use policy, with enhanced procedures for violations involving cardholder data (CHD), sensitive authentication data (SAD), or customer financial information.

### 2. Scope

This procedure applies to all workforce members and all reported or detected violations of the Acceptable Use Policy (AC-POL-002). It covers violations involving:

- Company information systems and network resources
- Cardholder data environment (CDE) systems
- Systems processing nonpublic personal information (NPI)
- Any unauthorized handling of payment card data

### 3. Overview

This procedure outlines the steps for responding to potential violations of the acceptable use policy, from initial report and investigation through to documentation and sanctioning, ensuring a consistent and fair process. Violations involving cardholder data or customer financial information require additional escalation and may trigger regulatory notification requirements.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Reporter (User or Automated System) | A potential violation is reported by a user or detected by an automated system (DLP, SIEM, endpoint detection). |
| **2** | IT Security Team | Triage the report to determine if CHD, SAD, or NPI may be involved. If so, escalate immediately to the PCI Program Manager and proceed with incident response per RES-PROC-001. |
| **3** | IT Security Team | Investigate the report to validate the violation and assess its impact, including potential unauthorized access to or disclosure of sensitive data. |
| **4** | IT Security Team | Notify the employee's manager and document initial findings. |
| **5** | Manager & Human Resources | In consultation with HR, determine a sanction consistent with the Sanction Policy. |
| **6** | IT Security Team | Document the outcome formally in the security incident tracking system. |
| **7** | PCI Program Manager (if applicable) | If CHD was involved, determine if the violation constitutes a security incident requiring payment brand notification per PCI DSS 12.10.1. |
| **8** | Privacy Officer (if applicable) | If NPI was involved, assess breach notification requirements under GLBA and applicable state laws. |

**Note:** If the security team determines that the violation is critical or involves potential data breach, incident response procedures (RES-PROC-001) take precedence.

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-6** | SOC 2 TSC | CC6.8 |
| **2, 7** | PCI DSS v4.0 | 12.10.1, 12.10.5 |
| **8** | GLBA Safeguards | § 314.4(h) |

### 6. Artifact(s)

- Completed policy violation investigation report
- Incident ticket with timeline and actions taken
- Sanction documentation (maintained by HR)
- Regulatory notification records (if applicable)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Cardholder Data (CHD)** | At minimum, the full Primary Account Number (PAN). May also include cardholder name, expiration date, and service code. |
| **Nonpublic Personal Information (NPI)** | Personally identifiable financial information as defined under GLBA. |
| **Sensitive Authentication Data (SAD)** | Security-related information including full track data, card verification codes, and PINs/PIN blocks. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Reporter** | Any workforce member responsible for reporting suspected policy violations. |
| **IT Security Team** | Investigates reported violations, validates their authenticity, assesses technical impact, and determines if CHD/NPI is involved. |
| **PCI Program Manager** | Assesses violations involving cardholder data for PCI DSS compliance implications and payment brand notification requirements. |
| **Privacy Officer** | Assesses violations involving customer financial information for GLBA breach notification requirements. |
| **Managers** | Notified of violations by their direct reports and participate in determining appropriate sanctions. |
| **Human Resources** | Consulted on sanctions to ensure consistency with company policy and legal requirements. |

