# Logging and Monitoring Policy (OP-POL-005)

## 1. Objective

This policy establishes requirements for logging and monitoring all access to system components and cardholder data in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that security events are captured, audit logs are protected, and anomalies are detected and addressed to prevent, detect, and minimize the impact of data compromises.

## 2. Scope

This policy applies to all **[Company Name]** workforce members responsible for implementing, maintaining, and reviewing system logging and monitoring. It encompasses:

- All systems within the cardholder data environment (CDE)
- All systems connected to the CDE
- All critical system components
- All systems that store, process, or transmit customer financial information
- All servers and components performing security functions

## 3. Policy

**[Company Name]** implements comprehensive logging and monitoring processes that meet PCI DSS, SOC 2, and GLBA requirements.

### 3.1 Audit Log Implementation

Audit logs are enabled and active for all system components and cardholder data per PCI DSS 10.2.1.

**Logging Coverage:**
- All system components in the CDE have audit logging enabled
- All systems processing or storing customer financial information have audit logging enabled
- All critical system components have audit logging enabled
- All security systems (firewalls, IDS/IPS, authentication servers) have audit logging enabled

### 3.2 Auditable Events

Audit logs capture specific events for security analysis per PCI DSS 10.2.1.1 through 10.2.1.7.

**Required Log Events:**
- All individual user access to cardholder data
- All actions taken by any individual with administrative access
- Access to all audit trails
- Invalid logical access attempts
- Use of and changes to identification and authentication mechanisms (including creation of new accounts and elevation of privileges)
- Initialization, stopping, or pausing of the audit logs
- Creation and deletion of system-level objects

### 3.3 Audit Log Content

Audit logs record required details for each auditable event per PCI DSS 10.2.2.

**Required Log Entry Elements:**
- User identification
- Type of event
- Date and time
- Success and failure indication
- Origination of event
- Identity or name of affected data, system component, resource, or service

### 3.4 Audit Log Protection

Audit logs are protected from destruction and unauthorized modifications per PCI DSS 10.3.

**Access Control (per PCI DSS 10.3.1):**
- Read access to audit log files is limited to those with a job-related need
- Access controls prevent unauthorized viewing of log data

**Modification Prevention (per PCI DSS 10.3.2):**
- Audit log files are protected to prevent modifications by individuals
- Access control mechanisms, physical segregation, and/or network segregation are used

**Centralized Log Management (per PCI DSS 10.3.3):**
- Audit log files are promptly backed up to a secure, central, internal log server(s)
- External-facing technology logs are included
- Central log storage is difficult to modify

**File Integrity Monitoring (per PCI DSS 10.3.4):**
- File integrity monitoring or change-detection mechanisms are used on audit logs
- Alerts are generated when existing log data is changed
- New log data being added does not generate alerts

### 3.5 Audit Log Review

Audit logs are reviewed to identify anomalies or suspicious activity per PCI DSS 10.4.

**Daily Review (per PCI DSS 10.4.1):**
The following logs are reviewed at least once daily:
- All security events
- Logs of all system components that store, process, or transmit CHD and/or SAD
- Logs of all critical system components
- Logs of all servers and system components that perform security functions

**Periodic Review (per PCI DSS 10.4.2):**
- Logs of all other system components (not specified above) are reviewed periodically
- Review frequency is based on risk assessment

**Automated Tools:**
- Log harvesting, parsing, and alerting tools are implemented
- Security Information and Event Management (SIEM) solutions are used for centralized log management and analysis
- Automated alerts are configured for security events and anomalies

**Exception Handling (per PCI DSS 10.4.3):**
- Exceptions and anomalies identified during the review process are addressed
- Processes define how to rank and prioritize exceptions
- Procedures specify reporting and escalation requirements
- Responsibilities for investigation and remediation are documented

### 3.6 Audit Log Retention

Audit log history is retained and available for analysis per PCI DSS 10.5.1.

**Retention Requirements:**
- Audit log history is retained for at least 12 months
- At least the most recent three months are immediately available for analysis
- Older logs are available for restoration within a reasonable timeframe

**Storage Methods:**
- Online storage for recent logs (minimum three months)
- Archive storage for historical logs (months 4-12)
- Backup verification ensures logs can be restored when needed

### 3.7 Time Synchronization

Time-synchronization mechanisms support consistent time settings across all systems per PCI DSS 10.6.

**Time Server Configuration (per PCI DSS 10.6.1 and 10.6.2):**
- System clocks and time are synchronized using time-synchronization technology (e.g., NTP)
- One or more designated time servers are in use
- Only designated central time server(s) receive time from external sources
- Time received from external sources is based on International Atomic Time or UTC
- Designated time server(s) accept time updates only from specific industry-accepted external sources
- Where multiple time servers exist, they peer with one another
- Internal systems receive time information only from designated central time server(s)

