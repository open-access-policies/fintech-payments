# Risk Management Policy (SEC-POL-003)

## 1. Objective

This policy establishes a comprehensive risk management framework for **[Company Name]** that meets PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that information security risks to the cardholder data environment (CDE), customer financial information, and company information assets are systematically identified, assessed, managed, and reported in accordance with regulatory requirements.

## 2. Scope

This policy applies to all **[Company Name]** workforce members, contractors, and third parties. It encompasses:

- All systems within the cardholder data environment (CDE)
- All systems that store, process, or transmit nonpublic personal information (NPI) under GLBA
- All company information assets, systems, and processes
- Cloud services and remote work environments
- Third-party service providers (TPSPs) with access to cardholder data or customer information

## 3. Policy

**[Company Name]** implements a comprehensive risk management process that meets PCI DSS, SOC 2, and GLBA Safeguards Rule requirements.

### 3.1 Risk Management Framework

**[Company Name]** establishes an effective risk management process in accordance with GLBA § 314.4(b).

- Risk management shall follow a cycle of identification, assessment, treatment, monitoring, and reporting.

- Risk management activities shall be documented consistently using written risk assessments.

- The framework shall be reviewed at least annually and updated as needed to reflect changes to business objectives, the regulatory environment, or risks to the CDE and customer information per PCI DSS 12.1.2.

- Risk considerations shall be integrated into system changes, vendor decisions, and new business initiatives.

- The risk management program shall be evaluated and adjusted in light of testing results, material changes to operations, and any circumstances known to materially impact security per GLBA § 314.4(g).

### 3.2 Risk Identification

**[Company Name]** shall identify information security risks through regular assessment and monitoring per GLBA § 314.4(b).

- A comprehensive written risk assessment shall be conducted at least annually and when significant system changes occur.

- Risk identification shall identify reasonably foreseeable internal and external risks to the security, confidentiality, and integrity of customer information and cardholder data.

- Risk identification shall consider threats including:
  - Cybersecurity threats (malware, phishing, ransomware, unauthorized access)
  - System failures and outages affecting the CDE or customer information systems
  - Human error and insider threats
  - Natural disasters and environmental hazards
  - Third-party and vendor risks
  - Payment fraud and transaction manipulation
  - Data breaches and exfiltration
  - Regulatory and compliance risks

### 3.3 Risk Assessment

All identified risks shall be analyzed using documented criteria per GLBA § 314.4(b)(1).

- Written risk assessments shall include:
  - Criteria for evaluating identified risks
  - Assessment of the sufficiency of existing controls to address identified risks
  - Risk treatment plans for high and medium risks

- Impact assessment shall consider financial, operational, reputational, and regulatory consequences.

- Likelihood assessment shall consider threat capabilities, system vulnerabilities, and existing controls.

- Risk levels shall be categorized as **Critical**, **High**, **Medium**, or **Low** using documented criteria.

- Risk assessments shall be periodically reassessed based on changes to the environment or threat landscape.

### 3.4 Targeted Risk Analysis (PCI DSS)

**[Company Name]** shall perform targeted risk analyses for PCI DSS requirements that allow flexibility in how frequently activities are performed per PCI DSS 12.3.1.

- Targeted risk analysis documentation shall include:
  - Identification of the assets being protected
  - Identification of the threat(s) that the requirement is protecting against
  - Identification of factors that contribute to the likelihood and/or impact of a threat being realized
  - Resulting analysis that determines and justifies how frequently the requirement must be performed
  - Review of each targeted risk analysis at least once every 12 months

- Targeted risk analyses shall be performed for requirements including but not limited to:
  - Application and system account password change frequency (PCI DSS 8.6.3)
  - Firewall and router rule review frequency
  - Vulnerability scan frequency beyond minimum requirements
  - Log review frequency for non-critical systems

### 3.5 Technology Risk Review

Hardware and software technologies in use shall be reviewed at least annually per PCI DSS 12.3.4.

- Technology reviews shall include:
  - Analysis that technologies continue to receive security fixes from vendors promptly
  - Analysis that technologies continue to support PCI DSS compliance
  - Documentation of vendor "end of life" announcements or industry trends
  - A plan approved by senior management to remediate outdated technologies

### 3.6 Cryptographic Risk Review

Cryptographic cipher suites and protocols in use shall be documented and reviewed at least annually per PCI DSS 12.3.3.

- Cryptographic reviews shall include:
  - Up-to-date inventory of all cryptographic cipher suites and protocols in use, including purpose and location
  - Active monitoring of industry trends regarding continued viability
  - Documented strategy to respond to anticipated changes in cryptographic vulnerabilities

