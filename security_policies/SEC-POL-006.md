# Physical Security Policy (SEC-POL-006)

## 1. Objective

This policy establishes physical security requirements for **[Company Name]**'s facilities, equipment, and cardholder data environment (CDE) in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that appropriate physical safeguards are implemented to restrict physical access to systems that store, process, or transmit cardholder data and customer financial information, and to protect against unauthorized access, theft, environmental hazards, and physical threats.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, contractors, visitors, and third parties who access company facilities or handle company equipment. It encompasses:

- All facilities containing systems in the cardholder data environment (CDE)
- Sensitive areas within the CDE (data centers, server rooms, payment processing areas)
- Corporate offices and remote work environments
- All physical assets including servers, workstations, point-of-interaction (POI) devices, networking equipment, and media
- Cloud provider facilities where company data is processed or stored

## 3. Policy

**[Company Name]** implements layered physical security controls to protect the CDE, customer financial information, and all physical assets per PCI DSS Requirement 9 and GLBA requirements.

### 3.1 Facility Entry Controls

Appropriate facility entry controls restrict physical access to systems in the CDE per PCI DSS 9.2.1.

**Entry Control Requirements:**
- Electronic badge access systems or equivalent controls are implemented for facilities containing CDE systems
- Multi-factor authentication or dual-control access required for sensitive areas (data centers, server rooms)
- Physical access controls are in place at each computer room, data center, and physical area with CDE systems
- Access controls are monitored and maintained to ensure only authorized personnel gain access

**Network Access Point Security (per PCI DSS 9.2.2, 9.2.3):**
- Physical and/or logical controls restrict use of publicly accessible network jacks
- Physical access to wireless access points, gateways, networking/communications hardware, and telecommunication lines is restricted
- Network jacks in public areas are disabled unless explicitly authorized

**Console Security (per PCI DSS 9.2.4):**
- Access to consoles in sensitive areas is restricted via locking when not in use
- Automatic screen locks activate after **[Duration, e.g., 15 minutes]** of inactivity

### 3.2 Personnel Physical Access

Procedures authorize and manage physical access of personnel to the CDE per PCI DSS 9.3.1.

**Access Management:**
- Personnel are clearly identified through badge systems or equivalent mechanisms
- Changes to individual physical access requirements are managed promptly
- Personnel identification is revoked or terminated upon separation or role change
- Access to the identification/badging system is limited to authorized personnel

**Access Authorization:**
- Physical access to the CDE requires formal approval based on job role and business need
- Access permissions are reviewed at least every **[Timeframe, e.g., 6 months]**
- Access lists are maintained and kept current

### 3.3 Visitor Management

Procedures authorize and manage visitor access to the CDE per PCI DSS 9.3.2.

**Visitor Authorization:**
- Visitors are authorized before entering the CDE
- Visitors are escorted at all times within the CDE
- Visitors are clearly identified with badges or identification that expires
- Visitor badges visibly distinguish visitors from personnel

**Visitor Badge Management (per PCI DSS 9.3.3):**
- Visitor badges or identification are surrendered or deactivated before visitors leave or at expiration date

**Visitor Log (per PCI DSS 9.3.4):**
A visitor log maintains physical record of visitor activity including:
- Visitor name and organization represented
- Date and time of visit (entry and exit)
- Name of personnel authorizing physical access
- Log retention for at least three months unless otherwise restricted by law

### 3.4 Media Physical Security

All media with cardholder data is physically secured per PCI DSS 9.4.

**Media Storage (per PCI DSS 9.4.1, 9.4.2):**
- All media with cardholder data is physically secured in locked storage
- Media is classified according to the sensitivity of the data

**Media Distribution (per PCI DSS 9.4.3, 9.4.4):**
- Media sent outside the facility is logged
- Media is sent by secured courier or trackable delivery method
- Offsite tracking logs include details about media location
- Management approves all media with cardholder data moved outside the facility

**Media Inventory (per PCI DSS 9.4.5):**
- Inventory logs of all electronic media with cardholder data are maintained
- Inventory is verified at least annually

**Media Destruction (per PCI DSS 9.4.6, 9.4.7):**

**Hard-copy materials:**
- Cross-cut shredded, incinerated, or pulped so data cannot be reconstructed
- Stored in secure containers prior to destruction

**Electronic media:**
- Destroyed or rendered unrecoverable through secure wiping, degaussing, or physical destruction
- Follows NIST SP 800-88 guidelines for media sanitization

### 3.5 Point-of-Interaction (POI) Device Security

POI devices that capture payment card data are protected from tampering and unauthorized substitution per PCI DSS 9.5.

**POI Device Inventory (per PCI DSS 9.5.1):**
A list of POI devices is maintained including:
- Device make, model, and serial number
- Location of device
- Device serial number or unique identifier

**POI Device Inspection:**
- Devices are periodically inspected for tampering or unauthorized substitution
- Inspection frequency is based on risk assessment per PCI DSS 12.3.1
- Personnel are trained to recognize signs of tampering

**Tampering Detection:**
- Inspect device surfaces for unexpected attachments or modifications
- Verify security seals and labels are intact
- Compare device serial numbers against inventory
- Report suspected tampering to security immediately

