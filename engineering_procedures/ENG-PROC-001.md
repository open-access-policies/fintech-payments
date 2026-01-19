# Application Security Testing Procedure (ENG-PROC-001)

### 1. Purpose

To detail the process for conducting static application security testing (SAST), dynamic application security testing (DAST), and penetration testing to identify and remediate security vulnerabilities in applications, with enhanced requirements for applications processing cardholder data or customer financial information per PCI DSS Requirements 6 and 11.

### 2. Scope

This procedure applies to all company-developed applications, including:

- Applications within the cardholder data environment (CDE)
- Applications processing customer financial information (NPI)
- Public-facing web applications and APIs
- Internal applications processing sensitive data
- Payment processing applications

### 3. Overview

This procedure outlines the security testing requirements for applications in accordance with PCI DSS 6.2, 6.3, and 11.4. It includes automated security scans integrated into the development process and periodic security assessments to identify and remediate vulnerabilities.

### 4. Procedure

#### 4.1 Automated Security Testing (SAST/DAST)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Development Team | Integrates SAST tools into the CI/CD pipeline to scan code for vulnerabilities during development per PCI DSS 6.2.3. |
| **2** | Development Team | Configures DAST tools to scan running applications in staging/test environments. |
| **3** | CI/CD Pipeline (Automated) | Blocks deployment if high/critical vulnerabilities are detected in CDE applications. |
| **4** | Development Team | Reviews security scan reports and addresses high-severity findings before production deployment per PCI DSS 6.2.4. |
| **5** | Development Team | Documents remediation efforts and tracks resolution of identified security issues. |

#### 4.2 Penetration Testing (per PCI DSS 11.4)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Security Team / CISO | Plans annual penetration testing program per PCI DSS 11.4.1, including: |
| | | - Internal penetration testing |
| | | - External penetration testing |
| | | - Network layer testing |
| | | - Application layer testing |
| **2** | Qualified Penetration Tester | Conducts penetration tests using industry-accepted methodologies per PCI DSS 11.4.2. |
| **3** | Qualified Penetration Tester | Tests segmentation controls to verify effectiveness per PCI DSS 11.4.5. |
| **4** | IT Security Team | Reviews penetration test findings and prioritizes remediation based on risk. |
| **5** | Development/IT Team | Implements remediation for identified vulnerabilities within established timeframes. |
| **6** | Qualified Penetration Tester | Retests to verify remediation of exploitable vulnerabilities per PCI DSS 11.4.4. |
| **7** | PCI Program Manager | Documents penetration test results and remediation for PCI DSS compliance evidence. |

#### 4.3 Significant Change Testing

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Development Team | For significant changes to CDE applications, conducts security testing before deployment per PCI DSS 6.3.2. |
| **2** | IT Security Team | Reviews changes for security impact and determines if additional penetration testing is required. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1** | PCI DSS v4.0 | 6.2.3, 6.2.4, 6.3.2 |
| **4.1** | SOC 2 TSC | CC7.1 |
| **4.2** | PCI DSS v4.0 | 11.4.1, 11.4.2, 11.4.3, 11.4.4, 11.4.5 |
| **4.3** | PCI DSS v4.0 | 6.3.2, 11.4.3 |

### 6. Artifact(s)

- SAST/DAST scan reports
- Vulnerability remediation tracking records
- Penetration test reports with methodology and findings
- Remediation verification documentation
- Segmentation validation test results
- PCI DSS compliance evidence package

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **SAST (Static Application Security Testing)** | Analysis of source code to identify security vulnerabilities without executing the code. |
| **DAST (Dynamic Application Security Testing)** | Analysis of running applications to identify vulnerabilities from an external perspective. |
| **Penetration Testing** | Authorized simulated attack on a system to evaluate security by exploiting vulnerabilities. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Development Team** | Implements security scanning, reviews findings, and remediates vulnerabilities in applications. |
| **IT Security Team** | Manages penetration testing program and provides guidance on vulnerability remediation priorities. |
| **Qualified Penetration Tester** | Conducts penetration tests using industry-accepted methodologies per PCI DSS 11.4.1. |
| **PCI Program Manager** | Ensures testing meets PCI DSS requirements and maintains compliance documentation. |

