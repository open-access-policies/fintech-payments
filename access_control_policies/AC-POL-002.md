# Acceptable Use Policy (AC-POL-002)

## 1. Objective

This policy establishes acceptable use rules for **[Company Name]**'s network, information systems, and technology resources that meet PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements while maintaining a secure and productive work environment. This policy protects company information resources, cardholder data, and customer financial information through appropriate use of technology.

## 2. Scope

This policy applies to all **[Company Name]** workforce members and anyone granted access to company network, information systems, and technology resources. It encompasses:

- All network resources including internet access, email, and cloud services
- All devices connected to the corporate network or accessing company data
- All software applications and tools used for business purposes
- Systems within or connected to the cardholder data environment (CDE)
- Systems processing customer financial information

## 3. Policy

All use of **[Company Name]**'s technology resources must be conducted in a secure, professional manner that supports business objectives and protects cardholder data and customer information per PCI DSS 12.2.1.

### 3.1 General Use and Ownership

End-user technologies must be explicitly approved before use per PCI DSS 12.2.1.

**Company Property:**
- All network infrastructure, systems, software, and data are the property of **[Company Name]**
- Employees have no expectation of privacy when using company systems
- Company reserves the right to access, monitor, and review all use of company systems

**Monitoring:**
- Network traffic and system usage are monitored for security threats and policy compliance
- User activities on CDE systems are logged and monitored per OP-POL-005
- Monitoring complies with applicable laws and regulations

**Business Purpose:**
- Network resources and technology tools are provided primarily for business activities
- Limited personal use is permitted if it does not interfere with work performance, security, or company policies

### 3.2 Approved Technologies

Only approved hardware and software may be used to access company resources per PCI DSS 12.2.1.

**Hardware Approval:**
- Only company-approved hardware may connect to the corporate network
- Personal devices (BYOD) require explicit approval and MDM enrollment
- Unauthorized devices are prohibited from connecting to the CDE

**Software Approval:**
- A list of company-approved products/services and software is maintained
- Use of any third-party service requires prior approval from IT/Security
- Software must have a valid business justification
- Software must be properly licensed

**Prohibited Software:**
The following software categories are strictly prohibited:
- Unlicensed or pirated software
- Peer-to-peer (P2P) file-sharing clients
- Cryptocurrency mining software
- Tools designed to disable or circumvent security controls
- Software from untrusted or unverified sources
- Software that collects or transmits sensitive data without explicit consent

### 3.3 Security Requirements

Workforce members are responsible for maintaining security and protecting company data per PCI DSS 12.6.3.3.

**Credential Security:**
- Account credentials must not be shared
- Each user must use only their assigned accounts
- Passwords must meet complexity requirements per AC-POL-001
- Multi-factor authentication must be used when required

**Malware Prevention:**
- Exercise caution with email attachments and links
- Report suspicious emails to IT Security immediately
- Do not disable or circumvent anti-malware protections
- Report any suspected malware infection immediately

**Data Protection:**
- Transmission of sensitive data must use approved, encrypted methods
- Cardholder data may only be accessed, stored, or transmitted per SEC-POL-004
- Customer financial information must be protected per GLBA requirements
- Do not store cardholder data on personal devices or unauthorized systems

**Incident Reporting:**
- Report suspected security incidents immediately per RES-POL-001
- Report unauthorized access or vulnerabilities to IT Security
- Report lost or stolen devices containing company data

### 3.4 Prohibited Activities

The following activities are prohibited when using company technology resources.

**Illegal Activities:**
- Any activity that violates local, state, or federal law
- Harassment, discrimination, or threats
- Copyright infringement or software piracy
- Fraud or misrepresentation

**Security Violations:**
- Attempting to bypass or disable security controls
- Accessing systems, data, or accounts without explicit authorization
- Sharing credentials or authentication factors
- Copying or relocating cardholder data without authorization per PCI DSS 3.4.2
- Disabling logging or audit controls

**Network Misuse:**
- Activities that could disrupt network services
- Degrading performance for other users
- Port scanning or network probing
- Unauthorized access attempts

**Data Handling Violations:**
- Using unapproved file-sharing services for company data
- Transferring company data to personal cloud storage
- Sending cardholder data via unsecured channels
- Storing cardholder data in unauthorized locations

