# Incident Response Policy (RES-POL-001)

## 1. Objective

This policy establishes a comprehensive incident response framework for **[Company Name]** to effectively detect, respond to, contain, and recover from information security incidents in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. The policy ensures that security incidents affecting the cardholder data environment (CDE) and customer financial information are handled in a coordinated, timely, and effective manner to minimize impact, protect sensitive data, maintain regulatory compliance, and preserve evidence.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, contractors, third parties, and business associates who may detect, report, or respond to information security incidents. It encompasses:

- All systems within the cardholder data environment (CDE)
- All systems that store, process, or transmit customer financial information
- All information systems, applications, networks, devices, and data owned, operated, or managed by **[Company Name]**
- Cloud services, mobile devices, and third-party systems

This policy covers all types of security incidents including data breaches, malware infections, unauthorized access, denial of service attacks, payment fraud incidents, suspicious activity warranting SAR filing, and physical security breaches.

## 3. Policy

**[Company Name]** maintains a formal incident response capability that enables rapid detection, assessment, containment, eradication, and recovery from security incidents per PCI DSS 12.10 and GLBA § 314.4(h).

### 3.1 Incident Response Plan

**[Company Name]** maintains a written incident response plan that is ready to be activated in the event of a suspected or confirmed security incident per PCI DSS 12.10.1 and GLBA § 314.4(h).

**Plan Elements:**
- Goals of the incident response plan
- Internal processes for responding to security events
- Clear roles, responsibilities, and levels of decision-making authority
- External and internal communications and information sharing
- Identification of requirements for the remediation of any identified weaknesses
- Documentation and reporting regarding security events and related incident response activities
- Post-incident review and revision of the incident response plan

**Additional PCI DSS Requirements (per PCI DSS 12.10.1):**
- Roles, responsibilities, and communication and contact strategies in the event of a suspected or confirmed security incident, including notification of payment brands and acquirers
- Incident response procedures with specific containment and mitigation activities for different types of incidents
- Business recovery and continuity procedures
- Data backup processes
- Analysis of legal requirements for reporting compromises
- Coverage and responses of all critical system components
- Reference or inclusion of incident response procedures from the payment brands

### 3.2 Incident Response Team

Specific personnel are designated to be available on a 24/7 basis to respond to suspected or confirmed security incidents per PCI DSS 12.10.3.

**Core Team Members:**

| **Role** | **Primary Responsibility** |
|---|---|
| **Incident Commander** | Overall incident response coordination and decision-making authority. Communication with executive leadership and external stakeholders. |
| **Security Analyst** | Technical investigation and analysis. Evidence collection and preservation. Threat intelligence and malware analysis. |
| **System Administrator** | System containment and isolation procedures. System restoration and recovery. Network security controls implementation. |
| **PCI Program Manager** | Coordination of CDE-related incidents. Payment brand notification. PCI DSS compliance verification post-incident. |
| **BSA/AML Compliance Officer** | SAR determination and filing. FinCEN coordination. Regulatory reporting for AML-related incidents. |
| **Legal Counsel** | Legal implications assessment. Law enforcement coordination. Regulatory notification compliance. Litigation hold requirements. |
| **Communications Lead** | Internal and external communication coordination. Customer and stakeholder notification. Media relations. |

**24/7 Availability:**
- On-call rotation schedule is maintained for incident response team members
- Contact information is current and accessible to all team members
- Escalation procedures are defined for after-hours incidents

### 3.3 Incident Classification

All incidents are classified based on severity, potential impact, and regulatory implications.

**Critical (P1) - Response within 15 minutes:**
- Confirmed data breach involving cardholder data or customer financial information
- Active compromise of CDE systems
- Widespread malware infection or ransomware attack affecting CDE
- Unauthorized access to payment processing systems
- Physical security breach affecting CDE or data centers
- Incidents requiring immediate payment brand notification

**High (P2) - Response within 1 hour:**
- Suspected unauthorized access to cardholder data or customer information
- Malware infection on systems connected to the CDE
- Denial of service attacks affecting payment processing
- Suspected insider threat activity involving sensitive data
- Third-party security incident affecting shared cardholder data

**Medium (P3) - Response within 4 hours:**
- Unsuccessful attack attempts against CDE systems
- Malware infection on non-CDE systems
- Policy violations with potential security impact
- Suspicious network activity or anomalous behavior
- Detected vulnerabilities requiring urgent remediation

