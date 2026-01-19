# Vulnerability Management and Security Testing Policy (SEC-POL-007)

## 1. Objective

This policy establishes requirements for identifying, prioritizing, and addressing security vulnerabilities through regular vulnerability scanning and penetration testing in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that the cardholder data environment (CDE) and systems processing customer financial information are regularly tested to maintain a strong security posture.

## 2. Scope

This policy applies to all **[Company Name]** workforce members responsible for security testing activities. It encompasses:

- All systems within the cardholder data environment (CDE)
- All systems connected to the CDE
- All systems that store, process, or transmit customer financial information
- All external-facing systems and applications
- All wireless access points
- Network segmentation controls

## 3. Policy

**[Company Name]** implements comprehensive vulnerability management and security testing processes that meet PCI DSS, SOC 2, and GLBA requirements.

### 3.1 Vulnerability Identification and Management

Security vulnerabilities are identified and managed per PCI DSS 6.3.1.

**Vulnerability Identification:**
- New security vulnerabilities are identified using industry-recognized sources
- Sources include alerts from international and national CERTs, vendor security advisories, and threat intelligence feeds
- Vulnerabilities in bespoke/custom software and third-party software (operating systems, databases) are covered

**Risk Ranking:**
- Vulnerabilities are assigned risk rankings based on industry best practices and potential impact
- Risk rankings identify all vulnerabilities considered high-risk or critical to the environment
- CVSS scores are used as a baseline, adjusted for environmental factors

**Vulnerability Tracking:**
- All identified vulnerabilities are documented in a vulnerability tracking system
- Tracking includes vulnerability details, affected systems, risk ranking, remediation status, and target dates

### 3.2 Internal Vulnerability Scanning

Internal vulnerability scans are performed per PCI DSS 11.3.1.

**Frequency and Scope:**
- Scans are performed at least once every three months
- All system components in the CDE are scanned
- All systems connected to the CDE are scanned

**Scan Requirements:**
- Scan tool is kept up to date with latest vulnerability information
- Scans are performed by qualified personnel
- Organizational independence of the tester exists

**Remediation:**
- High-risk and critical vulnerabilities (per the risk ranking process) are resolved
- Rescans are performed to confirm all high-risk and critical vulnerabilities have been resolved

**After Significant Changes (per PCI DSS 11.3.1.3):**
- Internal scans are performed after any significant change
- Significant changes include new system component installations, network topology changes, firewall rule modifications, and product upgrades
- Scans occur after the change is completed and per the entity's change management procedures

### 3.3 External Vulnerability Scanning

External vulnerability scans are performed per PCI DSS 11.3.2.

**Frequency and Scope:**
- Scans are performed at least once every three months
- All external-facing IP addresses and domains are scanned

**Scan Requirements:**
- Scans are performed by a PCI SSC Approved Scanning Vendor (ASV)
- Vulnerabilities are resolved and ASV Program Guide requirements for a passing scan are met
- Rescans are performed as needed to confirm vulnerabilities are resolved

**After Significant Changes (per PCI DSS 11.3.2.1):**
- External scans are performed after any significant change
- Scans are performed per the ASV Program Guide

### 3.4 Penetration Testing Methodology

A penetration testing methodology is defined, documented, and implemented per PCI DSS 11.4.1.

**Methodology Requirements:**
- Based on industry-accepted penetration testing approaches (e.g., PTES, OWASP, NIST SP 800-115)
- Coverage for the entire CDE perimeter and critical systems
- Testing from both inside and outside the network
- Testing to validate segmentation and scope-reduction controls
- Application-layer testing to identify vulnerabilities listed in PCI DSS 6.2.4
- Network-layer tests encompassing all components supporting network functions and operating systems
- Review and consideration of threats and vulnerabilities experienced in the last 12 months

**Documentation:**
- Documented approach to assessing and addressing risk posed by exploitable vulnerabilities
- Retention of penetration testing results and remediation activities for at least 12 months

### 3.5 Internal Penetration Testing

Internal penetration testing is performed per PCI DSS 11.4.2.

**Frequency:**
- At least once every 12 months
- After any significant infrastructure or application upgrade or change

**Requirements:**
- Performed per the entity's defined methodology
- Performed by a qualified internal resource or qualified external third party
- Organizational independence of the tester exists (not required to be a QSA or ASV)

### 3.6 External Penetration Testing

External penetration testing is performed per PCI DSS 11.4.3.

**Frequency:**
- At least once every 12 months
- After any significant infrastructure or application upgrade or change

**Requirements:**
- Performed per the entity's defined methodology
- Performed by a qualified internal resource or qualified external third party
- Organizational independence of the tester exists (not required to be a QSA or ASV)

### 3.7 Penetration Test Remediation

Exploitable vulnerabilities and security weaknesses found during penetration testing are corrected per PCI DSS 11.4.4.

- Vulnerabilities are addressed in accordance with the entity's risk assessment process (per PCI DSS 6.3.1)
- Penetration testing is repeated to verify corrections
- Critical and high-risk findings are remediated with priority

### 3.8 Segmentation Testing

If segmentation is used to isolate the CDE from other networks, penetration tests validate segmentation controls per PCI DSS 11.4.5.

**Frequency:**
- At least once every 12 months
- After any changes to segmentation controls/methods
- For service providers: at least once every six months per PCI DSS 11.4.6

**Testing Requirements:**
- Covers all segmentation controls/methods in use
- Confirms segmentation controls are operational and effective
- Confirms the CDE is isolated from all out-of-scope systems
- Confirms effectiveness of isolation between systems with differing security levels
- Performed by a qualified internal resource or qualified external third party
- Organizational independence of the tester exists

### 3.9 Wireless Access Point Monitoring

