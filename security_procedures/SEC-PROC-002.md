# Internal ISMS Audit Procedure (SEC-PROC-002)

### 1. Purpose

To outline the process for planning, conducting, and reporting on annual internal audits of the Information Security Management System (ISMS), with enhanced requirements for auditing cardholder data environment (CDE) controls and GLBA Safeguards Rule compliance.

### 2. Scope

This procedure applies to all internal audits of the ISMS, including all systems, processes, and controls that fall under its scope. This includes:

- PCI DSS v4.0 compliance controls
- SOC 2 Trust Services Criteria controls
- GLBA Safeguards Rule controls
- Cardholder data environment (CDE) systems
- Systems processing nonpublic personal information (NPI)

### 3. Overview

This procedure details the end-to-end process for the annual internal audit of the ISMS. It covers the creation of an audit plan, the execution of audit fieldwork, the documentation of findings, the generation of a formal report, and the tracking of corrective actions through to resolution. For fintech organizations, the audit must address PCI DSS 12.10.2 requirements for testing incident response plans and validate controls across all applicable frameworks.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Head of Internal Audit / CISO | Develops and documents an annual internal audit plan, including scope, objectives, resources, and framework coverage (PCI DSS, SOC 2, GLBA). |
| **2** | Head of Internal Audit | Ensures audit plan includes testing of incident response plan per PCI DSS 12.10.2. |
| **3** | Internal Auditor(s) | Conducts audit fieldwork by gathering and analyzing evidence to assess control effectiveness across all frameworks. |
| **4** | Internal Auditor(s) | For CDE systems: Verifies compliance with applicable PCI DSS requirements using the appropriate SAQ or ROC methodology. |
| **5** | Internal Auditor(s) | Documents all findings, including non-conformities, observations, and opportunities for improvement, categorized by framework. |
| **6** | Head of Internal Audit | Creates and distributes a formal audit report detailing the scope, findings, and recommendations. |
| **7** | Management / Process Owners | Develops and implements corrective action plans for identified findings with target remediation dates. |
| **8** | Head of Internal Audit | Tracks the status of all corrective actions to completion in a tracking log. |
| **9** | PCI Program Manager | Reviews CDE-related findings and ensures they are included in the PCI DSS compliance evidence package. |
| **10** | CISO / Qualified Individual | Reports audit results to the Board of Directors per GLBA § 314.4(i). |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC4.1, CC4.2 |
| **1-4** | PCI DSS v4.0 | 12.10.2 |
| **10** | GLBA Safeguards | § 314.4(i) |

### 6. Artifact(s)

- Annual internal audit plan
- Audit fieldwork documentation and evidence
- Final internal audit report
- Corrective action tracking log
- Board reporting documentation (for GLBA)
- PCI DSS compliance evidence package

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **ISMS** | Information Security Management System - the set of policies, processes, and controls that govern information security. |
| **Non-conformity** | A deviation from a policy, procedure, or regulatory requirement that requires corrective action. |
| **Observation** | A finding that does not constitute a non-conformity but represents an opportunity for improvement. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Head of Internal Audit / CISO** | Oversees the entire audit process, from planning to reporting and tracking. Ensures coverage of all applicable frameworks. |
| **Internal Auditor(s)** | Executes the audit plan, documents findings, and assists in report creation. |
| **PCI Program Manager** | Ensures CDE-related audit activities align with PCI DSS requirements and maintains compliance evidence. |
| **Management / Process Owners** | Responsible for implementing corrective actions to address audit findings. |
| **Qualified Individual** | Ensures GLBA-required reporting to the Board is completed. |

