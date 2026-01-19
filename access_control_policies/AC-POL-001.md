# Access Control Policy (AC-POL-001)

## 1. Objective

This policy defines requirements for managing access to **[Company Name]**'s information systems and data in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures access is granted using least privilege and need-to-know principles, with enhanced controls for the cardholder data environment (CDE) and systems processing customer financial information.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, contractors, and third-party service providers who require access to company information systems or data. This includes:

- All systems within the cardholder data environment (CDE)
- Systems that store, process, or transmit nonpublic personal information (NPI) under GLBA
- Applications, servers, databases, network devices, and cloud services
- Physical facilities where company information is accessed or stored

## 3. Policy

Access to all **[Company Name]** information systems and data shall be managed through documented processes that implement least privilege and need-to-know principles, with enhanced requirements for the CDE and customer financial information.

### 3.1 Least Privilege and Need-to-Know Principles

All access rights shall be granted based on least privilege and business need-to-know.

- Workforce members shall receive only the minimum access necessary to perform their job responsibilities.

- Access to system components and cardholder data is based on users' job classification and function per PCI DSS 7.2.1.

- An access control model is defined and documented that includes appropriate access depending on business and access needs.

- Access control systems are configured to "deny all" by default per PCI DSS 7.3.3.

### 3.2 Access to the Cardholder Data Environment (CDE)

Access to the CDE requires additional controls due to the sensitivity of cardholder data.

- Access to cardholder data is restricted to personnel whose job requires such access.

- User access to query repositories of stored cardholder data is restricted per PCI DSS 7.2.6:
  - Via applications or programmatic methods with access based on user roles and least privileges
  - Only responsible database administrators can directly access or query CHD repositories

- All access to the CDE requires multi-factor authentication (MFA) per PCI DSS 8.4.2.

- Access rights to the CDE are documented with business justification.

### 3.3 Access to Customer Financial Information

Access to nonpublic personal information (NPI) and customer financial information is controlled in accordance with GLBA Safeguards Rule requirements.

- Access to customer information is limited to authorized workforce members with a legitimate business need.

- Access controls ensure only authorized individuals can access customer records containing NPI.

- Physical and electronic access to customer information is restricted and monitored.

### 3.4 User Access Lifecycle Management

Access rights shall be managed throughout the user's employment lifecycle per PCI DSS 8.2.4.

- **Provisioning:** Access for new workforce members shall be requested by their manager through the IT service request process. Access shall be based on job role and documented responsibilities with appropriate approval per PCI DSS 7.2.3.

- **Modification:** When workforce members change roles, their manager shall request access modifications. Previous access no longer needed shall be revoked promptly.

- **Deprovisioning:** Access for terminated users is immediately revoked per PCI DSS 8.2.5. Upon termination, all system and facility access shall be revoked within **[Number, e.g., 24]** hours. For involuntary terminations, access shall be revoked immediately.

- **Inactive Accounts:** Inactive user accounts are removed or disabled within 90 days of inactivity per PCI DSS 8.2.6.

### 3.5 Access Reviews

Regular access reviews shall be conducted to ensure access rights remain appropriate per PCI DSS 7.2.4.

- All user accounts and related access privileges, including third-party/vendor accounts, are reviewed at least every six months for systems in the CDE or processing customer financial information.

- Reviews verify that user accounts and access remain appropriate based on job function.

- Any inappropriate access identified during reviews is addressed promptly.

- Management acknowledges that access remains appropriate.

- Accounts with privileged or administrative access shall be reviewed quarterly by system owners or managers.

- Review results and any access modifications shall be documented.

- Failure to complete reviews within **[Number, e.g., 14]** days shall result in escalation to the **[Role Title, e.g., CISO or Security Manager]**.

### 3.6 Privileged Access Management

Administrative accounts require additional controls due to their elevated risk.

- Administrative access shall be granted on a limited, as-needed basis with documented business justification per PCI DSS 7.2.2.

- Workforce members with administrative privileges shall use separate accounts for administrative tasks and standard accounts for daily activities.

- Multi-factor authentication (MFA) is mandatory for all administrative accounts.

- Administrative activities shall be logged and monitored per PCI DSS 10.2.

- Privileged Access Management (PAM) solutions are recommended for granting temporary elevated access.

### 3.7 Unique User Identification

All users are assigned unique identification for accountability and traceability per PCI DSS 8.2.1.

- Every user shall have a unique user ID. Shared accounts are prohibited except as specified in Section 3.8.

- Access to system components or cardholder data is allowed only after assignment of a unique ID.

- All actions taken can be traced to known and authorized users.

### 3.8 Shared and Group Accounts

Group, shared, or generic accounts are only used when necessary on an exception basis per PCI DSS 8.2.2.

- Account use is prevented unless needed for an exceptional circumstance.

- Use is limited to the time needed for the exceptional circumstance.

