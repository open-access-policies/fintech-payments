# Security Awareness and Training Policy (SEC-POL-008)

## 1. Objective

This policy establishes requirements for security awareness education and personnel screening to ensure all **[Company Name]** workforce members understand their security responsibilities and are appropriately vetted before receiving access to cardholder data and customer financial information. This policy aligns with PCI DSS v4.0 Requirements 12.6 and 12.7, SOC 2, and GLBA Safeguards Rule requirements.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, including employees, contractors, temporary staff, and third parties who have access to:

- Systems within the cardholder data environment (CDE)
- Customer financial information (nonpublic personal information under GLBA)
- Information systems, applications, networks, and data
- Payment processing systems and cardholder data

This policy covers the entire workforce lifecycle from pre-employment screening through ongoing security awareness education.

## 3. Policy

**[Company Name]** implements a comprehensive security awareness program and personnel screening process to reduce insider risk and ensure workforce members understand their role in protecting cardholder data and customer information per PCI DSS 12.6 and 12.7.

### 3.1 Security Awareness Program

A formal security awareness program makes all personnel aware of the entity's information security policy and procedures per PCI DSS 12.6.1.

**Program Objectives:**
- Ensure personnel understand the importance of protecting cardholder data
- Educate personnel on their role in protecting the CDE
- Communicate information security policies and procedures
- Address threats and vulnerabilities relevant to the environment

**Program Coverage:**
- All workforce members with access to the CDE or customer information
- All personnel who can impact the security of account data
- Contractors and third parties with system access
- Personnel in security-sensitive roles (incident response, system administration)

### 3.2 Security Awareness Program Review

The security awareness program is reviewed and updated per PCI DSS 12.6.2.

**Review Requirements:**
- Program content is reviewed at least once every 12 months
- Program is updated as needed to address new threats and vulnerabilities
- Updates reflect changes to business objectives or risks to the CDE
- Emerging threats (phishing, social engineering, skimming) are incorporated

**Update Triggers:**
- New security threats or attack vectors identified
- Changes to the CDE or business processes
- Security incidents or lessons learned
- Regulatory changes affecting security requirements

### 3.3 Security Awareness Training Delivery

Personnel receive security awareness training per PCI DSS 12.6.3.

**Training Frequency:**
- Upon hire (within **[Number, e.g., 30]** days of start date)
- At least once every 12 months thereafter
- Upon significant changes to the CDE or security policies

**Training Methods:**
Multiple methods of communication are used, including:
- Online training modules with assessments
- In-person or virtual instructor-led sessions
- Posters, newsletters, and awareness campaigns
- Simulated phishing exercises
- Team meetings and security briefings

**Acknowledgment:**
- Personnel acknowledge at least once every 12 months that they have read and understood information security policies and procedures
- Acknowledgments are documented and retained

### 3.4 Training Content

Security awareness training covers topics relevant to protecting cardholder data and customer information.

**Core Training Topics:**
- Information security policy overview
- Cardholder data protection requirements
- Data classification and handling procedures
- Acceptable use of end-user technologies
- Password and authentication requirements
- Physical security requirements
- Clean desk and screen lock policies
- Incident reporting procedures

**Threat Awareness:**
- Social engineering and phishing recognition
- Malware prevention and detection
- Secure browsing and email practices
- Mobile device security
- Remote work security requirements

**Role-Specific Training:**
- CDE access holders: PCI DSS specific requirements
- Incident response team: Incident handling procedures
- System administrators: Secure configuration and access management
- Developers: Secure coding practices

### 3.5 Acceptable Use Training

Personnel understand acceptable use policies for end-user technologies per PCI DSS 12.2.1.

**Acceptable Use Topics:**
- Explicit approval requirements for technology use
- Acceptable uses of company technology
- List of approved hardware and software
- Prohibited activities and behaviors
- Consequences of policy violations

### 3.6 Personnel Screening

Potential personnel who will have access to the CDE are screened prior to hire per PCI DSS 12.7.1.

**Screening Requirements:**
- Background checks conducted within constraints of local laws
- Screening performed before granting CDE access
- Screening scope appropriate to the position and access level

**Screening Elements:**

**Standard Screening (all CDE-access personnel):**
- Identity verification
- Criminal history check
- Employment history verification
- Reference checks

**Enhanced Screening (elevated access roles):**
- Credit history check (where legally permitted and appropriate)
- Education verification
- Professional license verification
- Extended criminal history search

**Adverse Findings:**
- Adverse findings are reviewed by Human Resources and **[Role Title, e.g., CISO]**
- Employment eligibility is determined based on finding nature and role requirements
- Decisions are documented and retained

