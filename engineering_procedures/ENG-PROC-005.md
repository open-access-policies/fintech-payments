# System Hardening Baseline Procedure (ENG-PROC-005)

### 1. Purpose

To describe the process for applying documented security baselines to new systems and verifying their ongoing compliance to ensure a consistent and secure configuration, with enhanced requirements for systems within or connected to the cardholder data environment (CDE) per PCI DSS 2.2.

### 2. Scope

This procedure applies to all systems including:

- Production servers, virtual machines, and container images
- Systems within the cardholder data environment (CDE)
- Systems processing or transmitting NPI
- Network devices and security appliances
- Payment processing infrastructure

### 3. Overview

This procedure details the steps for system hardening per PCI DSS 2.2. It begins with the provisioning of a new system, followed by the automated application of a security baseline, removal of unnecessary software and services, and concludes with a compliance scan to verify the configuration and detect any drift.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Engineer / Automated System | A new server or service is provisioned using Infrastructure as Code (IaC) templates that incorporate security baseline settings. |
| **2** | Automated Configuration Script | An automated configuration management script applies the documented security baseline per PCI DSS 2.2.1, including: |
| | | - CIS Benchmarks for operating systems |
| | | - PCI DSS hardening standards for CDE systems |
| | | - Vendor security configuration guides |
| **3** | Automated Configuration Script | The script removes or disables unnecessary services, ports, protocols, and software packages to reduce the system's attack surface per PCI DSS 2.2.4 and 2.2.5. |
| **4** | Automated Compliance Tool | A compliance scan is automatically run after provisioning to verify that the baseline was applied correctly and to establish the initial secure state per PCI DSS 2.2.1. |
| **5** | IT Security Team | Periodically runs compliance scans to detect any configuration drift from the established baseline and alerts the system owner if deviations are found. |
| **6** | PCI Program Manager | For CDE systems: Documents baseline configuration and compliance verification for PCI DSS evidence. |

Note: If the security team determines the configuration drift is critical or affects CDE systems, an incident post-mortem may be initiated to analyze the deviation in detail.

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-6** | SOC 2 TSC | CC6.1 |
| **2-5** | PCI DSS v4.0 | 2.2.1, 2.2.4, 2.2.5, 2.2.7 |
| **2, 4** | CIS Controls | Control 4, 5 |

### 6. Artifact(s)

- Compliance scan reports confirming adherence to security baseline
- System configuration documentation
- Baseline deviation reports and remediation records
- PCI DSS configuration standards documentation (for CDE systems)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **CIS Benchmarks** | A set of globally recognized and consensus-developed best practices for the secure configuration of a target system. |
| **Configuration Drift** | The process by which a system's configuration changes over time from its established, secure baseline. |
| **Infrastructure as Code (IaC)** | The management of infrastructure (networks, virtual machines, load balancers, and connection topology) in a descriptive model, using the same versioning as DevOps team uses for source code. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Engineer** | Develops and maintains the Infrastructure as Code templates and automated configuration scripts. |
| **IT Security Team** | Defines the security baselines, manages the compliance scanning tools, and reviews scan reports for deviations. |
| **System Owner** | Is responsible for remediating any configuration drift detected on their systems. |
| **PCI Program Manager** | Ensures CDE system configurations are documented and meet PCI DSS requirements. |