- Business justification for use is documented.

- Use is explicitly approved by management.

- Individual user identity is confirmed before access to an account is granted.

- Every action taken is attributable to an individual user.

### 3.9 Password and Authentication Requirements

All systems and applications must be configured to enforce comprehensive authentication requirements aligned with PCI DSS Requirement 8.

- **Password Complexity:** Per PCI DSS 8.3.6, passwords must meet:
  - Minimum length of twelve (12) characters (or eight characters if the system does not support 12)
  - Contain both numeric and alphabetic characters
  - For administrative accounts: Minimum sixteen (16) characters with additional complexity

- **Password History:** Individuals are not allowed to submit a new password that is the same as any of the last four passwords used per PCI DSS 8.3.7.

- **Password Age:** If passwords are used as the only authentication factor for user access, passwords are changed at least every 90 days, OR dynamic security posture analysis is implemented per PCI DSS 8.3.9.

- **First-Time and Reset Passwords:** Passwords are set to a unique value for first-time use and upon reset, and forced to be changed immediately after first use per PCI DSS 8.3.5.

- **Account Lockout:** User accounts are automatically locked after not more than 10 invalid logon attempts per PCI DSS 8.3.4. Lockout duration is a minimum of 30 minutes or until the user's identity is confirmed.

- **Authentication Factor Protection:** Strong cryptography is used to render all authentication factors unreadable during transmission and storage per PCI DSS 8.3.2.

- **Identity Verification:** User identity is verified before modifying any authentication factor per PCI DSS 8.3.3.

### 3.10 Multi-Factor Authentication (MFA)

MFA is required to secure access to the CDE and sensitive systems per PCI DSS 8.4.

- **CDE Access:** MFA is implemented for all access into the CDE per PCI DSS 8.4.2.

- **Remote Access:** MFA is implemented for all remote network access originating from outside the entity's network that could access or impact the CDE per PCI DSS 8.4.3, including:
  - All remote access by all personnel (users and administrators)
  - All remote access by third parties and vendors

- **Administrative Access:** MFA is required for all administrative access to critical systems.

- **Cloud Services:** MFA is required for all cloud-based business applications and services.

- **MFA Configuration:** Per PCI DSS 8.5.1, MFA systems are configured so that:
  - The MFA system is not susceptible to replay attacks
  - MFA cannot be bypassed by any users unless specifically documented and approved by management on an exception basis for a limited time
  - At least two different types of authentication factors are used
  - Success of all authentication factors is required before access is granted

### 3.11 Session Management

Systems shall implement session controls to protect against unauthorized access.

- **Session Timeout:** If a user session has been idle for more than 15 minutes, the user is required to re-authenticate to re-activate the terminal or session per PCI DSS 8.2.8.

- **Sensitive Systems:** Sessions to the CDE and systems containing customer financial information shall timeout after **[Duration, e.g., 15]** minutes of inactivity.

### 3.12 Remote Access Security

All remote work must be conducted securely to protect cardholder data and customer financial information.

- **Secure Network Connectivity:** All access to internal company systems and sensitive data must use the company-approved Virtual Private Network (VPN) with MFA.

- **Device Security Requirements:** Any device used to access company resources remotely must meet security standards:
  - Full-disk encryption enabled on all devices
  - Strong passwords or biometric controls with automatic lock after **[Number, e.g., 15]** minutes of inactivity
  - Company-approved anti-malware software installed and current
  - Operating systems and applications kept up-to-date with security patches

- **Data Handling:** Cardholder data and customer NPI may not be stored locally on personal devices. All sensitive data must be accessed through company-managed systems.

- **Physical Security:** Measures must be taken to prevent unauthorized viewing of screens in public spaces. Company equipment must be physically secured.

### 3.13 Third-Party Access

Third parties require security review and enhanced controls before receiving access to company systems or data per PCI DSS 8.2.7.

- All third parties shall undergo security assessment before access is granted.

- Third-party access shall be limited to specific systems and data required for their function.

- Accounts used by third parties for remote access are:
  - Enabled only during the time period needed
  - Disabled when not in use
  - Monitored for unexpected activity

- Third-party activities shall be monitored and logged.

- Service providers with remote access to customer premises use unique authentication factors for each customer premises per PCI DSS 8.2.3.

### 3.14 Application and System Accounts

Application and system accounts are managed with strict controls per PCI DSS 7.2.5 and 8.6.

- Application and system accounts are assigned based on least privileges necessary for operability.

- Access is limited to systems, applications, or processes that specifically require their use.

- If accounts can be used for interactive login, they are managed per PCI DSS 8.6.1:
  - Interactive use is prevented unless needed for an exceptional circumstance
  - Business justification is documented and explicitly approved by management
  - Every action taken is attributable to an individual user

- Passwords for application and system accounts are not hard coded in scripts, configuration files, or source code per PCI DSS 8.6.2.

