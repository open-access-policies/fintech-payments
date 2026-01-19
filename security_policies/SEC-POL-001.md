# Information Security Policy (SEC-POL-001)

## 1. Objective

This policy establishes **[Company Name]**'s Information Security Management System (ISMS) to achieve and maintain compliance with PCI DSS v4.0, SOC 2, GLBA, and BSA/AML requirements. This policy defines comprehensive security controls to protect the confidentiality, integrity, and availability of cardholder data, customer financial information, and company information assets while supporting business operations in the payments and financial services ecosystem.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, including employees, contractors, and temporary staff. It encompasses:

- All systems that store, process, or transmit cardholder data (the Cardholder Data Environment or CDE)
- All systems processing nonpublic personal information (NPI) as defined under GLBA
- All customer financial information subject to BSA/AML requirements
- All company information assets, systems, and data, whether on-premises, in cloud services, or accessed remotely

This policy also applies to third-party service providers (TPSPs) who access company systems, process payment transactions, or handle customer financial data on behalf of **[Company Name]**.

## 3. Policy

**[Company Name]** is committed to implementing comprehensive information security controls that meet the requirements of PCI DSS v4.0, SOC 2 Trust Services Criteria, GLBA Safeguards Rule, and BSA/AML program requirements.

### 3.1 Security Governance and Management

**[Company Name]** establishes effective security governance aligned with regulatory requirements.

- A **Qualified Individual** is designated with overall responsibility for the information security program as required by GLBA § 314.4(a). This individual may be employed directly, through an affiliate, or via a service provider, though **[Company Name]** retains ultimate compliance responsibility.

- A **[Role Title, e.g., Chief Information Security Officer (CISO)]** is designated with responsibility for day-to-day information security operations, policy development, and security monitoring.

- A **[Role Title, e.g., BSA/AML Compliance Officer]** is designated with responsibility for anti-money laundering compliance, suspicious activity monitoring, and regulatory reporting.

- Security roles and responsibilities are documented and communicated to all workforce members with access to cardholder data or customer financial information.

- The information security policy is reviewed at least annually and updated as needed to reflect changes to business objectives, the regulatory environment, or risks to the CDE and customer information.

### 3.2 Risk Management

**[Company Name]** implements a comprehensive risk management program that satisfies GLBA § 314.4(b) and PCI DSS Requirement 12.3 requirements.

- Written risk assessments are conducted at least annually to identify reasonably foreseeable internal and external risks to the security, confidentiality, and integrity of customer information and cardholder data.

- Risk assessments include:
  - Criteria for evaluating identified risks
  - Assessment of the sufficiency of existing controls to address identified risks
  - Risk treatment plans for high and medium risks
  - Consideration of risks specific to payment processing and financial services

- A targeted risk analysis is performed for each PCI DSS requirement allowing flexibility in how frequently an activity is performed (per PCI DSS 12.3.1).

- The risk register is maintained and updated to track identified risks, control effectiveness, and remediation efforts.

- Risk assessment results are reported to the Board of Directors or equivalent governing body at least annually.

### 3.3 Access Control

Access to company systems and data is controlled through formal processes that implement least privilege principles, with enhanced controls for the cardholder data environment.

- All users have unique user accounts and are authenticated before accessing company systems.

- Multi-factor authentication (MFA) is implemented for:
  - All access to the cardholder data environment (CDE) per PCI DSS 8.4.2
  - All remote access to company systems
  - All administrative access to critical systems

- User access to cardholder data is restricted based on business need-to-know and job responsibilities.

- User access is reviewed quarterly for systems with access to cardholder data or customer financial information, and at least annually for all other systems.

- Privileged access is monitored, logged, and restricted to authorized personnel only.

- Access rights are promptly revoked upon termination or change in job responsibilities.

### 3.4 Cardholder Data Protection

**[Company Name]** protects cardholder data throughout its lifecycle in accordance with PCI DSS requirements.

- Cardholder data storage is minimized and limited to that which is necessary for business, legal, or regulatory purposes.

- Primary Account Numbers (PANs) are rendered unreadable anywhere they are stored using tokenization, encryption, or other approved methods per PCI DSS 3.5.

- Sensitive Authentication Data (SAD) including full track data, CVV2/CVC2, and PINs is never stored after authorization.

- Strong cryptography is used to protect cardholder data during transmission over open, public networks per PCI DSS 4.1.

- Encryption key management procedures are implemented per PCI DSS 3.6 and 3.7.

### 3.5 Customer Financial Information Protection

**[Company Name]** protects nonpublic personal information (NPI) in accordance with GLBA Safeguards Rule requirements.

- Customer financial information is classified and handled according to data classification standards.

- Encryption is implemented for customer information:
  - In transit over external networks
  - At rest in storage systems

- Data retention periods comply with regulatory requirements (minimum **[Number, e.g., 7]** years for financial records) and data is securely disposed of when no longer needed per GLBA § 314.4(c)(6).