### 3.7 Ongoing Personnel Management

Workforce members are managed securely throughout the employment lifecycle.

**Onboarding:**
- Confidentiality and non-disclosure agreements signed as condition of employment
- Security awareness training completed within required timeframe
- Access provisioned based on least privilege principles per AC-POL-001
- Security responsibilities acknowledged in writing

**Role Changes:**
- Screening consideration for transfers to CDE-access roles
- Access adjusted to reflect new responsibilities
- Additional training for new security-sensitive roles

**Termination:**
- Immediate notification to HR and IT of voluntary or involuntary terminations
- Prompt revocation of all logical and physical access
- Return of all company property including devices, badges, and documents
- Exit process including reminder of ongoing confidentiality obligations

### 3.8 Policy Enforcement

Security policy violations result in disciplinary action per formal sanction procedures.

**Sanction Framework:**
- Formal sanction policy addresses ISMS policy violations
- Disciplinary actions are fair, consistent, and proportionate to violation severity

**Disciplinary Actions:**
- Verbal or written warnings
- Mandatory retraining
- Suspension
- Termination of employment
- Civil or criminal legal action where applicable

**Documentation:**
- All policy violations and sanctions are documented by Human Resources
- Documentation includes consultation with manager and **[Role Title, e.g., CISO]**

### 3.9 Specialized Training Programs

Additional training is provided for personnel with specialized security responsibilities.

**Incident Response Training (per PCI DSS 12.10.4):**
- Personnel responsible for incident response are trained on their responsibilities
- Training covers evidence handling and chain of custody
- Regulatory notification requirements are covered
- Payment brand incident procedures are included

**PCI DSS-Specific Training:**
- Personnel with CDE responsibilities understand applicable PCI DSS requirements
- Training covers specific requirements related to their job functions
- Updates provided when PCI DSS requirements change

**GLBA Training:**
- Personnel handling customer financial information understand GLBA requirements
- Privacy notice requirements are covered
- Customer information safeguards are emphasized

### 3.10 Training Records and Metrics

Training completion and effectiveness are tracked and reported.

**Record Keeping:**
- Training completion records maintained for all workforce members
- Acknowledgment records retained for audit purposes
- Records retained for at least **[Number, e.g., 3]** years

**Metrics:**
- Training completion rates tracked and reported
- Assessment scores monitored
- Simulated phishing results analyzed
- Repeat offenders identified for additional training

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 12.6.1 |
| 3.1 | SOC 2 TSC | CC2.2 |
| 3.1 | GLBA Safeguards | § 314.4(e)(1) |
| 3.2 | PCI DSS v4.0 | 12.6.2 |
| 3.3 | PCI DSS v4.0 | 12.6.3 |
| 3.3 | SOC 2 TSC | CC2.2 |
| 3.5 | PCI DSS v4.0 | 12.2.1 |
| 3.6 | PCI DSS v4.0 | 12.7.1 |
| 3.6 | SOC 2 TSC | CC2.1, CC2.2 |
| 3.6 | GLBA Safeguards | § 314.4(e)(1) |
| 3.9 | PCI DSS v4.0 | 12.10.4 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Personnel** | Full-time and part-time employees, temporary employees, contractors, and consultants with security responsibilities for protecting account data or that can impact the security of account data. |
| **Security Awareness Program** | An ongoing educational initiative to ensure personnel understand their security responsibilities and can recognize and respond to security threats. |
| **Background Check** | A process of verifying the identity and credentials of a candidate, which may include criminal history, employment verification, and other checks as permitted by law. |
| **Social Engineering** | Psychological manipulation techniques used to deceive individuals into divulging confidential information or performing actions that compromise security. |
| **Phishing** | A type of social engineering attack using fraudulent communications (typically email) to trick recipients into revealing sensitive information or installing malware. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own security awareness policy. Approve training content and program. Review training effectiveness. Advise on personnel screening requirements. |
| **Human Resources Department** | Manage screening and background check processes. Conduct onboarding and termination procedures. Administer sanction policy. Maintain training and acknowledgment records. |
| **IT Security Team** | Develop and maintain security awareness content. Deliver technical security training. Conduct simulated phishing exercises. Track training metrics. |
| **PCI Program Manager** | Ensure training meets PCI DSS requirements. Coordinate PCI-specific training content. Track CDE personnel training compliance. |
| **Managers/Supervisors** | Ensure direct reports complete required training. Report terminations promptly. Enforce security policies. Support sanction policy enforcement. |
| **All Workforce Members** | Complete security awareness training as required. Acknowledge security policies. Report suspected security incidents. Follow all information security policies. |

