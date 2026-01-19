# Vendor Security Assessment Procedure (SEC-PROC-005)

### 1. Purpose

To detail the process for assessing a new vendor's security posture before engagement to ensure they meet the company's security requirements, with enhanced due diligence for vendors handling cardholder data (CHD), sensitive authentication data (SAD), or customer financial information (NPI).

### 2. Scope

This procedure applies to all new vendors that will:

- Handle, store, process, or transmit company data
- Be connected to the company's network or systems
- Have access to the cardholder data environment (CDE)
- Process, store, or transmit cardholder data on behalf of the company
- Handle customer financial information (NPI)

Third-party service providers (TPSPs) with access to cardholder data are subject to enhanced requirements per PCI DSS 12.8.

### 3. Overview

This procedure outlines the steps for conducting due diligence on prospective vendors. It includes initiating the request, classifying the vendor's risk level, performing a security assessment tailored to that risk level, and obtaining formal approval before a contract is signed. For vendors handling CHD or NPI, additional due diligence and contractual requirements apply.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Business Owner | Initiates a new vendor request and provides details about the services, data involved, and whether CHD, SAD, or NPI will be accessed. |
| **2** | IT Security Team | Classifies the vendor's inherent risk level: |
| | | - **Critical:** Access to CHD, SAD, or payment systems |
| | | - **High:** Access to NPI or CDE-connected systems |
| | | - **Medium:** Access to internal/confidential data |
| | | - **Low:** No access to sensitive data |
| **3** | IT Security Team | Performs due diligence activities based on risk level: |
| | | - **Critical/High:** SOC 2 Type II report review, PCI DSS AOC (if applicable), security questionnaire, technical assessment |
| | | - **Medium:** Security questionnaire, SOC 2 report review |
| | | - **Low:** Security questionnaire |
| **4** | PCI Program Manager | For vendors with CHD access: Verifies PCI DSS compliance status per PCI DSS 12.8.4 and obtains current Attestation of Compliance (AOC). |
| **5** | IT Security Team | Documents findings in a Vendor Risk Assessment Report and provides a recommendation. |
| **6** | Business Owner / CISO | Reviews the assessment report and formally approves or denies the vendor engagement. |
| **7** | Legal / Procurement | Ensures contract includes required security provisions: |
| | | - Data protection requirements |
| | | - TPSP acknowledgment of responsibility for CHD security (per PCI DSS 12.8.2) |
| | | - Incident notification requirements |
| | | - Right to audit |
| | | - Compliance with applicable regulations |
| **8** | IT Security Team | Adds approved vendor to the TPSP inventory per PCI DSS 12.8.1. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC9.2 |
| **2-5, 8** | PCI DSS v4.0 | 12.8.1, 12.8.2, 12.8.3, 12.8.4, 12.8.5 |
| **3-7** | GLBA Safeguards | § 314.4(f) |

### 6. Artifact(s)

- Vendor request form with service and data details
- Vendor Risk Assessment Report
- PCI DSS Attestation of Compliance (AOC) for CHD vendors
- SOC 2 Type II report (for high/critical vendors)
- Completed security questionnaire
- Executed contract with security provisions
- Updated TPSP inventory

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Third-Party Service Provider (TPSP)** | An external entity that stores, processes, transmits, or can impact the security of cardholder data or customer information on behalf of the company. |
| **SOC 2 Report** | A report on controls at a service organization relevant to security, availability, processing integrity, confidentiality, or privacy. |
| **Attestation of Compliance (AOC)** | A document provided by a PCI DSS compliant entity confirming their compliance status. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Business Owner** | Initiates the vendor request and acts as the primary point of contact for the vendor relationship. |
| **IT Security Team** | Conducts the risk classification and due diligence assessment, produces the final report, and maintains the TPSP inventory. |
| **PCI Program Manager** | Verifies PCI DSS compliance for vendors with CHD access and maintains compliance evidence. |
| **CISO** | Provides final approval for vendor engagement based on the risk assessment findings. |
| **Legal / Procurement** | Ensures contracts include required security and compliance provisions. |