- Passwords for application and system accounts are changed periodically based on targeted risk analysis and upon suspicion or confirmation of compromise per PCI DSS 8.6.3.

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 7.2.1, 7.3.3 |
| 3.1 | SOC 2 TSC | CC6.1 |
| 3.1 | GLBA Safeguards | § 314.4(c)(1) |
| 3.2 | PCI DSS v4.0 | 7.2.6, 8.4.2 |
| 3.2 | SOC 2 TSC | CC6.1, CC6.3 |
| 3.3 | GLBA Safeguards | § 314.4(c)(1), § 314.4(c)(5) |
| 3.3 | SOC 2 TSC | CC6.1 |
| 3.4 | PCI DSS v4.0 | 7.2.3, 8.2.4, 8.2.5, 8.2.6 |
| 3.4 | SOC 2 TSC | CC6.2, CC6.3 |
| 3.5 | PCI DSS v4.0 | 7.2.4 |
| 3.5 | SOC 2 TSC | CC6.2, CC6.3 |
| 3.5 | GLBA Safeguards | § 314.4(c)(1) |
| 3.6 | PCI DSS v4.0 | 7.2.2, 10.2 |
| 3.6 | SOC 2 TSC | CC6.1, CC6.3 |
| 3.7 | PCI DSS v4.0 | 8.2.1 |
| 3.7 | SOC 2 TSC | CC6.1 |
| 3.8 | PCI DSS v4.0 | 8.2.2 |
| 3.8 | SOC 2 TSC | CC6.1 |
| 3.9 | PCI DSS v4.0 | 8.3.2, 8.3.3, 8.3.4, 8.3.5, 8.3.6, 8.3.7, 8.3.9 |
| 3.9 | SOC 2 TSC | CC6.1 |
| 3.10 | PCI DSS v4.0 | 8.4.2, 8.4.3, 8.5.1 |
| 3.10 | SOC 2 TSC | CC6.1 |
| 3.10 | GLBA Safeguards | § 314.4(c)(5) |
| 3.11 | PCI DSS v4.0 | 8.2.8 |
| 3.11 | SOC 2 TSC | CC6.1 |
| 3.12 | PCI DSS v4.0 | 8.4.3 |
| 3.12 | SOC 2 TSC | CC6.6, CC6.7 |
| 3.12 | GLBA Safeguards | § 314.4(c)(5) |
| 3.13 | PCI DSS v4.0 | 8.2.3, 8.2.7 |
| 3.13 | SOC 2 TSC | CC6.3, CC9.2 |
| 3.13 | GLBA Safeguards | § 314.4(f) |
| 3.14 | PCI DSS v4.0 | 7.2.5, 8.6.1, 8.6.2, 8.6.3 |
| 3.14 | SOC 2 TSC | CC6.1 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Authentication Factor** | A credential used to verify identity: something you know (password), something you have (token), or something you are (biometric). |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Customer Information** | Any record containing nonpublic personal information about a customer, whether in paper, electronic, or other form (per GLBA). |
| **Least Privilege** | The security principle of restricting access rights for users to the minimum permissions needed to perform their work. |
| **Multi-Factor Authentication (MFA)** | An authentication method requiring two or more different types of verification factors to gain access. |
| **Need to Know** | Providing access to only the least amount of data needed to perform a job function. |
| **Nonpublic Personal Information (NPI)** | Personally identifiable financial information and any list, description, or grouping of consumers derived from such information. |
| **Privileged Account** | A user account with elevated permissions, such as administrator or system accounts. |
| **Privileged Access Management (PAM)** | A method to grant access to privileged accounts only when those privileges are required, immediately revoking access once no longer needed. |
| **System Owner** | The individual responsible for a specific system or application, typically a manager or technical lead. |
| **Virtual Private Network (VPN)** | A secure, encrypted connection over a public network to access company systems. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own, review, and update this policy annually. Oversee access control program and ensure compliance with PCI DSS, SOC 2, and GLBA requirements. |
| **IT Security Team** | Implement and manage technical access controls. Configure MFA, password policies, and session management. Monitor access and respond to security events. |
| **IT Department** | Process access requests and conduct access provisioning, modification, and deprovisioning. Maintain access control systems and identity management platforms. |
| **PCI Program Manager** | Ensure CDE access controls meet PCI DSS requirements. Coordinate access reviews for CDE systems. Maintain documentation for PCI assessments. |
| **Managers / System Owners** | Request and approve access for their teams. Conduct periodic access reviews. Ensure team members follow access policies. Document business justification for access. |
| **Human Resources** | Notify IT promptly of employee terminations and role changes. Coordinate access provisioning for new hires. |
| **All Workforce Members** | Follow access control requirements. Use only assigned accounts. Protect authentication credentials. Report unauthorized access or suspicious activity. Never share passwords or authentication factors. |

