# Third-Party Component Approval Procedure (ENG-PROC-002)

### 1. Purpose

To define the steps for scanning, reviewing, and approving the use of new open-source or commercial software components to minimize security and licensing risks, with enhanced requirements for components used in the cardholder data environment (CDE) or payment processing applications per PCI DSS 6.3.

### 2. Scope

This procedure applies to all new open-source and commercial third-party software components, libraries, and dependencies being considered for inclusion in company software, particularly:

- Components for CDE applications
- Payment processing libraries
- Encryption and security libraries
- Components handling customer financial information (NPI)

### 3. Overview

This procedure describes the process for managing the security of third-party components per PCI DSS 6.3.2. It begins with a developer proposing a new component, followed by automated scanning, a formal review of the results by engineering and security teams, and concludes with a documented approval or denial.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Developer | Proposes the use of a new third-party component by creating an issue ticket documenting: |
| | | - Component name, version, and source |
| | | - Purpose and business justification |
| | | - Whether it will be used in CDE or NPI applications |
| **2** | Developer / CI/CD Pipeline | Uses automated Software Composition Analysis (SCA) tools to scan the component for: |
| | | - Known vulnerabilities (CVEs) |
| | | - License compliance issues |
| | | - End-of-life or unmaintained status |
| **3** | Development Team Lead | Reviews SCA scan results and assesses: |
| | | - Severity of any identified vulnerabilities |
| | | - Implications of the component's license |
| | | - Component's maintenance status and community support |
| **4** | IT Security Team | For CDE/NPI components: Reviews security implications and provides approval per PCI DSS 6.3.2. |
| **5** | Development Team | If vulnerabilities are found, creates a remediation plan: |
| | | - Wait for a patched version |
| | | - Use an alternative component |
| | | - Document risk acceptance with compensating controls (requires CISO approval for CDE) |
| **6** | Development Team Lead | Based on the review and any remediation plan, formally approves or denies the use of the component. |
| **7** | Development Team | Updates the approved component inventory with the new component. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-7** | SOC 2 TSC | CC8.1 |
| **2-6** | PCI DSS v4.0 | 6.3.2 |
| **2** | NIST | SP 800-161 |

### 6. Artifact(s)

- SCA scan results
- Component approval/denial documentation
- Risk acceptance documentation (if applicable)
- Updated approved component inventory
- License compliance records

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **SCA (Software Composition Analysis)** | Automated process that identifies third-party software in a codebase to evaluate security, license compliance, and code quality. |
| **CVE (Common Vulnerabilities and Exposures)** | A list of publicly disclosed computer security flaws. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Developer** | Proposes new components and initiates the SCA scan. Documents business justification. |
| **Development Team Lead** | Reviews scan results, makes the final decision on component use, and ensures proper documentation. |
| **IT Security Team** | Reviews SCA results for CDE components, provides guidance on vulnerability risk, and reviews risk acceptance cases. |
| **PCI Program Manager** | Ensures component approval process meets PCI DSS requirements for CDE applications. |

