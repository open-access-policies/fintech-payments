# Employee Onboarding and Offboarding Security Checklist (OP-PROC-007)

### 1. Purpose

To provide a formal checklist and process to ensure all security-related tasks are consistently and verifiably completed during employee onboarding and termination, with enhanced requirements for personnel with access to cardholder data or customer financial information per PCI DSS 12.7 and GLBA 314.4(e).

### 2. Scope

This procedure applies to all new and departing employees, contractors, and temporary staff, with particular attention to those with access to:

- Cardholder data environment (CDE) systems
- Payment processing applications
- Customer financial information (NPI)
- Sensitive company data

It involves the Human Resources (HR) department, the IT department, and the hiring manager.

### 3. Overview

This procedure establishes standardized checklists for the security-related aspects of employee onboarding and offboarding per PCI DSS 12.6 and 12.7. The onboarding process ensures new hires are properly vetted, provisioned, trained, and aware of their security responsibilities. The offboarding process ensures timely revocation of access and return of company assets to prevent unauthorized access after departure.

### 4. Procedure

#### 4.1 Onboarding

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Human Resources (HR) | Initiates the onboarding process upon a candidate's acceptance of an offer. |
| **2** | Human Resources (HR) | Verifies completion of background check per PCI DSS 12.7.1 (for CDE/NPI access roles). |
| **3** | New Hire | Signs required agreements: |
| | | - Confidentiality and Non-Disclosure Agreement (NDA) |
| | | - Acceptable Use Policy (AUP) |
| | | - Information Security Policy acknowledgment |
| **4** | IT Department | Provisions user accounts, access credentials, and necessary hardware based on the role defined by the hiring manager. For CDE access, ensures approval is documented per PCI DSS 7.2.1. |
| **5** | New Hire | Completes mandatory security awareness training within the first week of employment, including: |
| | | - General security awareness |
| | | - PCI DSS awareness (for CDE roles) |
| | | - NPI handling (for roles with access to customer financial data) |
| **6** | Hiring Manager & HR | Complete and sign the onboarding checklist, verifying all steps have been completed. The checklist is filed in the employee's HR record. |

#### 4.2 Offboarding

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Manager / HR | Immediately notifies the IT department of the employee's departure, providing the exact time and date of termination. |
| **2** | IT Department | Immediately upon notification (same day per PCI DSS 8.2.5), revokes all physical and logical access, including: |
| | | - User accounts and authentication credentials |
| | | - VPN and remote access |
| | | - CDE system access |
| | | - Email and collaboration tools |
| | | - Physical access badges |
| **3** | Departing Employee & Manager | The departing employee returns all company assets, including laptops, mobile devices, tokens, and security badges, to their manager. The manager verifies the return of all items. |
| **4** | Manager & HR | Complete and sign the offboarding checklist, verifying all access has been revoked and all assets have been returned. The checklist is filed in the employee's HR record. |
| **5** | IT Security Team | For individuals with CDE access: Verifies all access revocation is complete and documents for PCI DSS compliance. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1, 4.2** | SOC 2 TSC | CC6.1, CC6.2 |
| **4.1 Step 2** | PCI DSS v4.0 | 12.7.1 |
| **4.1 Steps 4-5** | PCI DSS v4.0 | 7.2.1, 12.6.1, 12.6.2 |
| **4.2 Step 2** | PCI DSS v4.0 | 8.2.5 |
| **4.1, 4.2** | GLBA Safeguards | § 314.4(e) |

### 6. Artifact(s)

- Completed and signed onboarding/offboarding checklist
- Signed NDA and AUP agreements
- Security training completion records
- Access provisioning/revocation logs
- Background check verification records (for CDE/NPI roles)
- PCI DSS compliance documentation

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Onboarding** | The process of integrating a new employee into an organization. |
| **Offboarding** | The formal process of separation when an employee leaves a company. |
| **AUP (Acceptable Use Policy)** | A document stipulating constraints and practices that a user must agree to for access to a corporate network or the Internet. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Human Resources (HR)** | Manages the overall onboarding/offboarding process, verifies background checks, and maintains official employee records. |
| **IT Department** | Responsible for provisioning and revoking access to systems and hardware. |
| **Hiring Manager** | Responsible for defining access needs, ensuring asset return, and verifying checklist completion. |
| **Employee** | Responsible for completing required agreements and training, and for returning assets upon departure. |
| **IT Security Team** | Verifies access revocation for CDE roles and maintains compliance documentation. |

