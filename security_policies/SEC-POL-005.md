# Third-Party Service Provider Management Policy (SEC-POL-005)

## 1. Objective

This policy establishes requirements for assessing, managing, and monitoring security risks associated with third-party service providers (TPSPs) in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that **[Company Name]** maintains appropriate oversight of external parties who access, process, store, or transmit cardholder data or customer financial information.

## 2. Scope

This policy applies to all **[Company Name]** workforce members involved in TPSP selection, contract negotiation, or ongoing management. It encompasses:

- All TPSPs that store, process, or transmit cardholder data on behalf of **[Company Name]**
- All TPSPs that could affect the security of the cardholder data environment (CDE)
- All service providers with access to customer financial information (NPI)
- All vendors, consultants, and contractors with access to **[Company Name]** information systems

This policy covers the entire TPSP lifecycle from initial assessment through contract termination.

## 3. Policy

**[Company Name]** implements a TPSP risk management program that meets PCI DSS, SOC 2, and GLBA requirements to ensure all third-party relationships maintain appropriate security controls.

### 3.1 TPSP Inventory

A list of all TPSPs is maintained per PCI DSS 12.8.1.

**Inventory Requirements:**
- All TPSPs with which account data is shared are documented
- All TPSPs that could affect the security of account data are documented
- The list includes a description of the services provided by each TPSP
- The inventory is reviewed and updated at least annually

**Inventory Contents:**
- TPSP name and contact information
- Description of services provided
- Type of data accessed (CHD, NPI, etc.)
- Risk classification
- PCI DSS compliance status and validation date
- Contract effective date and renewal date

### 3.2 TPSP Classification and Risk Assessment

All TPSPs are classified based on their risk level and subject to appropriate due diligence per GLBA § 314.4(f)(1).

**Risk Classifications:**

**High Risk:**
- TPSPs with access to the CDE or cardholder data
- Payment processors, gateways, and acquirers
- Cloud service providers hosting CDE systems
- TPSPs with privileged access to systems

**Medium Risk:**
- TPSPs with access to customer financial information (NPI)
- TPSPs providing business-critical services
- TPSPs with access to Internal data

**Low Risk:**
- TPSPs with limited access to Internal data
- TPSPs with no direct system access
- TPSPs providing non-critical services

**Pre-Engagement Risk Assessment:**

**High-Risk TPSP Requirements:**
- Comprehensive security questionnaire
- PCI DSS compliance validation (AOC/ROC)
- SOC 2 Type II report or equivalent
- Financial stability assessment
- Cyber insurance verification

**Medium-Risk TPSP Requirements:**
- Standard security questionnaire
- SOC 2 or ISO 27001 certification
- Financial stability review
- Insurance verification

**Low-Risk TPSP Requirements:**
- Basic security questionnaire
- General insurance verification

### 3.3 Written Agreements

Written agreements are maintained with all TPSPs per PCI DSS 12.8.2 and GLBA § 314.4(f)(2).

**Essential Agreement Provisions:**
- Acknowledgment of TPSP responsibility for the security of account data the TPSP possesses or otherwise stores, processes, or transmits on behalf of **[Company Name]**
- Requirement to implement and maintain appropriate safeguards for customer information per GLBA
- Data protection and confidentiality requirements
- Incident notification and response procedures with defined timeframes
- Right to audit and conduct security assessments
- Compliance with applicable laws and regulations
- Requirement for secure data return or destruction upon contract termination

**Additional High-Risk TPSP Provisions:**
- Specific security control requirements (encryption, access controls, logging)
- PCI DSS compliance maintenance requirements
- Breach notification procedures with specific timelines (typically 24-72 hours)
- Subcontractor approval and oversight requirements
- Business continuity and disaster recovery provisions
- Right to terminate for security violations

### 3.4 PCI DSS Compliance Monitoring

TPSP PCI DSS compliance status is monitored at least annually per PCI DSS 12.8.4.

