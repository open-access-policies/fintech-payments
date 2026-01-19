# Access Control Exception Procedure (SEC-PROC-003)

### 1. Purpose

To provide a formal process for requesting, reviewing, and documenting exceptions to the Access Control Policy password and authentication requirements, with enhanced controls for exceptions affecting the cardholder data environment (CDE) or customer financial information.

### 2. Scope

This procedure applies to all personnel and systems within the organization when a deviation from the established Access Control Policy password and authentication requirements is required. This includes:

- Password complexity or length requirements
- Multi-factor authentication requirements
- Session timeout requirements
- Account lockout requirements
- Systems in the CDE or processing NPI

### 3. Overview

This procedure outlines the steps for submitting, evaluating, and documenting requests for exceptions to the company's Access Control Policy password and authentication requirements. It ensures that any deviation is subject to a formal risk assessment and approval by the Security Officer, and that all approved exceptions are tracked. Exceptions affecting CDE systems require additional review to ensure continued PCI DSS compliance.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | User or System Owner | Submits a formal Access Control Policy Exception Request form, including: |
| | | - Detailed justification for the exception |
| | | - Duration of exception needed |
| | | - Proposed compensating controls |
| | | - Systems and data affected (including CDE/NPI classification) |
| **2** | IT Security Team | Conducts a risk assessment of the request to evaluate potential security impacts. |
| **3** | PCI Program Manager | For CDE systems: Reviews to ensure exception does not violate PCI DSS requirements or documents compensating controls per PCI DSS 12.3.1. |
| **4** | CISO / Security Officer | Reviews risk assessment and formally approves or denies the request in writing. |
| **5** | IT Security Team | Documents all approved exceptions in a central tracking log, including: |
| | | - Justification and risk assessment |
| | | - Compensating controls implemented |
| | | - Expiration date |
| | | - Review schedule |
| **6** | IT Security Team | Reviews all active exceptions quarterly and upon expiration to determine if they should be renewed or revoked. |

**Note:** Exceptions to PCI DSS requirements must include documented compensating controls and are subject to QSA review during annual assessments.

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-6** | SOC 2 TSC | CC6.8 |
| **3, 5** | PCI DSS v4.0 | 12.3.1 (Targeted Risk Analysis) |

### 6. Artifact(s)

- Completed Access Control Policy Exception Request form
- Risk assessment documentation
- Compensating control documentation (for PCI DSS)
- Exception tracking log with quarterly review records
- Approval/denial documentation

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Compensating Control** | An alternative security control that provides equivalent protection when a primary control cannot be implemented. |
| **Targeted Risk Analysis** | A risk analysis performed to determine the frequency of a specific activity, per PCI DSS 12.3.1. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **User / System Owner** | Initiates the exception request and provides all necessary information and justification. |
| **IT Security Team** | Performs risk assessment, maintains exception tracking log, and conducts quarterly reviews. |
| **PCI Program Manager** | Reviews CDE-related exceptions for PCI DSS compliance implications and compensating controls. |
| **CISO / Security Officer** | Makes the final decision on the exception request and maintains all approval documentation. |