**Time Data Protection (per PCI DSS 10.6.3):**
- Access to time data is restricted to only personnel with a business need
- Any changes to time settings on critical systems are logged, monitored, and reviewed

### 3.8 Security Control Failure Detection

Failures of critical security control systems are detected, reported, and responded to promptly per PCI DSS 10.7.

**Monitored Systems (per PCI DSS 10.7.2):**
- Network security controls
- IDS/IPS
- Change-detection mechanisms
- Anti-malware solutions
- Physical access controls
- Logical access controls
- Audit logging mechanisms
- Segmentation controls (if used)
- Audit log review mechanisms
- Automated security testing tools (if used)

**Detection and Alerting:**
- Failures are detected automatically where possible
- Alerts are generated when critical security controls fail
- Personnel are notified promptly of control failures

**Response to Failures (per PCI DSS 10.7.3):**
- Security functions are restored promptly
- Duration of security failure is documented (start and end date/time)
- Cause(s) of failure are identified and documented
- Required remediation is documented
- Security issues that arose during the failure are identified and addressed
- Determination is made whether further actions are required
- Controls are implemented to prevent the cause of failure from reoccurring
- Monitoring of security controls is resumed

### 3.9 GLBA Monitoring Requirements

Activity monitoring and logging is implemented per GLBA § 314.4(c)(8).

**Monitoring Requirements:**
- Policies, procedures, and controls monitor and log the activity of authorized users
- Systems detect unauthorized access, use, or tampering with customer information
- Continuous monitoring or periodic testing verifies the effectiveness of key controls per GLBA § 314.4(d)

### 3.10 Payment Page Monitoring

For public-facing payment pages, change and tamper detection is implemented to detect unauthorized modifications per PCI DSS 11.6.1.

**Monitoring Scope:**
- HTTP headers received by consumer browsers
- Payment page contents received by consumer browsers
- Indicators of compromise, changes, additions, and deletions

**Monitoring Frequency:**
- At least once every seven days
- Or at the frequency defined in the targeted risk analysis per PCI DSS 12.3.1

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 10.2.1 |
| 3.1 | SOC 2 TSC | CC7.2 |
| 3.2 | PCI DSS v4.0 | 10.2.1.1-10.2.1.7 |
| 3.3 | PCI DSS v4.0 | 10.2.2 |
| 3.4 | PCI DSS v4.0 | 10.3.1, 10.3.2, 10.3.3, 10.3.4 |
| 3.4 | SOC 2 TSC | CC7.2 |
| 3.5 | PCI DSS v4.0 | 10.4.1, 10.4.2, 10.4.3 |
| 3.5 | SOC 2 TSC | CC7.2, CC7.3 |
| 3.5 | GLBA Safeguards | § 314.4(c)(8) |
| 3.6 | PCI DSS v4.0 | 10.5.1 |
| 3.7 | PCI DSS v4.0 | 10.6.1, 10.6.2, 10.6.3 |
| 3.8 | PCI DSS v4.0 | 10.7.2, 10.7.3 |
| 3.8 | SOC 2 TSC | CC7.4 |
| 3.9 | GLBA Safeguards | § 314.4(c)(8), § 314.4(d) |
| 3.10 | PCI DSS v4.0 | 11.6.1 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Audit Log** | A chronological record of system activities that provides documentary evidence of the sequence of actions. |
| **Audit Trail** | The record showing who has accessed a system and what operations they have performed during a given period. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Critical System Component** | Any system component whose failure could significantly impact the security of the CDE or processing of transactions. |
| **File Integrity Monitoring (FIM)** | Tools that check for changes, additions, and deletions to critical files and notify when such changes are detected. |
| **Network Time Protocol (NTP)** | A networking protocol for clock synchronization between computer systems. |
| **Security Information and Event Management (SIEM)** | A solution that combines security information management and security event management to provide real-time analysis of security alerts. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own logging and monitoring policy. Ensure compliance with PCI DSS, SOC 2, and GLBA requirements. Review security control failure reports. |
| **IT Security Team** | Implement and maintain logging infrastructure. Configure SIEM and alerting. Conduct daily log reviews. Investigate security events and anomalies. Respond to security control failures. |
| **System Administrators** | Enable and configure audit logging on systems. Maintain time synchronization. Ensure log data is transmitted to central log management. |
| **PCI Program Manager** | Ensure logging meets PCI DSS requirements. Verify log retention compliance. Coordinate with QSA on logging-related assessment activities. |
| **SOC/Monitoring Team** | Monitor security dashboards and alerts. Escalate security events per defined procedures. Document and track security incidents. |

