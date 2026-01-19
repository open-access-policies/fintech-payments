# Lost or Stolen Device Response Procedure (OP-PROC-003)

### 1. Purpose

To provide the immediate steps a user and the IT Security Team take when a mobile device used for company business is reported lost or stolen, with enhanced procedures for devices that may have accessed cardholder data or customer financial information.

### 2. Scope

This procedure applies to all users of company-issued or personal mobile devices (BYOD) that are enrolled in the company's Mobile Device Management (MDM) system or have access to company resources, including:

- Smartphones and tablets
- Laptops
- Any device with access to email, company applications, or data
- Devices that have accessed CDE systems or customer financial information

### 3. Overview

This procedure details the rapid response actions required to mitigate security risk arising from a lost or stolen mobile device. The primary goals are to protect company data, cardholder data, and customer financial information by remotely locking and wiping the device and to prevent unauthorized access by revoking associated credentials. For devices with CDE access, this event may trigger incident response procedures.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | User | Immediately (within 1 hour of discovery) reports the lost or stolen device to the IT Security Team through the designated emergency contact: **[Contact Method, e.g., security@company.com or emergency hotline]**. |
| **2** | User | Provides details: device type, data accessed (including whether CDE or NPI was accessed), last known location, circumstances. |
| **3** | IT Security Team | Upon receiving the report, immediately initiates the remote lock command via the MDM system. |
| **4** | IT Security Team | Initiates the remote wipe command via the MDM system to erase all corporate data from the device. |
| **5** | IT Security Team | Immediately revokes all access credentials associated with the device: |
| | | - User's primary account (temporary suspension or password reset) |
| | | - VPN access |
| | | - Application-specific passwords and tokens |
| | | - MFA tokens associated with the device |
| **6** | IT Security Team | Determines if the device had access to cardholder data or customer financial information. |
| **7** | PCI Program Manager | For devices with CDE access: Assesses whether incident response procedures (RES-PROC-001) should be initiated and determines if payment brand notification is required per PCI DSS 12.10.1. |
| **8** | Privacy Officer | For devices with NPI access: Assesses breach notification requirements under GLBA and applicable state laws. |
| **9** | IT Security Team | Creates a formal incident report documenting the event, actions taken, and outcome. |
| **10** | IT Security Team | Issues replacement device or restores user access after verification of secure replacement. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-9** | SOC 2 TSC | CC6.4, CC7.3 |
| **6-7** | PCI DSS v4.0 | 12.10.1, 12.10.5 |
| **8** | GLBA Safeguards | § 314.4(h) |

### 6. Artifact(s)

- Incident report documenting loss/theft, response actions, and resolution
- MDM logs showing remote lock and wipe commands
- Credential revocation records
- Breach assessment documentation (if applicable)
- Replacement device provisioning records

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Remote Lock** | A feature of MDM software that allows an administrator to remotely make a device inaccessible. |
| **Remote Wipe** | A feature of MDM software that allows an administrator to remotely delete all data from a device. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **User** | Responsible for the timely reporting of a lost or stolen device within 1 hour of discovery. |
| **IT Security Team** | Responsible for executing remote lock and wipe, revoking credentials, documenting the incident, and coordinating response. |
| **PCI Program Manager** | Assesses CDE-related incidents for PCI DSS notification requirements. |
| **Privacy Officer** | Assesses NPI-related incidents for GLBA breach notification requirements. |