### 3.6 Sensitive Area Controls

Enhanced controls protect sensitive areas within the CDE.

**Sensitive Area Definition:**
- Data centers and server rooms containing CDE systems
- Areas where cardholder data is processed, stored, or transmitted
- Network operations centers
- Areas containing payment processing equipment

**Sensitive Area Controls:**
- Separate access controls for sensitive areas within broader facilities
- Access limited to personnel with specific job-related need
- 24/7 physical security monitoring where feasible
- Environmental controls (fire suppression, climate control, power management)

### 3.7 Remote Work Environment Security

Remote work environments meet security requirements to protect company information and CDE access.

**Remote Work Requirements:**
- Dedicated workspace with privacy measures
- Secure storage for company equipment when not in use
- Physical security of devices and materials
- Prohibition of accessing cardholder data in public spaces
- Privacy screens required when working on sensitive information in shared spaces

**Remote CDE Access:**
- Remote access to CDE requires VPN and multi-factor authentication
- Cardholder data may not be stored locally on personal devices
- Remote work environments with CDE access must be approved by **[Role Title, e.g., CISO]**

### 3.8 Equipment and Asset Protection

All company equipment and physical assets are protected throughout their lifecycle.

**Equipment Security:**
- Full disk encryption for all laptops and mobile devices
- Remote wipe capabilities for mobile devices
- Asset tagging and inventory tracking
- Secure storage requirements for devices containing sensitive information

**Asset Lifecycle:**
- Secure provisioning with pre-configured security settings
- Regular physical inventory audits
- Secure decommissioning with verified data destruction
- Return procedures for workforce member separation

### 3.9 Cloud Provider Physical Security Oversight

Physical security controls of cloud service providers are validated per PCI DSS 12.8 requirements.

**Cloud Provider Requirements:**
- SOC 2 Type II certification or equivalent demonstrating physical security controls
- Multi-factor authentication and biometric access controls for data center facilities
- 24/7 physical security monitoring and surveillance
- Environmental controls (fire suppression, climate control, power management)

**Validation:**
- Annual review of cloud providers' security certifications and audit reports
- Validation of physical security controls through third-party assessments
- Contractual agreements including physical security standards

### 3.10 CCTV and Surveillance

Video surveillance systems monitor entry/exit points and sensitive areas per PCI DSS 9.1.1.

**Surveillance Requirements:**
- CCTV coverage of entry/exit points to CDE and sensitive areas
- Video retention for minimum **[Duration, e.g., 90 days]** with secure storage
- Video is protected from unauthorized access and tampering
- Video review procedures for incident investigation

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 9.2.1, 9.2.2, 9.2.3, 9.2.4 |
| 3.1 | SOC 2 TSC | CC6.4 |
| 3.2 | PCI DSS v4.0 | 9.3.1 |
| 3.3 | PCI DSS v4.0 | 9.3.2, 9.3.3, 9.3.4 |
| 3.3 | SOC 2 TSC | CC6.4 |
| 3.4 | PCI DSS v4.0 | 9.4.1-9.4.7 |
| 3.4 | GLBA Safeguards | § 314.4(c)(6) |
| 3.5 | PCI DSS v4.0 | 9.5.1 |
| 3.6 | PCI DSS v4.0 | 9.1.1, 9.2.1 |
| 3.9 | PCI DSS v4.0 | 12.8.1, 12.8.4 |
| 3.9 | SOC 2 TSC | CC9.1 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Point-of-Interaction (POI) Device** | Device that captures payment card data via direct physical interaction with the payment card form factor (e.g., card swipes, dips, taps). |
| **Sensitive Area** | Any area containing systems that store, process, or transmit cardholder data, or that could impact the security of the CDE. |
| **Facility** | Physical boundary of a business premise within which CDEs and sensitive areas reside. |
| **Media** | All paper and electronic media containing cardholder data, including hard drives, backup tapes, removable storage, and printed materials. |
| **Skimming** | Unauthorized capture of payment card data using devices attached to legitimate payment terminals. |
| **Tailgating** | Unauthorized access gained by following an authorized person through a controlled access point. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own physical security policy. Approve access to sensitive areas. Ensure compliance with PCI DSS physical security requirements. |
| **Facilities Management** | Implement and maintain physical security systems. Manage visitor access and logs. Coordinate building security and environmental controls. |
| **IT Security Team** | Secure IT equipment and infrastructure. Manage POI device inventory. Conduct physical security assessments. Monitor surveillance systems. |
| **PCI Program Manager** | Ensure physical security meets PCI DSS requirements. Maintain POI device inventory. Coordinate with QSA on physical security assessments. |
| **Reception/Administrative Staff** | Manage visitor registration and badging. Monitor lobby areas. Enforce visitor policies. |
| **All Workforce Members** | Comply with physical security policies. Secure workspaces and equipment. Challenge unauthorized individuals. Report security incidents. Report suspected POI device tampering. |
| **Remote Workers** | Implement home office security measures. Protect company equipment. Follow secure work practices. |

