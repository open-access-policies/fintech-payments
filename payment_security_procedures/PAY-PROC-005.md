# ASV Vulnerability Scanning Procedure (PAY-PROC-005)

### 1. Purpose

To define the process for conducting quarterly external vulnerability scans using an Approved Scanning Vendor (ASV) as required by PCI DSS 11.3.2, ensuring that all external-facing systems within the CDE scope are scanned and passing results are maintained.

### 2. Scope

This procedure applies to:

- All external IP addresses and domain names within PCI DSS scope
- All public-facing web applications and APIs in the CDE
- All external network perimeter systems
- Quarterly ASV scan scheduling and execution

### 3. Overview

This procedure establishes the workflow for quarterly ASV vulnerability scanning per PCI DSS 11.3.2. It covers scope definition, scan execution, result review, remediation of identified vulnerabilities, and rescanning to achieve passing results.

### 4. Procedure

#### 4.1 Scan Preparation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Schedules quarterly ASV scan at least **[Number, e.g., 6]** weeks before quarter end. |
| **2** | IT Security Team | Reviews and updates the list of external IP addresses and domains in scope. |
| **3** | IT Security Team | Confirms the scope includes: |
| | | - All external-facing CDE systems |
| | | - All public-facing payment-related applications |
| | | - Perimeter network devices |
| | | - Any recently added external assets |
| **4** | IT Operations Team | Notifies relevant teams of scheduled scan window. |
| **5** | PCI Program Manager | Provides updated scope to the ASV. |

#### 4.2 Scan Execution

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | ASV | Conducts external vulnerability scan per PCI SSC ASV Program Guide. |
| **2** | IT Operations Team | Monitors systems during scan for any operational issues. |
| **3** | ASV | Generates scan report upon completion. |
| **4** | PCI Program Manager | Receives and reviews scan report. |

#### 4.3 Result Review and Classification

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Security Team | Reviews all identified vulnerabilities, classifying each as: |
| | | - Confirmed vulnerability requiring remediation |
| | | - False positive requiring dispute |
| | | - Out-of-scope finding |
| **2** | IT Security Team | For each confirmed vulnerability, documents: |
| | | - CVSS score and severity |
| | | - Affected systems |
| | | - Remediation plan and timeline |
| | | - Owner assignment |
| **3** | IT Security Team | For potential false positives, prepares documentation for ASV dispute. |

#### 4.4 Remediation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | System/Application Owners | Implement remediation for confirmed vulnerabilities per assigned timeline: |
| | | - Critical (CVSS 9.0+): Within **[Number, e.g., 7]** days |
| | | - High (CVSS 7.0-8.9): Within **[Number, e.g., 30]** days |
| | | - Medium (CVSS 4.0-6.9): Within **[Number, e.g., 30]** days (or before quarter end) |
| **2** | IT Security Team | Verifies remediation through internal testing. |
| **3** | PCI Program Manager | Tracks remediation progress and escalates delays. |

#### 4.5 Rescanning and Dispute Resolution

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Submits any false positive disputes to ASV with supporting documentation. |
| **2** | ASV | Reviews disputes and updates findings as appropriate. |
| **3** | PCI Program Manager | Schedules rescan after remediation is complete. |
| **4** | ASV | Conducts rescan of previously vulnerable systems. |
| **5** | IT Security Team | Reviews rescan results to confirm vulnerabilities are resolved. |
| **6** | Process repeats until a passing scan is achieved | |

#### 4.6 Documentation and Attestation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | ASV | Generates final passing scan report and attestation. |
| **2** | PCI Program Manager | Reviews and accepts the ASV scan attestation. |
| **3** | PCI Program Manager | Archives scan reports, remediation records, and attestation for PCI DSS evidence. |
| **4** | PCI Program Manager | Confirms passing scan achieved before quarter end. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1-4.6** | PCI DSS v4.0 | 11.3.2 |
| **4.4** | PCI DSS v4.0 | 6.3.3 |
| **4.1-4.6** | PCI SSC | ASV Program Guide |
| **4.1-4.6** | SOC 2 TSC | CC7.1 |

### 6. Artifact(s)

- ASV scan reports (all scans including rescans)
- Passing scan attestation
- Scope documentation
- False positive dispute documentation
- Remediation tickets and evidence
- Quarterly scan schedule

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Approved Scanning Vendor (ASV)** | An organization approved by PCI SSC to conduct external vulnerability scanning services per PCI DSS requirements. |
| **CVSS** | Common Vulnerability Scoring System - a standard for assessing the severity of security vulnerabilities. |
| **False Positive** | A vulnerability finding that, upon investigation, is determined not to represent an actual security weakness. |
| **Passing Scan** | An ASV scan that contains no vulnerabilities with CVSS 4.0 or higher (after addressing any disputes). |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **PCI Program Manager** | Schedule scans, coordinate with ASV, track remediation, maintain documentation. |
| **IT Security Team** | Define scope, review results, classify findings, verify remediation. |
| **IT Operations Team** | Notify stakeholders, monitor during scans, support remediation. |
| **System/Application Owners** | Remediate vulnerabilities on their systems within required timeframes. |
| **ASV** | Conduct scans per PCI SSC guidelines, provide reports and attestations. |