**Compliance Validation:**
- Obtain and review Attestation of Compliance (AOC) annually
- Verify compliance level is appropriate for services provided
- Document the date compliance was confirmed
- Track compliance validation expiration dates

**Non-Compliant TPSPs:**
- TPSPs with lapsed compliance are flagged for immediate review
- Risk assessment is updated to reflect compliance status
- Remediation timeline is obtained from TPSP
- Alternative providers are identified if compliance cannot be restored

### 3.5 PCI DSS Responsibility Documentation

Information is maintained about which PCI DSS requirements are managed by each TPSP per PCI DSS 12.8.5.

**Responsibility Matrix:**
- Document which requirements are managed by the entity
- Document which requirements are managed by each TPSP
- Document shared responsibilities
- Update responsibility matrices when services or scope changes

**Service-Level Documentation:**
For each TPSP, document:
- System components in scope
- PCI DSS requirements the TPSP is responsible for meeting
- Requirements the TPSP supports but does not fully manage
- How compliance is validated

### 3.6 Ongoing TPSP Assessment

TPSPs are periodically assessed based on the risk they present and the continued adequacy of their safeguards per GLBA § 314.4(f)(3).

**Continuous Monitoring:**
- Annual security questionnaire updates for High-risk TPSPs
- Review of updated security certifications and assessment reports
- Monitoring of TPSP security incidents and breach notifications
- Performance and service level monitoring
- Compliance with contractual security requirements

**Periodic Assessments:**
- High-Risk TPSPs: Annual security assessment
- Medium-Risk TPSPs: Assessment every two years or upon contract renewal
- Low-Risk TPSPs: Assessment upon contract renewal

### 3.7 TPSP Access Management

Access granted to TPSPs is controlled and monitored per PCI DSS 8.2.3 and 8.2.7.

**Access Provisioning:**
- Formal approval is required by the business owner and **[Role Title, e.g., CISO]**
- Access is limited to the minimum necessary to perform contracted services
- TPSP personnel are individually identified and authenticated
- MFA is required for High-risk TPSP access

**Account Management (per PCI DSS 8.2.7):**
- Accounts used by TPSPs for remote access are:
  - Enabled only during the time period needed
  - Disabled when not in use
  - Monitored for unexpected activity

**Service Provider Authentication (per PCI DSS 8.2.3):**
- Service providers with remote access to customer premises use unique authentication factors for each customer

**Access Review:**
- All TPSP access is logged and monitored
- Access reviews are conducted at least every six months for TPSPs with CDE access
- Access is promptly revoked upon contract termination or personnel changes

### 3.8 TPSP Incident Management

TPSPs notify **[Company Name]** of security incidents per contractual requirements.

**Notification Requirements:**
- TPSPs report security incidents within contractually specified timeframes
- **[Company Name]** assesses the impact of TPSP incidents on company operations and data
- Incident response coordination with TPSPs follows documented procedures

**Incident Response:**
- TPSP incidents involving cardholder data or customer information are escalated immediately
- Coordination with TPSPs follows the Incident Response Policy (RES-POL-001)
- Post-incident reviews include assessment of TPSP security controls

### 3.9 Cloud Service Provider Management

Cloud service providers are subject to enhanced security requirements.

**Cloud Provider Requirements:**
- PCI DSS compliance for cloud services processing or storing cardholder data
- SOC 2 Type II certification or equivalent (ISO 27001)
- Data encryption at rest and in transit
- Geographic data location controls where required
- Incident response and breach notification procedures
- Business continuity and disaster recovery capabilities

**Shared Responsibility:**
- Cloud shared responsibility model is documented
- **[Company Name]** responsibilities versus provider responsibilities are clearly defined
- Customer-managed encryption keys (CMEK) are used for sensitive data

### 3.10 Subcontractor Management

TPSPs obtain approval before engaging subcontractors for services involving **[Company Name]** data.

