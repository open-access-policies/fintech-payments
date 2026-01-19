# Third-Party Service Provider Compliance Monitoring Procedure (PAY-PROC-006)

### 1. Purpose

To define the process for monitoring PCI DSS compliance status of third-party service providers (TPSPs) that store, process, or transmit cardholder data or could impact the security of the CDE per PCI DSS 12.8 and 12.9.

### 2. Scope

This procedure applies to all third-party service providers including:

- Payment processors and gateways
- Hosting providers for CDE systems
- Tokenization service providers
- Managed security service providers
- Cloud service providers hosting CHD
- Any other entity with CHD access or CDE connectivity

### 3. Overview

This procedure establishes the annual and ongoing monitoring workflow for TPSP PCI DSS compliance per PCI DSS 12.8.4. It covers obtaining compliance evidence, reviewing shared responsibilities, and addressing compliance gaps to ensure continuous protection of cardholder data.

### 4. Procedure

#### 4.1 TPSP Inventory Maintenance

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Reviews and updates the TPSP inventory at least annually, including: |
| | | - Service provider name and contact |
| | | - Services provided |
| | | - CHD/CDE access type |
| | | - Compliance requirements applicable |
| | | - Agreement effective dates |
| **2** | PCI Program Manager | Identifies new TPSPs added during the year. |
| **3** | PCI Program Manager | Removes TPSPs no longer in use (verify CHD access terminated). |
| **4** | PCI Program Manager | Confirms each TPSP is documented per PCI DSS 12.8.1. |

#### 4.2 Annual Compliance Evidence Collection

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Initiates annual compliance review process **[Number, e.g., 60]** days before AOC expiration. |
| **2** | PCI Program Manager | Requests current compliance evidence from each TPSP: |
| | | - Attestation of Compliance (AOC) |
| | | - Service Provider compliance certificate |
| | | - SOC 2 Type II report (if applicable) |
| **3** | PCI Program Manager | Verifies received documentation: |
| | | - AOC is current (not expired) |
| | | - Scope of AOC covers services provided |
| | | - No significant compliance gaps noted |
| | | - Entity name matches contracted provider |
| **4** | PCI Program Manager | Documents verification in TPSP compliance tracker. |

#### 4.3 Responsibility Matrix Review

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Reviews the shared responsibility matrix (per PCI DSS 12.9.2) for each TPSP. |
| **2** | PCI Program Manager | Confirms matrix documents which PCI DSS requirements are: |
| | | - Fully managed by TPSP |
| | | - Shared between **[Company Name]** and TPSP |
| | | - Fully managed by **[Company Name]** |
| **3** | PCI Program Manager | Verifies **[Company Name]** controls are in place for shared and company-managed requirements. |
| **4** | IT Security Team | Validates technical controls align with responsibility matrix. |
| **5** | PCI Program Manager | Updates responsibility matrix if service changes have occurred. |

#### 4.4 Compliance Gap Remediation

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | If TPSP cannot provide current AOC or compliance evidence: |
| | | - Requests explanation and timeline for compliance |
| | | - Assesses risk of continued use |
| | | - Documents compensating controls in place |
| **2** | PCI Program Manager | Escalates non-compliant TPSPs to CISO for risk decision. |
| **3** | CISO | Determines action: |
| | | - Accept risk with compensating controls |
| | | - Require TPSP remediation by deadline |
| | | - Terminate relationship and migrate to compliant provider |
| **4** | Legal/Procurement | Enforces contractual compliance requirements if needed. |

#### 4.5 Ongoing Monitoring

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Monitors for TPSP security incidents through: |
| | | - Vendor security notifications |
| | | - Industry news and alerts |
| | | - Payment brand notifications |
| **2** | PCI Program Manager | If TPSP reports a security incident: |
| | | - Determines potential impact on **[Company Name]** CHD |
| | | - Coordinates with TPSP on investigation |
| | | - Initiates incident response if **[Company Name]** data is affected |
| **3** | IT Security Team | Reviews TPSP connection security periodically: |
| | | - Network connectivity review |
| | | - Credential/access review |
| | | - Configuration validation |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1** | PCI DSS v4.0 | 12.8.1 |
| **4.2** | PCI DSS v4.0 | 12.8.4 |
| **4.3** | PCI DSS v4.0 | 12.9.2 |
| **4.4, 4.5** | PCI DSS v4.0 | 12.8.5 |
| **4.1-4.5** | SOC 2 TSC | CC9.2 |
| **4.1-4.5** | GLBA Safeguards | § 314.4(d) |

### 6. Artifact(s)

- TPSP inventory list
- Current AOC for each TPSP
- Responsibility matrices (per PCI DSS 12.9.2)
- Compliance verification documentation
- Risk acceptance records (if applicable)
- TPSP incident communication records

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Attestation of Compliance (AOC)** | A form for merchants and service providers to attest to the results of a PCI DSS assessment. |
| **Responsibility Matrix** | A document that specifies which PCI DSS requirements are managed by the TPSP, the entity, or shared between both. |
| **Third-Party Service Provider (TPSP)** | A business entity that provides services involving the storing, processing, or transmitting of CHD on behalf of another entity. |
| **Service Provider** | In PCI DSS, a business entity that is not a payment brand and provides services directly involving processing, storing, or transmitting CHD. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **PCI Program Manager** | Maintain TPSP inventory, collect compliance evidence, review responsibility matrices, track compliance status. |
| **IT Security Team** | Validate TPSP technical controls, review connection security, support incident response. |
| **CISO** | Approve risk decisions for non-compliant TPSPs, oversee TPSP security requirements. |
| **Legal/Procurement** | Include PCI DSS requirements in TPSP contracts, enforce compliance obligations. |
| **Business Owners** | Identify new TPSPs, notify PCI Program Manager of service changes, support compliance reviews. |