### 3.7 Risk Treatment

**[Company Name]** shall implement appropriate responses to identified risks based on their level and business impact.

- Risk treatment options include:
  - **Accept:** Monitor risks within acceptable tolerance levels with documented risk acceptance by appropriate management
  - **Avoid:** Eliminate risk by discontinuing or modifying activities
  - **Mitigate:** Implement controls to reduce likelihood or impact
  - **Transfer:** Share risk through insurance or contracts

- Critical and high risks shall be addressed with priority and escalated to executive management.

- Risk treatment plans shall include specific actions, responsible parties, timelines, and success criteria.

- Controls shall be deployed addressing the risks identified through risk assessment per GLBA § 314.4(c).

### 3.8 Risk Monitoring and Review

**[Company Name]** shall monitor risks and the effectiveness of risk treatments on an ongoing basis per GLBA § 314.4(d).

- A risk register shall be maintained to track identified risks, assessments, treatments, and current status.

- Risk levels shall be reviewed:
  - Monthly for critical risks
  - Quarterly for high risks
  - Semi-annually for medium risks
  - Annually for low risks

- The effectiveness of safeguards' key controls, systems, and procedures shall be regularly tested or monitored per GLBA § 314.4(d)(1).

- Testing shall include continuous monitoring or periodic penetration testing and vulnerability assessments per GLBA § 314.4(d)(2).

- The annual risk assessment shall validate identified risks and assess program effectiveness.

### 3.9 Risk Communication and Reporting

Risk information shall be communicated effectively to support informed decision-making and meet regulatory reporting requirements.

**Management Reporting:**
- Risk reports shall be provided to management in a clear, actionable format.
- Critical risks shall be escalated immediately to appropriate management levels.
- Risk status reports shall be provided to management quarterly.

**Board Reporting (per GLBA § 314.4(i)):**
- The Qualified Individual shall report in writing, regularly and at least annually, to the Board of Directors or equivalent governing body.
- Reports shall include:
  - Overall status of the information security program and compliance
  - Risk assessment results and risk management decisions
  - Service provider arrangements
  - Results of testing and monitoring
  - Security events or violations and management's responses
  - Recommendations for changes in the information security program

### 3.10 Third-Party Risk Management

Risks from third-party service providers shall be assessed and managed per PCI DSS 12.8 and GLBA § 314.4(f).

**Due Diligence (per PCI DSS 12.8.3 and GLBA § 314.4(f)(1)):**
- Security assessments shall be conducted before engaging third parties with access to the CDE or customer information.
- Assessment shall evaluate the TPSP's capability to maintain appropriate safeguards.

**TPSP Inventory (per PCI DSS 12.8.1):**
- A list of all TPSPs with which account data is shared or that could affect CDE security is maintained.
- The list includes a description of services provided by each TPSP.

**Written Agreements (per PCI DSS 12.8.2 and GLBA § 314.4(f)(2)):**
- Written agreements are maintained with all TPSPs.
- Agreements include acknowledgment of TPSP responsibility for security of account data.
- Service providers are contractually required to implement and maintain appropriate safeguards.

**Compliance Monitoring (per PCI DSS 12.8.4 and GLBA § 314.4(f)(3)):**
- TPSP PCI DSS compliance status is monitored at least annually.
- Service providers are periodically assessed based on the risk they present.

**Responsibility Documentation (per PCI DSS 12.8.5):**
- Information is maintained about which PCI DSS requirements are managed by each TPSP.
- Responsibility matrices document requirements managed by the entity, TPSP, or shared.

### 3.11 CDE Scope Validation

PCI DSS scope shall be documented and validated per PCI DSS 12.5.

**Scope Documentation (per PCI DSS 12.5.1):**
- An inventory of system components in scope for PCI DSS is maintained, including description of function/use.

**Annual Scope Validation (per PCI DSS 12.5.2):**
- PCI DSS scope is documented and confirmed at least annually and upon significant change.
- Validation includes:
  - Identifying all data flows for payment stages (authorization, capture, settlement, chargebacks, refunds)
  - Updating data-flow diagrams
  - Identifying all locations where account data is stored, processed, and transmitted
  - Identifying all system components in the CDE, connected to the CDE, or that could impact CDE security
  - Identifying all segmentation controls and justification for out-of-scope environments
  - Identifying all third-party connections to the CDE

### 3.12 Risk Appetite and Tolerance

Executive leadership shall formally document, approve, and annually review the company's risk appetite and tolerance levels.

- Risk appetite defines the level of risk the organization is willing to accept in pursuit of its objectives.

- Risk tolerance defines acceptable variation around risk appetite.