Authorized and unauthorized wireless access points are identified and monitored per PCI DSS 11.2.1.

**Testing Requirements:**
- The presence of wireless (Wi-Fi) access points is tested for
- All authorized and unauthorized wireless access points are detected and identified
- Testing occurs at least once every three months
- If automated monitoring is used, personnel are notified via generated alerts

**Wireless Inventory (per PCI DSS 11.2.2):**
- An inventory of authorized wireless access points is maintained
- A documented business justification exists for all authorized wireless access points

**Unauthorized Access Points:**
- Unauthorized wireless access points are addressed according to incident response procedures
- Detection of unauthorized access points triggers security incident evaluation

### 3.10 Intrusion Detection and Prevention

Intrusion-detection and/or intrusion-prevention techniques are used per PCI DSS 11.5.1.

**Monitoring Requirements:**
- All traffic is monitored at the perimeter of the CDE
- All traffic is monitored at critical points in the CDE
- Personnel are alerted to suspected compromises
- All intrusion-detection and prevention engines, baselines, and signatures are kept up to date

### 3.11 File Integrity Monitoring

A change-detection mechanism is deployed per PCI DSS 11.5.2.

**Configuration:**
- Alerts personnel to unauthorized modification (including changes, additions, and deletions) of critical files
- Performs critical file comparisons at least once weekly
- Critical files include system executables, application executables, configuration files, and audit logs

**Response:**
- Alerts are investigated according to incident response procedures
- Unauthorized changes trigger security incident evaluation

### 3.12 Payment Page Tamper Detection

A change- and tamper-detection mechanism is deployed for payment pages per PCI DSS 11.6.1.

**Configuration:**
- Alerts personnel to unauthorized modification of HTTP headers and payment page contents as received by the consumer browser
- Mechanism evaluates the received HTTP header and payment page
- Functions are performed at least once every seven days (or at the frequency defined in the targeted risk analysis per PCI DSS 12.3.1)

**Indicators:**
- Detection includes indicators of compromise, changes, additions, and deletions
- Known skimming signatures and script behaviors are monitored

### 3.13 GLBA Testing Requirements

Testing is performed to verify the effectiveness of safeguards per GLBA § 314.4(d).

**Testing Requirements:**
- Key controls, systems, and procedures are regularly tested or monitored
- Penetration testing is performed at least annually per GLBA § 314.4(d)(2)
- Vulnerability assessments are performed at least semi-annually per GLBA § 314.4(d)(2)
- Systematic scans or reviews monitor systems for attacks, intrusions, or unauthorized data access

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 6.3.1 |
| 3.1 | SOC 2 TSC | CC7.1 |
| 3.2 | PCI DSS v4.0 | 11.3.1, 11.3.1.3 |
| 3.2 | GLBA Safeguards | § 314.4(d)(2) |
| 3.3 | PCI DSS v4.0 | 11.3.2, 11.3.2.1 |
| 3.4 | PCI DSS v4.0 | 11.4.1 |
| 3.5 | PCI DSS v4.0 | 11.4.2 |
| 3.5 | GLBA Safeguards | § 314.4(d)(2) |
| 3.6 | PCI DSS v4.0 | 11.4.3 |
| 3.7 | PCI DSS v4.0 | 11.4.4 |
| 3.8 | PCI DSS v4.0 | 11.4.5, 11.4.6 |
| 3.9 | PCI DSS v4.0 | 11.2.1, 11.2.2 |
| 3.10 | PCI DSS v4.0 | 11.5.1 |
| 3.10 | SOC 2 TSC | CC7.2 |
| 3.11 | PCI DSS v4.0 | 11.5.2 |
| 3.12 | PCI DSS v4.0 | 11.6.1 |
| 3.13 | GLBA Safeguards | § 314.4(d)(1), § 314.4(d)(2) |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Approved Scanning Vendor (ASV)** | A company approved by the PCI SSC to conduct external vulnerability scanning services. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **CVSS (Common Vulnerability Scoring System)** | A framework for rating the severity of security vulnerabilities. |
| **File Integrity Monitoring (FIM)** | Tools that check for changes, additions, and deletions to critical files and notify when such changes are detected. |
| **Intrusion Detection System (IDS)** | A system that monitors network traffic for suspicious activity and issues alerts when such activity is discovered. |
| **Intrusion Prevention System (IPS)** | A system that monitors network traffic and takes automated action to block or prevent detected intrusions. |
| **Penetration Testing** | An authorized simulated cyberattack to evaluate the security of a system by attempting to exploit vulnerabilities. |
| **Segmentation** | Network security technique that divides a network into multiple segments to isolate the CDE from other networks. |
| **Vulnerability Scan** | An automated test using tools designed to expose potential vulnerabilities in applications, operating systems, and network devices. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own vulnerability management policy. Approve penetration testing methodology. Review vulnerability remediation status. Ensure compliance with PCI DSS, SOC 2, and GLBA testing requirements. |
| **IT Security Team** | Conduct internal vulnerability scans. Coordinate external vulnerability scans with ASV. Manage vulnerability tracking system. Implement and monitor IDS/IPS and FIM. Respond to security alerts. |
| **PCI Program Manager** | Coordinate penetration testing schedule. Maintain penetration testing documentation. Ensure segmentation testing is completed. Track remediation of PCI-related findings. |
| **Network Operations** | Remediate network-related vulnerabilities. Maintain wireless access point inventory. Implement segmentation controls. Configure IDS/IPS systems. |
| **System Administrators** | Remediate system vulnerabilities. Apply security patches. Maintain FIM configurations. Address unauthorized changes. |
| **Application Development** | Remediate application vulnerabilities. Support application penetration testing. Address findings from code reviews and security scans. |

