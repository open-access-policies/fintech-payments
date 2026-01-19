# Vulnerability Management Procedure (SEC-PROC-008)

### 1. Purpose

To describe the workflow for identifying, prioritizing, remediating, and verifying vulnerabilities across the organization's systems and applications, with enhanced requirements for cardholder data environment (CDE) systems per PCI DSS Requirement 6 and 11.

### 2. Scope

This procedure applies to all company-owned or managed systems, networks, and applications, including:

- All systems within the cardholder data environment (CDE)
- Systems connected to the CDE
- Systems processing customer financial information (NPI)
- Web applications and APIs
- Internal and external network infrastructure
- Cloud resources

### 3. Overview

This procedure outlines the systematic process for managing vulnerabilities in accordance with PCI DSS 6.3 and 11.3. It begins with the discovery of vulnerabilities through various means, followed by prioritization based on risk. It then details the assignment of remediation tasks to asset owners, the remediation process itself, and the final verification by the Security Team to confirm the fix.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Security Team | Discovers vulnerabilities through: |
| | | - Internal vulnerability scans (at least quarterly and after significant changes per PCI DSS 11.3.1) |
| | | - External vulnerability scans by ASV (at least quarterly per PCI DSS 11.3.2) |
| | | - Penetration tests (at least annually per PCI DSS 11.4) |
| | | - Vendor security advisories |
| | | - Threat intelligence feeds |
| **2** | IT Security Team | Prioritizes identified vulnerabilities using: |
| | | - CVSS scores (Critical: 9.0+, High: 7.0-8.9, Medium: 4.0-6.9, Low: 0.1-3.9) |
| | | - Exploitability and threat intelligence |
| | | - Asset criticality (CDE systems receive highest priority) |
| | | - Business context and impact |
| **3** | IT Security Team | Creates remediation tickets and assigns to appropriate asset owners with SLAs: |
| | | - **Critical (CVSS 9.0+):** 24 hours for CDE, 72 hours for non-CDE |
| | | - **High (CVSS 7.0-8.9):** 7 days for CDE, 14 days for non-CDE |
| | | - **Medium (CVSS 4.0-6.9):** 30 days |
| | | - **Low (CVSS 0.1-3.9):** 90 days |
| **4** | Asset Owner | Performs remediation actions to fix the vulnerability within the specified SLA. |
| **5** | IT Security Team | Performs verification scans to confirm successful remediation per PCI DSS 11.3.1.3. |
| **6** | IT Security Team | Closes the finding in the vulnerability tracking system upon successful verification. |
| **7** | PCI Program Manager | For CDE vulnerabilities: Documents remediation for compliance evidence and ensures high-risk and critical vulnerabilities are addressed per PCI DSS 6.3.3. |

**Exception Process:** If remediation cannot be completed within SLA, follow SEC-PROC-009 (Remediation Exception Procedure).

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1** | PCI DSS v4.0 | 11.3.1, 11.3.2, 11.4.1 |
| **2-3** | PCI DSS v4.0 | 6.3.1, 6.3.3 |
| **4-6** | PCI DSS v4.0 | 6.3.3, 11.3.1.3 |
| **1-6** | SOC 2 TSC | CC7.1 |

### 6. Artifact(s)

- Vulnerability scan reports (internal and ASV)
- Penetration test reports
- Remediation tickets with SLA tracking
- Verification scan results
- Vulnerability tracking system records
- Exception documentation (if applicable)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **CVSS** | Common Vulnerability Scoring System - a standard for assessing the severity of security vulnerabilities. |
| **ASV** | Approved Scanning Vendor - a company approved by PCI SSC to conduct external vulnerability scans. |
| **SLA** | Service Level Agreement - a commitment defining the timeframe for remediation. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **IT Security Team** | Responsible for discovering, prioritizing, assigning, and verifying vulnerabilities. Maintains vulnerability tracking system. |
| **Asset Owner** | Responsible for remediating identified vulnerabilities on their assigned assets within the defined SLAs. |
| **PCI Program Manager** | Ensures CDE vulnerability management meets PCI DSS requirements and maintains compliance evidence. |
| **CISO** | Approves exceptions to remediation SLAs and reviews vulnerability metrics. |