**Low (P4) - Response within 24 hours:**
- Security policy violations without immediate risk
- Failed login attempts within normal thresholds
- Spam or phishing emails reported by users
- Minor physical security issues

### 3.4 Incident Detection and Monitoring

The incident response plan includes monitoring and responding to alerts from security monitoring systems per PCI DSS 12.10.5.

**Covered Security Monitoring Systems:**
- Intrusion detection and intrusion prevention systems
- Network security controls
- Change detection mechanisms for critical files (file integrity monitoring)
- Change and tamper detection mechanisms for payment pages
- Detection of unauthorized wireless access points

**Detection Methods:**
- Security Information and Event Management (SIEM) alerts
- Anti-malware and endpoint detection and response (EDR) notifications
- Network anomaly detection and behavioral analysis
- Log monitoring and correlation
- Workforce member reports of suspicious activity
- Third-party service provider notifications
- Customer reports of potential compromise

### 3.5 Incident Response Procedures

Standardized procedures are followed for responding to different types of security incidents.

**Detection and Analysis:**
- Continuous monitoring to detect security events
- Initial triage to determine if a potential incident has occurred
- Formal incident declaration and activation of the incident response team
- Impact and severity assessment to classify the incident
- Evidence collection and chain of custody documentation

**Containment, Eradication, and Recovery:**
- Execution of containment strategies to prevent incident spread
- Identification of root cause and all affected systems
- Eradication of the threat (removing malware, disabling accounts, patching vulnerabilities)
- Systematic recovery of affected systems from trusted sources
- Validation that systems are clean before returning to production

**Post-Incident Activity:**
- Incident documentation and reporting
- Lessons learned analysis and improvement recommendations
- Incident response plan updates based on lessons learned per PCI DSS 12.10.6
- Stakeholder communication and follow-up

### 3.6 CDE-Specific Incident Procedures

Incidents affecting the cardholder data environment require additional procedures per PCI DSS 12.10.7.

**Detection of Stored PAN Outside CDE:**
When stored PAN is detected anywhere it is not expected, incident response procedures include:
- Determining what to do if PAN is discovered outside the CDE, including retrieval, secure deletion, and/or migration into the CDE
- Identifying whether sensitive authentication data is stored with PAN
- Determining where the account data came from and how it ended up where it was not expected
- Remediating data leaks or process gaps that resulted in the account data being where it was not expected

**Payment Brand Notification:**
- Acquirer and payment brand contacts are maintained and current
- Notification procedures from payment brands are referenced in the incident response plan
- Notification occurs per payment brand requirements (typically within 24-72 hours of confirmed breach)

### 3.7 Regulatory Notification Requirements

Incident response procedures ensure compliance with applicable legal and regulatory notification requirements.

**FTC Breach Notification (per GLBA § 314.4(j)):**
For notification events affecting information of at least 500 consumers, **[Company Name]** notifies the FTC as soon as possible and no later than 30 days after discovery. Notification includes:
- Name and contact information of the reporting financial institution
- Description of the types of information involved
- Date or date range of the notification event (if determinable)
- Number of consumers affected or potentially affected
- Description of the notification event, including how the information was acquired
- Whether any law enforcement official has provided written determination that notification would impede a criminal investigation

**State Breach Notification:**
- State-specific notification requirements are assessed for each incident
- Notification timelines and requirements vary by state
- Legal counsel coordinates state-level notifications

**Payment Brand Notification:**
- Acquirers and payment brands are notified per their specific requirements
- Card network incident response procedures are followed

**SAR Filing Consideration:**
- Incidents involving suspected fraud, money laundering, or other suspicious activity are evaluated for SAR filing
- The BSA/AML Compliance Officer determines SAR filing requirements per FIN-POL-001

### 3.8 Communication and Coordination

Effective communication is maintained throughout the incident response process.

**Internal Communications:**
- Immediate notification to executive leadership for Critical incidents
- Regular status updates throughout incident response
- Final incident report with lessons learned and recommendations
- Need-to-know basis for incident details

**External Communications:**
- Timely notification of customers potentially affected by incidents
- Coordination with third-party service providers for response activities
- Notification of payment processors, acquirers, and payment brands
- Coordination with insurance carriers and coverage providers

### 3.9 Training and Testing

Personnel responsible for responding to incidents are trained, and the plan is tested per PCI DSS 12.10.2 and 12.10.4.

**Training:**
- Personnel responsible for responding to suspected and confirmed security incidents are appropriately and periodically trained on their incident response responsibilities per PCI DSS 12.10.4
- Training includes handling of evidence, regulatory notification requirements, and payment brand procedures