- Regular backups are performed and tested to ensure data recoverability.

### 3.6 Security Awareness and Training

All workforce members receive security awareness training appropriate to their roles and access to cardholder data and customer financial information.

- New workforce members complete security awareness training within **[Number, e.g., 30]** days of hire.

- Annual security awareness training is provided to all workforce members, covering:
  - Information security policies and procedures
  - Protection of cardholder data and customer financial information
  - Recognition and reporting of security incidents
  - Social engineering and phishing awareness
  - Acceptable use of company systems

- Role-specific training is provided to personnel with access to the CDE or responsibility for security functions per PCI DSS 12.6.2.

- Training completion is tracked and documented.

### 3.7 Incident Response

**[Company Name]** maintains effective incident response capabilities in accordance with GLBA § 314.4(h) and PCI DSS 12.10 requirements.

- A written incident response plan is established and maintained, addressing:
  - Goals of the incident response plan
  - Internal processes for responding to security events
  - Clear roles, responsibilities, and decision-making authority
  - External and internal communications procedures
  - Identification of requirements for remediation
  - Documentation and reporting procedures
  - Post-incident review and plan revision

- The incident response plan includes procedures for:
  - Security incidents affecting the CDE or customer financial information
  - Suspected or confirmed data breaches
  - Ransomware and malware incidents
  - Third-party security incidents
  - Regulatory notification requirements

- All security incidents are documented and tracked through resolution.

- The incident response plan is tested at least annually.

### 3.8 System Monitoring and Logging

Continuous monitoring is implemented to detect security threats and suspicious activities in accordance with PCI DSS Requirement 10 and GLBA § 314.4(c)(8).

- Security logs are collected from all systems in the CDE and systems processing customer financial information.

- Logging includes:
  - User access to cardholder data
  - Actions taken by individuals with administrative access
  - Access to audit trails
  - Invalid logical access attempts
  - Use of identification and authentication mechanisms
  - Initialization, stopping, or pausing of audit logs
  - Creation and deletion of system-level objects

- Automated monitoring tools provide real-time alerting for security events.

- Log reviews are conducted daily using automated mechanisms per PCI DSS 10.4.1.

- Audit trails are protected from unauthorized modification and retained for at least one year, with a minimum of three months immediately available.

### 3.9 Vendor and Third-Party Management

Third-party service providers (TPSPs) are managed to ensure they meet **[Company Name]**'s security requirements and regulatory obligations per PCI DSS 12.8 and GLBA § 314.4(f).

- Due diligence is performed before engaging TPSPs that will have access to cardholder data or customer financial information.

- Written agreements are established with all TPSPs that:
  - Acknowledge TPSP responsibility for the security of cardholder data they possess
  - Define security requirements and expectations
  - Require notification of security incidents

- PCI DSS compliance status is obtained from TPSPs that store, process, or transmit cardholder data at least annually.

- A list of all TPSPs with access to cardholder data or customer information is maintained.

- TPSP compliance status and security practices are reviewed at least annually.

### 3.10 Change Management

Changes to systems and applications are managed through formal change control processes to maintain the security of the CDE and customer information systems.

- Change requests are documented, reviewed, and approved before implementation.

- Changes are tested to verify they do not introduce security vulnerabilities.

- Change documentation includes description, approval, testing results, and rollback procedures.

- Emergency changes follow documented emergency change procedures and are reviewed post-implementation.

### 3.11 Physical Security

Physical access to facilities and systems containing cardholder data and customer financial information is restricted and monitored per PCI DSS Requirement 9.

- Physical access to the CDE is restricted to authorized personnel.

- Visitor access is controlled, logged, and visitors are escorted in sensitive areas.

- Media containing cardholder data is physically secured and destroyed when no longer needed.

### 3.12 Regulatory Compliance

**[Company Name]** maintains compliance with applicable regulations and standards.

- **PCI DSS v4.0**: Compliance is validated annually through self-assessment questionnaire (SAQ) or Qualified Security Assessor (QSA) assessment as appropriate for **[Company Name]**'s merchant level.

- **SOC 2**: Type II attestation is maintained for Trust Services Criteria relevant to **[Company Name]**'s services.

- **GLBA Safeguards Rule**: The information security program meets all requirements of 16 CFR Part 314.

- **BSA/AML**: Anti-money laundering program requirements are addressed through FIN-POL-001 (AML Policy).

- Compliance gaps are documented and addressed through corrective action plans.

