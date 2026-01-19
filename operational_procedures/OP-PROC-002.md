# Mobile Device Enrollment Procedure (OP-PROC-002)

### 1. Purpose

To detail the steps for enrolling a new or personal device in the Mobile Device Management (MDM) system and ensuring it meets all security configuration requirements before being granted access to company resources, with enhanced controls for devices that may access the cardholder data environment (CDE) or customer financial information.

### 2. Scope

This procedure applies to all employees, contractors, and other authorized users who wish to use a personal or company-issued mobile device to access company data or systems, including:

- Company-issued mobile devices (smartphones, tablets)
- Personal devices (BYOD) approved for business use
- Devices requiring access to company email, applications, or data
- Devices that may access CDE systems or customer financial information (NPI)

### 3. Overview

This procedure describes the process for onboarding a mobile device, from obtaining management approval to final verification of security compliance per PCI DSS 1.5.1 requirements for devices connecting to both untrusted networks and the CDE. It ensures that all devices connecting to the corporate network are properly managed and secured, minimizing the risk of data loss or unauthorized access.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | User | Submits a request to their manager for approval to use a mobile device for business purposes, specifying: |
| | | - Device type and model |
| | | - Required access (email, applications, CDE access) |
| | | - Whether device is company-issued or personal (BYOD) |
| **2** | Manager | Reviews the request. If approved, forwards approval to the IT Security Team. For CDE access requests, provides documented business justification. |
| **3** | IT Security Team | Provides the user with instructions for enrolling their device into the company's MDM solution. |
| **4** | User | Enrolls their device in the MDM system and accepts the company's terms and conditions for mobile device usage, including: |
| | | - Consent to remote wipe capabilities |
| | | - Agreement to security policy enforcement |
| | | - Acknowledgment of monitoring |
| **5** | MDM System (Automated) | Automatically scans the device to verify compliance with security policies: |
| | | - Passcode complexity (minimum 6 digits or equivalent) |
| | | - Device encryption enabled |
| | | - OS version current (within supported versions) |
| | | - Screen lock timeout (maximum 15 minutes) |
| | | - No jailbreak/root detected |
| **6** | IT Security Team | Reviews the compliance report from the MDM system. |
| **7** | IT Security Team | For CDE access: Verifies personal firewall or equivalent protection per PCI DSS 1.5.1 is active and cannot be disabled by user. |
| **8** | IT Security Team | If device is compliant, grants access to approved company resources based on request. |
| **9** | IT Security Team | If device is not compliant, notifies user of specific remediation steps. Access is denied until device meets all security requirements. |

**Note:** Per PCI DSS and company policy, cardholder data and customer NPI may NOT be stored locally on mobile devices.

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-9** | SOC 2 TSC | CC6.7, CC6.8 |
| **5-7** | PCI DSS v4.0 | 1.5.1 |
| **5** | GLBA Safeguards | § 314.4(c)(5) |

### 6. Artifact(s)

- MDM enrollment confirmation
- Device compliance verification report
- Manager approval documentation
- User acceptance of terms and conditions
- CDE access justification (if applicable)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **MDM (Mobile Device Management)** | Software that allows an organization to secure, monitor, and manage mobile devices. |
| **BYOD (Bring Your Own Device)** | A policy that allows employees to use their personal devices for work-related purposes. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **User** | Responsible for requesting approval, enrolling their device, and ensuring it remains compliant with policies. |
| **Manager** | Responsible for approving or denying requests for mobile device usage and providing business justification for CDE access. |
| **IT Security Team** | Responsible for managing the MDM system, providing enrollment instructions, verifying device compliance, and enforcing security controls. |
| **PCI Program Manager** | Reviews CDE access requests to ensure compliance with PCI DSS requirements. |

