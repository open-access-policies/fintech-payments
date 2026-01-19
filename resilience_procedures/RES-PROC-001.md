# Incident Response Procedure (RES-PROC-001)

### 1. Purpose

To provide detailed, actionable steps for responding to information security incidents affecting cardholder data, customer financial information, or company systems to minimize impact and ensure a coordinated response per PCI DSS 12.10 and GLBA § 314.4(h).

### 2. Scope

This procedure applies to all personnel involved in the incident response process and covers all information systems and data, including:

- Cardholder data environment (CDE) systems
- Systems processing customer financial information (NPI)
- Payment processing systems
- All company information systems and data

### 3. Overview

This procedure outlines the formal process for managing information security incidents, from initial detection and analysis through containment, eradication, recovery, and post-incident review, following the NIST incident response lifecycle and meeting PCI DSS 12.10 requirements.

### 4. Procedure

| **Step** | **Phase** | **Who** | **What** |
|----------|-----------|---------|----------|
| **1** | **Preparation** | IT Security Team | Conduct annual incident response training and exercises per PCI DSS 12.10.2. |
| **2** | | IT Security Team | Maintain and test incident response tools and systems. |
| **3** | | IT Security Team | Maintain 24/7 contact information for incident response per PCI DSS 12.10.3. |
| **4** | **Detection & Analysis** | All Personnel | Report suspected incidents to the IT Security Team immediately via **[Contact Method, e.g., security@company.com or incident hotline]**. |
| **5** | | Security Analyst | Triage and classify incoming alerts and reports to determine if an incident has occurred. |
| **6** | | Security Analyst | Determine if cardholder data, SAD, or NPI may be affected. If so, escalate immediately. |
| **7** | | Incident Commander | For confirmed incidents, activate the Incident Response Team (IRT) per PCI DSS 12.10.1. |
| **8** | **Containment, Eradication, & Recovery** | IRT | Isolate affected systems to prevent further damage while preserving evidence. |
| **9** | | IRT | Identify and remove the root cause (malware, unauthorized access, vulnerability). |
| **10** | | IRT | For CHD incidents: Preserve evidence for forensic investigation per PCI DSS 12.10.5. |
| **11** | | IRT | Restore systems to normal operation from clean backups, validating integrity. |
| **12** | **Notification** | Incident Commander | For CHD compromise: Notify payment brands within 24 hours per card brand rules. |
| **13** | | Privacy Officer | For NPI breach: Assess and execute GLBA and state breach notification requirements. |
| **14** | | BSA/AML Officer | If incident involves potential money laundering or fraud, assess SAR filing requirements. |
| **15** | **Post-Incident Activity** | Incident Commander | Conduct post-incident review (lessons learned) meeting. |
| **16** | | Incident Commander | Complete and file formal Incident Report per PCI DSS 12.10.4. |
| **17** | | IT Security Team | Update incident response plan based on lessons learned per PCI DSS 12.10.6. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-17** | SOC 2 TSC | CC7.3, CC7.4, CC7.5 |
| **1-3, 7, 10, 12, 15-17** | PCI DSS v4.0 | 12.10.1, 12.10.2, 12.10.3, 12.10.4, 12.10.5, 12.10.6 |
| **13** | GLBA Safeguards | § 314.4(h) |

### 6. Artifact(s)

- Completed Incident Report
- Evidence preservation records
- Forensic investigation reports (if applicable)
- Breach notification records
- Post-incident review documentation
- Updated incident response plan

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Incident** | An event that actually or potentially jeopardizes the confidentiality, integrity, or availability of cardholder data, customer financial information, or company systems. |
| **Incident Response Team (IRT)** | A dedicated or virtual team responsible for responding to security incidents. |
| **CHD** | Cardholder Data - at minimum, the full Primary Account Number (PAN). |
| **SAD** | Sensitive Authentication Data - full track data, card verification codes, and PINs/PIN blocks. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Incident Commander** | Leads and coordinates the overall incident response effort. Makes notification decisions. |
| **Security Analyst** | Performs initial triage, analysis, and technical investigation of incidents. |
| **IT Security Team** | Maintains incident response capabilities and participates in containment and recovery. |
| **PCI Program Manager** | Coordinates payment brand notifications for CHD incidents. Maintains PCI DSS compliance evidence. |
| **Privacy Officer** | Assesses incidents for data breach notification requirements under GLBA and state laws. |
| **BSA/AML Officer** | Assesses incidents for potential SAR filing requirements if fraud or money laundering is suspected. |
| **Legal Counsel** | Provides legal guidance on incident handling, evidence preservation, and external communications. |