**Testing:**
- The incident response plan is reviewed and tested at least once every 12 months per PCI DSS 12.10.2
- Testing includes all elements in the incident response plan per PCI DSS 12.10.1
- Testing methods include tabletop exercises, simulated incidents, and walkthrough reviews
- Testing results are documented and used to improve the plan

### 3.10 Post-Incident Activities

Comprehensive post-incident activities ensure organizational learning and improvement.

**Incident Documentation:**
- Complete timeline of incident detection, response, and recovery
- Root cause analysis and contributing factors
- Impact assessment including affected systems and data
- Response effectiveness evaluation and lessons learned
- Recommendations for security improvements

**Lessons Learned (per PCI DSS 12.10.6):**
- The incident response plan is modified and evolved according to lessons learned
- Industry developments are incorporated into the plan
- Formal review meeting within **[Number, e.g., 14]** days of incident closure
- Additional security controls implemented to prevent similar incidents

### 3.11 Evidence Preservation

Evidence is preserved for potential legal proceedings and regulatory investigations.

- Preserve all relevant evidence in its original state
- Maintain proper chain of custody documentation
- Create forensic images of affected systems when appropriate
- Secure physical evidence and access logs
- Document all actions taken and decisions made
- Retain incident records per regulatory requirements and legal hold requirements

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 12.10.1 |
| 3.1 | SOC 2 TSC | CC7.4, CC7.5 |
| 3.1 | GLBA Safeguards | § 314.4(h) |
| 3.2 | PCI DSS v4.0 | 12.10.3 |
| 3.3 | PCI DSS v4.0 | 12.10.1 |
| 3.3 | SOC 2 TSC | CC7.4 |
| 3.4 | PCI DSS v4.0 | 12.10.5 |
| 3.4 | SOC 2 TSC | CC7.2 |
| 3.5 | PCI DSS v4.0 | 12.10.1 |
| 3.5 | SOC 2 TSC | CC7.4, CC7.5 |
| 3.6 | PCI DSS v4.0 | 12.10.1, 12.10.7 |
| 3.7 | GLBA Safeguards | § 314.4(j) |
| 3.7 | PCI DSS v4.0 | 12.10.1 |
| 3.8 | PCI DSS v4.0 | 12.10.1 |
| 3.8 | SOC 2 TSC | CC2.3 |
| 3.9 | PCI DSS v4.0 | 12.10.2, 12.10.4 |
| 3.10 | PCI DSS v4.0 | 12.10.6 |
| 3.10 | SOC 2 TSC | CC7.5 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Chain of Custody** | Documentation of the chronological transfer of evidence from collection to presentation. |
| **Customer Information** | Any record containing nonpublic personal information about a customer, whether in paper, electronic, or other form (per GLBA). |
| **Incident Commander** | Individual with overall authority and responsibility for incident response coordination. |
| **Incident Response Team (IRT)** | Designated group of individuals responsible for detecting, responding to, and recovering from security incidents. |
| **Indicators of Compromise (IOCs)** | Artifacts observed on networks or operating systems that indicate computer intrusion. |
| **Notification Event** | Unauthorized acquisition of unencrypted customer information (per GLBA). |
| **Security Incident** | Any event that could result in unauthorized access to, disclosure, modification, or destruction of cardholder data or customer financial information. |
| **Suspicious Activity Report (SAR)** | A report filed with FinCEN when a financial institution suspects potential money laundering or other financial crimes. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own the incident response program. Lead incident response activities. Ensure regulatory compliance. Approve major response decisions. Report to executive leadership. |
| **Incident Response Team** | Execute incident response procedures. Provide 24/7 availability. Participate in training and testing. Document incident activities. |
| **PCI Program Manager** | Coordinate CDE-related incidents. Manage payment brand notifications. Verify PCI DSS compliance post-incident. Maintain payment brand contact information. |
| **BSA/AML Compliance Officer** | Determine SAR filing requirements. Coordinate FinCEN notifications. Evaluate incidents for AML implications. |
| **Legal Counsel** | Provide legal guidance. Coordinate law enforcement relations. Manage litigation holds. Ensure regulatory notification compliance. Assess state breach notification requirements. |
| **IT Security Team** | Detect and analyze security incidents. Perform technical investigations. Implement containment measures. Conduct system recovery. Preserve evidence. |
| **All Workforce Members** | Report suspected incidents promptly. Cooperate with investigations. Follow incident response procedures. Participate in training. |