- Risks exceeding tolerance levels require management review and documented risk acceptance or additional treatment.

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 12.1.2 |
| 3.1 | SOC 2 TSC | CC3.1 |
| 3.1 | GLBA Safeguards | § 314.4(b), § 314.4(g) |
| 3.2 | PCI DSS v4.0 | 12.3.1 |
| 3.2 | SOC 2 TSC | CC3.2 |
| 3.2 | GLBA Safeguards | § 314.4(b) |
| 3.3 | PCI DSS v4.0 | 12.3.1 |
| 3.3 | SOC 2 TSC | CC3.2 |
| 3.3 | GLBA Safeguards | § 314.4(b)(1) |
| 3.4 | PCI DSS v4.0 | 12.3.1, 12.3.2 |
| 3.5 | PCI DSS v4.0 | 12.3.4 |
| 3.5 | SOC 2 TSC | CC3.2 |
| 3.6 | PCI DSS v4.0 | 12.3.3 |
| 3.7 | PCI DSS v4.0 | 12.3.1 |
| 3.7 | SOC 2 TSC | CC3.3 |
| 3.7 | GLBA Safeguards | § 314.4(c) |
| 3.8 | PCI DSS v4.0 | 12.3.1 |
| 3.8 | SOC 2 TSC | CC3.4, CC4.1 |
| 3.8 | GLBA Safeguards | § 314.4(d) |
| 3.9 | PCI DSS v4.0 | 12.4.1 |
| 3.9 | SOC 2 TSC | CC2.1 |
| 3.9 | GLBA Safeguards | § 314.4(i) |
| 3.10 | PCI DSS v4.0 | 12.8.1-12.8.5 |
| 3.10 | SOC 2 TSC | CC9.2 |
| 3.10 | GLBA Safeguards | § 314.4(f) |
| 3.11 | PCI DSS v4.0 | 12.5.1, 12.5.2 |
| 3.12 | SOC 2 TSC | CC3.1 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Customer Information** | Any record containing nonpublic personal information about a customer, whether in paper, electronic, or other form (per GLBA). |
| **Inherent Risk** | The level of risk that exists before any controls or mitigation measures are applied. |
| **Key Risk Indicators (KRIs)** | Metrics that provide early warning signals of increasing risk exposure. |
| **Qualified Individual** | The person designated to oversee and implement the information security program per GLBA § 314.4(a). |
| **Residual Risk** | The level of risk remaining after controls and mitigation measures have been applied. |
| **Risk Appetite** | The level of risk that an organization is willing to accept in pursuit of its objectives. |
| **Risk Assessment** | The systematic process of identifying, analyzing, and evaluating risks. |
| **Risk Register** | A document that records identified risks, their analysis, treatments, and current status. |
| **Risk Tolerance** | The acceptable level of variation around risk appetite. |
| **Targeted Risk Analysis** | A PCI DSS-specific risk analysis for requirements that allow flexibility in how frequently activities are performed. |
| **Third-Party Service Provider (TPSP)** | An external entity that stores, processes, transmits, or can impact the security of cardholder data or customer information on behalf of **[Company Name]**. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Board of Directors / Executive Leadership** | Approve risk appetite and tolerance levels. Approve risk treatment strategies for critical and high risks. Receive and review annual reports from the Qualified Individual. Provide resources for risk management activities. |
| **Qualified Individual (per GLBA)** | Oversee the information security program. Report in writing to the Board at least annually on program status and material security matters. |
| **Chief Information Security Officer (CISO)** | Own and maintain the risk management program. Conduct risk assessments and coordinate risk treatment activities. Report risk status to leadership. Ensure PCI DSS and GLBA compliance. |
| **PCI Program Manager** | Manage PCI DSS scope validation. Coordinate annual assessments. Maintain CDE documentation and responsibility matrices with TPSPs. Perform or oversee targeted risk analyses for PCI DSS requirements. |
| **IT Security Team** | Identify technical risks and vulnerabilities. Implement technical risk controls. Conduct penetration testing and vulnerability assessments. Monitor risk indicators and security events. |
| **Business Unit Managers** | Identify business risks within their areas. Participate in risk assessments. Implement assigned risk treatments. Report potential risks and security concerns. |
| **Asset/System Owners** | Assess risks for their assigned assets or systems. Implement and maintain appropriate risk controls. Participate in scope validation activities. |
| **Third-Party Risk Management** | Conduct TPSP due diligence. Maintain TPSP inventory. Monitor TPSP compliance status. Maintain responsibility matrices. |
| **All Workforce Members** | Report potential risks and security concerns. Comply with risk mitigation controls and procedures. Participate in risk identification activities. |

