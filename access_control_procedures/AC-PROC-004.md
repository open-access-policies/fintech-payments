# User Access Lifecycle Procedure (AC-PROC-004)

### 1. Purpose

To define the process for requesting, approving, implementing, modifying, and revoking user access to company information systems, ensuring the principle of least privilege is enforced, with enhanced controls for access to the cardholder data environment (CDE) and customer financial information.

### 2. Scope

This procedure applies to all workforce members, managers, system owners, and IT personnel involved in the lifecycle of user access to all company information systems, including:

- Production and development systems
- Cardholder data environment (CDE) systems
- Systems processing nonpublic personal information (NPI)
- Cloud services and applications
- Third-party and vendor accounts

### 3. Overview

This procedure covers the end-to-end management of user access, from initial provisioning and modification to final revocation upon termination. It ensures that all access changes are properly authorized, implemented, and documented to maintain a secure environment in accordance with PCI DSS Requirement 7 and 8, SOC 2, and GLBA Safeguards Rule requirements.

### 4. Procedure

#### 4.1 Access Provisioning

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Requestor (User or Manager) | Submits an access request ticket specifying the system, required permissions, and business justification. |
| **2** | Manager | Approves the request in the ticket, verifying the business need and confirming the access aligns with the user's job role. |
| **3** | System or Information Owner | Provides secondary approval, ensuring the request aligns with data classification and security policies. |
| **4** | PCI Program Manager | For CDE access: Provides additional approval per PCI DSS 7.2.3, verifying documented business need and role-based access. |
| **5** | IT Department | Provisions the approved access with a unique user ID per PCI DSS 8.2.1. |
| **6** | IT Department | Documents the provisioning in the access management system with approval chain. |

#### 4.2 Access Modification

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Manager | Identifies need for access modification due to role change, project assignment, or other business need. |
| **2** | Manager | Submits access modification request with business justification. |
| **3** | System Owner / IT Security | Reviews modification request; for CDE access changes, validates continued business need. |
| **4** | IT Department | Implements approved modifications and revokes access no longer required. |

#### 4.3 Access Revocation (Termination)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Human Resources | Notifies the IT Department of a workforce member's termination. For involuntary terminations, notification occurs before or immediately upon termination. |
| **2** | IT Department | Immediately revokes all logical access for the terminated workforce member per PCI DSS 8.2.5. |
| **3** | Facilities / Physical Security | Immediately revokes all physical access (badges, keys) for the terminated workforce member. |
| **4** | IT Department | Disables or removes all accounts within **[Number, e.g., 24]** hours of termination. |
| **5** | IT Department | Confirms completion of all revocation tasks and updates relevant records. |
| **6** | IT Security Team | Verifies access revocation for CDE systems and documents for compliance evidence. |

**Emergency Revocation:** For suspected security incidents or policy violations involving CHD or NPI, access may be suspended immediately pending investigation.

#### 4.4 Inactive Account Management

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Department | Generates monthly report of accounts inactive for 90 days or more per PCI DSS 8.2.6. |
| **2** | IT Department | Disables or removes inactive accounts within 90 days of last activity. |
| **3** | IT Security Team | Documents inactive account actions for compliance evidence. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1** | PCI DSS v4.0 | 7.2.1, 7.2.2, 7.2.3, 8.2.1 |
| **4.1** | SOC 2 TSC | CC6.1, CC6.2 |
| **4.1** | GLBA Safeguards | § 314.4(c)(1) |
| **4.2** | PCI DSS v4.0 | 7.2.4 |
| **4.3** | PCI DSS v4.0 | 8.2.4, 8.2.5 |
| **4.3** | SOC 2 TSC | CC6.2 |
| **4.4** | PCI DSS v4.0 | 8.2.6 |

### 6. Artifact(s)

- Completed access request tickets with full approval chain
- HR termination notification records
- IT confirmation of access revocation
- Inactive account reports and remediation records
- CDE access approval documentation

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **System Owner** | The individual or group responsible for the overall procurement, development, integration, modification, operation, and maintenance of an information system. |
| **Information Owner** | The individual with statutory or operational authority for specified information and responsibility for establishing the controls for its generation, collection, processing, dissemination, and disposal. |
| **CDE (Cardholder Data Environment)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **NPI (Nonpublic Personal Information)** | Personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Requestor** | Initiates access requests with a clear justification for the required permissions. |
| **Manager** | Provides initial approval for access requests, confirming the business need for their direct reports. |
| **System / Information Owner** | Provides secondary approval for access, ensuring it aligns with security and data handling policies. |
| **PCI Program Manager** | Provides additional approval for CDE access and maintains compliance documentation. |
| **IT Department** | Implements approved access changes and is responsible for timely revocation of access upon notification. |
| **IT Security Team** | Verifies access controls and documents compliance evidence. |
| **Human Resources** | Manages the employee lifecycle and provides timely notification of terminations to the IT Department. |

