# BYOD Registration Procedure (AC-PROC-002)

### 1. Purpose

To establish the process for registering and securing a personally-owned device (BYOD) for access to company resources, with additional controls for devices that may access the cardholder data environment (CDE) or customer financial information.

### 2. Scope

This procedure applies to all workforce members who wish to use a personal device to access company information or systems. Special restrictions apply to devices accessing:

- Cardholder data environment (CDE) systems
- Systems containing nonpublic personal information (NPI)
- Payment processing applications
- Customer financial information

### 3. Overview

This procedure details the steps for a workforce member to register a personal device for company use, including obtaining consent, installing required security software, and ensuring the device meets security standards before access is granted. Access to the CDE from personal devices requires additional approval and enhanced security controls per PCI DSS 1.5.1.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Workforce Member | Requests to use a personal device for work purposes, specifying whether CDE or NPI access is required. |
| **2** | Manager | Reviews and approves the business need for BYOD access. For CDE access requests, documents specific business justification. |
| **3** | Workforce Member | Provides formal consent to the installation of security software and acknowledges the company's right to remotely wipe corporate data. |
| **4** | Workforce Member | The device is formally registered with the IT Department. |
| **5** | IT Department | Installs and verifies required security software (MDM/EDR) and confirms the device meets security standards: |
| | | - Full-disk encryption enabled |
| | | - Strong password/biometric authentication |
| | | - Screen lock after 15 minutes of inactivity |
| | | - Current anti-malware software |
| | | - Operating system and applications up to date |
| **6** | IT Security Team | For CDE access: Verifies device meets PCI DSS 1.5.1 requirements for dual-network devices, including personal firewall that cannot be disabled by users. |
| **7** | IT Department | Access is granted to appropriate company resources based on approval level. |

**Note:** Per PCI DSS 1.5.1 and company policy, personal devices are NOT permitted to store cardholder data locally. Access to CDE systems from personal devices is limited to view-only capabilities through company-managed applications.

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-7** | SOC 2 TSC | CC6.4 |
| **5-6** | PCI DSS v4.0 | 1.5.1 |
| **5** | GLBA Safeguards | § 314.4(c)(5) |

### 6. Artifact(s)

- Completed and signed BYOD Registration and Consent form
- MDM enrollment confirmation
- Security configuration verification checklist
- Manager approval documentation (enhanced for CDE access)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **BYOD (Bring Your Own Device)** | A policy that allows employees to use their personal devices for work-related purposes. |
| **MDM (Mobile Device Management)** | Software that allows an organization to manage and secure employees' mobile devices. |
| **EDR (Endpoint Detection and Response)** | A solution that monitors endpoint and network events for detection, investigation, and response. |
| **CDE (Cardholder Data Environment)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Workforce Member** | Requests to use a personal device, provides consent, and ensures their device is available for security setup. |
| **Manager** | Approves business need for BYOD access and provides enhanced justification for CDE access requests. |
| **IT Department** | Manages the device registration process, installs and verifies security software, and grants access. |
| **IT Security Team** | Verifies CDE access requests meet PCI DSS requirements for dual-network devices. |
| **PCI Program Manager** | Reviews and approves exceptions for CDE access from personal devices. |

