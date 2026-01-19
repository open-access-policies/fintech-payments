# Physical Access Management Procedure (SEC-PROC-006)

### 1. Purpose

To describe the process for provisioning, reviewing, and revoking physical access to company facilities to ensure a secure physical environment, with enhanced controls for areas containing cardholder data or payment processing equipment.

### 2. Scope

This procedure applies to all employees, contractors, and visitors requiring access to company-controlled facilities, including:

- General office areas
- Data centers and server rooms
- Areas containing CDE system components
- Areas with payment processing equipment (POS terminals, HSMs)
- Sensitive media storage areas

### 3. Overview

This procedure outlines the standardized steps for managing physical access per PCI DSS Requirement 9. It covers the issuance of access badges for new personnel, the process for registering and escorting visitors in sensitive areas, and the requirement for regular reviews of access rights to ensure they remain appropriate.

### 4. Procedure

#### 4.1 Badge Provisioning

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Hiring Manager / HR | Submits a facility access request form for a new employee or contractor, specifying required access zones. |
| **2** | Manager | For CDE or sensitive area access: Provides documented business justification per PCI DSS 9.2.1. |
| **3** | Facilities / Security Team | Provisions and issues a physical access badge based on the approved request, corresponding to the individual's role and location. |
| **4** | Facilities / Security Team | Configures badge access to restrict CDE areas to authorized personnel only per PCI DSS 9.3. |

#### 4.2 Visitor Management

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Employee / Host | Registers visitors at the front desk before arrival or upon arrival. |
| **2** | Front Desk / Security | Issues temporary visitor badge that is visually distinguishable from employee badges per PCI DSS 9.4.2. |
| **3** | Employee / Host | Escorts visitors at all times in sensitive areas (CDE, data center) per PCI DSS 9.4.3. |
| **4** | Front Desk / Security | Maintains visitor log including name, organization, host, date/time in/out per PCI DSS 9.4.4. |
| **5** | Visitor | Returns visitor badge upon departure; badge expires within one day per PCI DSS 9.4.2. |

#### 4.3 Access Review and Revocation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Facilities / Security Team | Conducts quarterly reviews of all physical access permissions, with emphasis on CDE access. |
| **2** | Managers | Validate that physical access for their team members remains appropriate for current roles. |
| **3** | Manager / HR | Notifies Facilities/Security Team immediately upon termination of an employee or contractor. |
| **4** | Facilities / Security Team | Revokes physical access and collects access badges upon termination. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1** | PCI DSS v4.0 | 9.2.1, 9.3.1 |
| **4.1** | SOC 2 TSC | CC6.4 |
| **4.2** | PCI DSS v4.0 | 9.4.1, 9.4.2, 9.4.3, 9.4.4 |
| **4.3** | PCI DSS v4.0 | 9.3.1, 9.3.2 |

### 6. Artifact(s)

- Completed facility access request form with approvals
- Badge issuance records
- Visitor logs retained for minimum three months per PCI DSS 9.4.4
- Quarterly access review documentation
- Termination access revocation records

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Sensitive Area** | Any area that houses systems containing cardholder data, payment processing equipment, or other confidential information. |
| **Visitor** | Any individual who is not an employee, contractor, or consultant of the organization. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Hiring Manager / HR** | Initiates and approves access requests for new personnel and reports terminations promptly. |
| **Facilities / Security Team** | Manages the physical access control system, issues badges, conducts access reviews, and manages visitor logs. |
| **Employee / Host** | Responsible for their assigned access badge and for escorting any visitors they host. |
| **Managers** | Validate physical access for their team members during quarterly reviews. |
| **PCI Program Manager** | Ensures physical access controls meet PCI DSS Requirement 9 and maintains compliance evidence. |

