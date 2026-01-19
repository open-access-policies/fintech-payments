# Vulnerability Remediation Exception Procedure (SEC-PROC-009)

### 1. Purpose

To outline the process for formally requesting, approving, and documenting an exception to a remediation Service Level Agreement (SLA) for an identified vulnerability, with enhanced controls for exceptions affecting the cardholder data environment (CDE).

### 2. Scope

This procedure applies when an asset owner cannot remediate a vulnerability within the timeframe defined in the Vulnerability Management Policy (SEC-POL-007) and requires a formal exception. This includes:

- All systems within the CDE
- Systems connected to the CDE
- Systems processing customer financial information (NPI)
- All other company systems

### 3. Overview

This procedure provides a pathway for managing situations where immediate vulnerability remediation is not feasible. It details the steps for an asset owner to request an exception, the approval workflow with additional oversight for CDE systems, and the requirement to document approved exceptions in the risk register for regular review. Exceptions for CDE systems must include compensating controls per PCI DSS requirements.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Asset Owner | Submits a formal Exception Request Form, including: |
| | | - Detailed justification for the exception |
| | | - Vulnerability details (CVE, CVSS score, affected systems) |
| | | - Risk analysis of delayed remediation |
| | | - Compensating controls in place |
| | | - Proposed remediation timeline |
| | | - Whether CDE systems are affected |
| **2** | IT Security Team | Reviews the request and validates compensating controls are sufficient to mitigate risk. |
| **3** | PCI Program Manager | For CDE systems: Reviews to ensure compensating controls meet PCI DSS requirements and documents for compliance evidence. |
| **4** | CISO | Reviews the request for business validity and security implications, then provides final approval or denial. |
| **5** | IT Security Team | Documents the approved exception in the risk register, including: |
| | | - Exception details and justification |
| | | - Compensating controls |
| | | - Expiration date (maximum **[Duration, e.g., 90 days]** for CDE systems) |
| | | - Review schedule |
| **6** | IT Security Team | Reviews all active exceptions quarterly to ensure they are still valid and necessary. |
| **7** | IT Security Team | Notifies asset owners **[Number, e.g., 14]** days before exception expiration to ensure remediation is scheduled. |

**Note:** Exceptions for critical or high vulnerabilities (CVSS 7.0+) in the CDE require enhanced monitoring and shorter maximum durations.

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-6** | SOC 2 TSC | CC7.1 |
| **2-5** | PCI DSS v4.0 | 6.3.3, 12.3.1 |

### 6. Artifact(s)

- Completed Exception Request Form
- Risk analysis documentation
- Compensating control documentation
- Approval/denial records
- Risk register entries
- Quarterly exception review records

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Compensating Control** | An alternative security control that provides equivalent protection when a primary control (remediation) cannot be immediately implemented. |
| **Risk Register** | A log of identified risks, including vulnerability exceptions, their characteristics, compensating controls, and status. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Asset Owner** | Initiates the exception request and provides all necessary justification and documentation. Implements compensating controls. |
| **IT Security Team** | Reviews requests, validates compensating controls, maintains risk register, and conducts quarterly reviews. |
| **PCI Program Manager** | Reviews CDE-related exceptions for PCI DSS compliance and maintains compliance evidence. |
| **CISO** | Provides final approval for exception requests and ensures proper documentation. Reviews exception metrics. |