- The Qualified Individual reports to the Board of Directors or equivalent governing body at least annually on the status of the information security program per GLBA § 314.4(i).

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 12.1.1, 12.1.2, 12.4.1 |
| 3.1 | SOC 2 TSC | CC1.1, CC1.2, CC1.3 |
| 3.1 | GLBA Safeguards | § 314.4(a) - Qualified Individual |
| 3.2 | PCI DSS v4.0 | 12.3.1, 12.3.2, 12.3.3 |
| 3.2 | SOC 2 TSC | CC3.1, CC3.2, CC3.3, CC3.4 |
| 3.2 | GLBA Safeguards | § 314.4(b) - Risk Assessment |
| 3.3 | PCI DSS v4.0 | 7.1, 7.2, 8.1, 8.2, 8.3, 8.4 |
| 3.3 | SOC 2 TSC | CC6.1, CC6.2, CC6.3 |
| 3.3 | GLBA Safeguards | § 314.4(c)(1), § 314.4(c)(5) |
| 3.4 | PCI DSS v4.0 | 3.1, 3.2, 3.3, 3.4, 3.5, 3.6, 3.7 |
| 3.4 | SOC 2 TSC | CC6.1, C1.1, C1.2 |
| 3.5 | GLBA Safeguards | § 314.4(c)(3), § 314.4(c)(6) |
| 3.5 | SOC 2 TSC | C1.1, C1.2 |
| 3.6 | PCI DSS v4.0 | 12.6.1, 12.6.2, 12.6.3 |
| 3.6 | SOC 2 TSC | CC1.4, CC2.2 |
| 3.6 | GLBA Safeguards | § 314.4(e) - Personnel |
| 3.7 | PCI DSS v4.0 | 12.10.1, 12.10.2, 12.10.3, 12.10.4 |
| 3.7 | SOC 2 TSC | CC7.4, CC7.5 |
| 3.7 | GLBA Safeguards | § 314.4(h) - Incident Response |
| 3.8 | PCI DSS v4.0 | 10.1, 10.2, 10.3, 10.4, 10.5, 10.6, 10.7 |
| 3.8 | SOC 2 TSC | CC7.2, CC7.3 |
| 3.8 | GLBA Safeguards | § 314.4(c)(8) |
| 3.9 | PCI DSS v4.0 | 12.8.1, 12.8.2, 12.8.3, 12.8.4, 12.8.5 |
| 3.9 | SOC 2 TSC | CC9.2 |
| 3.9 | GLBA Safeguards | § 314.4(f) - Service Providers |
| 3.10 | PCI DSS v4.0 | 6.5.1, 6.5.2, 6.5.3, 6.5.4 |
| 3.10 | SOC 2 TSC | CC8.1 |
| 3.11 | PCI DSS v4.0 | 9.1, 9.2, 9.3, 9.4 |
| 3.11 | SOC 2 TSC | CC6.4, CC6.5 |
| 3.12 | PCI DSS v4.0 | 12.4.1, 12.5.1, 12.5.2 |
| 3.12 | GLBA Safeguards | § 314.4(i) - Board Reporting |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data (CHD)** | At minimum, the full Primary Account Number (PAN). May also include cardholder name, expiration date, and service code. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Customer Information** | Any record containing nonpublic personal information about a customer, whether in paper, electronic, or other form (per GLBA). |
| **Nonpublic Personal Information (NPI)** | Personally identifiable financial information and any list, description, or grouping of consumers derived from such information. |
| **Primary Account Number (PAN)** | Unique payment card number (typically 15-16 digits) that identifies the issuer and cardholder account. |
| **Qualified Individual** | The person designated to oversee and implement the information security program per GLBA § 314.4(a). |
| **Sensitive Authentication Data (SAD)** | Security-related information including full track data, card verification codes (CVV2/CVC2/CAV2), and PINs/PIN blocks used to authenticate cardholders. |
| **Third-Party Service Provider (TPSP)** | An external entity that stores, processes, transmits, or can impact the security of cardholder data or customer information on behalf of **[Company Name]**. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Board of Directors / Executive Leadership** | Provide governance oversight, approve security policies, allocate resources for the information security program, and receive annual reports from the Qualified Individual. |
| **Qualified Individual (per GLBA)** | Oversee and implement the information security program. Report to the Board at least annually on program status and material security matters. |
| **Chief Information Security Officer (CISO)** | Manage day-to-day security operations. Develop and maintain security policies and procedures. Conduct risk assessments and implement controls. Report security metrics and incidents. |
| **BSA/AML Compliance Officer** | Oversee anti-money laundering compliance. Ensure SAR and CTR filing requirements are met. Coordinate with regulators on BSA examinations. |
| **PCI Program Manager** | Manage PCI DSS compliance program. Coordinate annual assessments. Maintain CDE documentation and scope validation. |
| **IT Security Team** | Implement and maintain technical security controls. Monitor systems for security events. Respond to security incidents. Maintain security configurations. |
| **Human Resources** | Integrate security requirements into hiring processes. Manage workforce security training. Coordinate background check procedures. |
| **All Workforce Members** | Comply with security policies and procedures. Complete required security training. Report suspected security incidents. Protect cardholder data and customer information in daily work. |
| **Managers/Supervisors** | Ensure team compliance with security policies. Conduct required access reviews. Report security concerns through appropriate channels. |