**Inappropriate Use:**
- Accessing inappropriate or offensive content
- Using company resources for personal business ventures
- Excessive personal use that impacts productivity

### 3.5 CDE-Specific Requirements

Additional requirements apply when accessing the cardholder data environment.

**CDE Access:**
- Access only systems and data necessary for your job function
- Do not copy or relocate cardholder data without documented authorization
- Report any unauthorized cardholder data storage immediately
- Follow all PCI DSS requirements when handling cardholder data

**Remote CDE Access:**
- Requires VPN and multi-factor authentication
- Only from company-approved and secured devices
- Not permitted from public or shared computers
- Not permitted from unsecured networks

### 3.6 Email and Communication

Email and electronic communications must be used professionally and securely.

**Email Security:**
- Do not open attachments or click links from unknown senders
- Report phishing attempts to IT Security
- Do not send cardholder data via email unless encrypted per PCI DSS 4.2.1
- Use approved encryption methods for sensitive communications

**Professional Use:**
- Email is primarily for business communication
- Communications must be professional and appropriate
- Do not use email for illegal or unethical purposes
- Retain business-related emails per retention requirements

### 3.7 Internet and Cloud Services

Internet access and cloud service use must align with security requirements.

**Internet Use:**
- Internet access is provided for business purposes
- Do not access sites that pose security risks
- Do not download unauthorized software
- Follow content filtering policies

**Cloud Services:**
- Only use approved cloud services
- Do not store cardholder data in unapproved cloud services
- Do not store customer financial information in unapproved services
- Follow data classification requirements for cloud storage

**AI Tools:**
- AI-powered tools require prior approval from IT/Security
- Do not enter cardholder data into AI tools
- Do not enter confidential company or customer data into public AI tools
- Approved AI tools must be used according to specific guidelines

### 3.8 Mobile Device Use

Mobile devices must be used securely when accessing company resources.

**Company Devices:**
- Follow all security configurations and policies
- Report lost or stolen devices immediately
- Do not jailbreak or root company devices
- Keep devices updated with security patches

**Personal Devices (BYOD):**
- Must be enrolled in MDM and meet security requirements
- Company reserves right to remote wipe company data
- Report lost or stolen devices immediately
- Separate personal and company data

### 3.9 Physical Security

Workforce members must maintain physical security of technology resources.

**Workstation Security:**
- Lock screens when leaving workstations unattended
- Do not leave sensitive information visible (clean desk)
- Protect devices from theft
- Report theft or loss immediately

**Media Handling:**
- Protect removable media containing sensitive data
- Store media securely when not in use
- Dispose of media securely per OP-POL-003

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1, 3.2 | PCI DSS v4.0 | 12.2.1 |
| 3.1, 3.2 | SOC 2 TSC | CC6.1 |
| 3.3 | PCI DSS v4.0 | 12.6.3.3 |
| 3.3 | SOC 2 TSC | CC6.7, CC6.8 |
| 3.4 | PCI DSS v4.0 | 3.4.2 |
| 3.5 | PCI DSS v4.0 | 7.2.2, 8.4.2 |
| 3.6 | PCI DSS v4.0 | 4.2.1 |
| 3.7 | GLBA Safeguards | § 314.4(c)(3) |
| 3.8 | PCI DSS v4.0 | 1.5.1 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **End-User Technologies** | Hardware and software that store, process, transmit, or print cardholder data, or have access to systems that do. |
| **Network Resources** | Company-owned or managed hardware and software providing network connectivity and services. |
| **Sensitive Data** | Company information requiring protection, including cardholder data, customer financial information, and proprietary business information. |
| **Third-Party Service** | Any software, application, or online service not owned or directly controlled by **[Company Name]**. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own acceptable use policy. Approve technology for use. Review and update policy annually. |
| **IT Department** | Implement technical controls. Maintain approved hardware/software lists. Monitor for violations. Investigate security incidents. |
| **IT Security Team** | Monitor compliance. Approve third-party services. Respond to security incidents. Conduct awareness training. |
| **Managers** | Ensure team members understand and follow policy. Address violations in consultation with IT and HR. |
| **All Workforce Members** | Comply with policy. Use resources responsibly. Report violations or security concerns. Complete security awareness training. |