- Written approval is required before engaging subcontractors
- Subcontractors are subject to the same security requirements as primary TPSPs
- TPSPs maintain oversight of subcontractor security practices
- Notification is required for subcontractor changes or incidents

### 3.11 TPSP Offboarding

Formal processes ensure secure termination of TPSP relationships.

**Offboarding Process:**
1. Access revocation and account deactivation
2. Data return or secure destruction verification
3. Equipment and credential return
4. Final security assessment and documentation
5. Contract closure and relationship termination

**Data Handling:**
- Confirmation that TPSP has securely deleted or returned all cardholder data and customer information
- Certificate of destruction obtained where applicable
- Verification that no data copies are retained by TPSP

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 12.8.1 |
| 3.2 | PCI DSS v4.0 | 12.8.3 |
| 3.2 | SOC 2 TSC | CC9.2 |
| 3.2 | GLBA Safeguards | § 314.4(f)(1) |
| 3.3 | PCI DSS v4.0 | 12.8.2 |
| 3.3 | SOC 2 TSC | CC9.2 |
| 3.3 | GLBA Safeguards | § 314.4(f)(2) |
| 3.4 | PCI DSS v4.0 | 12.8.4 |
| 3.5 | PCI DSS v4.0 | 12.8.5 |
| 3.6 | PCI DSS v4.0 | 12.8.4 |
| 3.6 | GLBA Safeguards | § 314.4(f)(3) |
| 3.7 | PCI DSS v4.0 | 8.2.3, 8.2.7 |
| 3.7 | SOC 2 TSC | CC6.3 |
| 3.8 | PCI DSS v4.0 | 12.10.1 |
| 3.8 | GLBA Safeguards | § 314.4(h) |
| 3.9 | PCI DSS v4.0 | 12.8.2, 12.8.4 |
| 3.9 | SOC 2 TSC | CC9.2 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Attestation of Compliance (AOC)** | Document signed by a Qualified Security Assessor (QSA) or Internal Security Assessor (ISA) attesting to PCI DSS compliance status. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Customer Information** | Any record containing nonpublic personal information about a customer, whether in paper, electronic, or other form (per GLBA). |
| **Customer-Managed Encryption Keys (CMEK)** | Encryption keys that are created and managed by the customer within cloud provider key management services. |
| **Due Diligence** | The investigation or exercise of care that a reasonable business is expected to take before entering into an agreement. |
| **Responsibility Matrix** | A document that identifies which PCI DSS requirements are managed by **[Company Name]**, the TPSP, or shared. |
| **Service Level Agreement (SLA)** | A contract that defines the level of service expected from a service provider. |
| **Subcontractor** | An entity engaged by a TPSP to perform functions or activities on behalf of the TPSP. |
| **Third-Party Service Provider (TPSP)** | An external entity that stores, processes, transmits, or can impact the security of cardholder data or customer information on behalf of **[Company Name]**. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own TPSP security policy. Approve High-risk TPSP engagements. Oversee TPSP security compliance monitoring. |
| **PCI Program Manager** | Maintain TPSP inventory. Collect and review PCI DSS compliance documentation. Maintain responsibility matrices. Coordinate annual TPSP compliance reviews. |
| **Third-Party Risk Management** | Conduct TPSP due diligence and risk assessments. Perform ongoing security monitoring. Manage TPSP onboarding and offboarding. |
| **Legal/Contracts Team** | Negotiate security contract provisions. Ensure legal and regulatory compliance. Manage contract lifecycle. |
| **Business Owners** | Define business requirements. Approve TPSP selections. Monitor service delivery performance. Report TPSP security concerns. |
| **IT Security Team** | Implement technical controls for TPSP access. Monitor TPSP system activity. Manage TPSP integrations. Coordinate TPSP incident response. |
| **All Workforce Members** | Report TPSP security concerns. Comply with TPSP interaction policies. Protect company information shared with TPSPs. |

