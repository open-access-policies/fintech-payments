# Secure Development Policy (ENG-POL-001)

## 1. Objective

This policy establishes comprehensive security requirements for software development at **[Company Name]** in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures security controls are integrated into development processes to protect cardholder data, customer financial information, and company information systems throughout the software development lifecycle.

## 2. Scope

This policy applies to all **[Company Name]** workforce members involved in software development, including developers, testers, DevOps personnel, and contractors. It covers:

- All bespoke and custom software used on any system component included in or connected to the cardholder data environment (CDE)
- All software that transmits, accesses, or stores customer financial information
- All software development projects including new applications, system modifications, and third-party integrations
- All environments (development, testing, staging, production)
- All payment page scripts loaded and executed in consumer browsers

## 3. Policy

**[Company Name]** implements security principles throughout the software development lifecycle to ensure applications and systems are built with appropriate security controls per PCI DSS Requirement 6, GLBA § 314.4(c)(4), and SOC 2 CC8.1.

### 3.1 Security by Design

Security shall be integrated throughout all phases of software development per PCI DSS 6.2.1.

- Bespoke and custom software is developed securely:
  - Based on industry standards and best practices for secure development
  - In accordance with PCI DSS requirements (including secure authentication and logging)
  - Incorporating consideration of information security issues during each stage of the software development lifecycle

- **Security Requirements:** Security considerations shall be identified and documented for all applications that handle cardholder data or customer financial information based on the Data Classification and Handling Policy (SEC-POL-004).

- **Threat Modeling:** Development teams shall perform threat modeling for applications handling cardholder data, customer financial information, or other Confidential data.

- **Secure Architecture:** Applications shall be designed with security principles including defense in depth, least privilege, fail-safe defaults, and secure by default configurations.

### 3.2 Common Software Attack Prevention

Software engineering techniques shall be used to prevent or mitigate common software attacks per PCI DSS 6.2.4.

Development personnel shall use defined methods to prevent or mitigate the following attacks:

- **Injection Attacks:** SQL, LDAP, XPath, command, parameter, object, fault, or other injection-type flaws

- **Data Structure Attacks:** Attempts to manipulate buffers, pointers, input data, or shared data

- **Cryptography Attacks:** Attempts to exploit weak, insecure, or inappropriate cryptographic implementations, algorithms, cipher suites, or modes of operation

- **Business Logic Attacks:** Attempts to abuse or bypass application features through manipulation of APIs, communication protocols, client-side functionality, or other application functions. This includes cross-site scripting (XSS) and cross-site request forgery (CSRF)

- **Access Control Attacks:** Attempts to bypass or abuse identification, authentication, or authorization mechanisms

- **High-Risk Vulnerabilities:** Any vulnerabilities identified as high-risk in the vulnerability identification process per Section 3.6

### 3.3 Code Review and Quality

All bespoke and custom software shall be reviewed prior to release to production per PCI DSS 6.2.3.

- **Peer Review:** All code changes shall be reviewed by at least one qualified team member before deployment to production.

- **Security Focus:** Code reviews shall:
  - Ensure code is developed according to secure coding guidelines
  - Look for both existing and emerging software vulnerabilities
  - Verify appropriate corrections are implemented prior to release

- **Review Content:** Code reviews shall include consideration of:
  - Searching for undocumented features, implant tools, or backdoors
  - Confirming secure use of external components (libraries, frameworks, APIs)
  - Checking for correct use of logging to prevent sensitive data in logs
  - Analysis of insecure code structures related to common software attacks
  - Checking application behavior for logical vulnerabilities

- **Documentation:** Review approvals and any identified issues shall be documented in the version control system.

### 3.4 Automated Security Integration

All code shall undergo automated security scanning before deployment to production per GLBA § 314.4(c)(4).

- **Continuous Security Testing:** Automated security scanning tools shall be integrated into the CI/CD pipeline to identify vulnerabilities early in development.

- **Build Failure on Critical Issues:** The build process shall fail if critical or high-severity security vulnerabilities are detected, preventing insecure code from reaching production.

- **Tool Maintenance:** Security scanning tools shall be kept current with the latest vulnerability signatures and detection capabilities.

- **Scanning Types:** Automated scanning shall include:
  - Static Application Security Testing (SAST)
  - Software Composition Analysis (SCA) for third-party components
  - Secret scanning for credentials and API keys
  - Container security scanning where applicable

### 3.5 Security Training

Software development personnel shall receive security training per PCI DSS 6.2.2.

- Training is required at least once every 12 months for all personnel working on bespoke and custom software.

- Training shall include:
  - Software security relevant to job function and development languages
  - Secure software design and secure coding techniques
  - Use of security testing tools for detecting vulnerabilities in software
  - Prevention of common software attacks per Section 3.2
  - PCI DSS requirements relevant to software development

- **Initial Training:** New development team members shall receive secure coding training within **[Number, e.g., 30]** days of starting.

- **Training Records:** Completion of security training is tracked and documented.

### 3.6 Vulnerability Management

Security vulnerabilities shall be identified and managed per PCI DSS 6.3.

- **Vulnerability Identification (per PCI DSS 6.3.1):**
  - New security vulnerabilities are identified using industry-recognized sources, including alerts from CERTs
  - Vulnerabilities are assigned risk rankings based on industry best practices and potential impact
  - Risk rankings identify all vulnerabilities considered high-risk or critical to the environment
  - Vulnerabilities in bespoke/custom software and third-party software are covered

- **Patch Management (per PCI DSS 6.3.3):**
  - Critical or high-security patches are installed within one month of release
  - All other applicable security patches are installed within three months of release
  - Exceptions require documented risk acceptance by appropriate management

### 3.7 Third-Party Component Security

Third-party libraries and components shall be managed to minimize security risks per PCI DSS 6.3.2.

- **Software Inventory:** An inventory of bespoke and custom software, and third-party software components incorporated into bespoke and custom software, is maintained to facilitate vulnerability and patch management.

- **Vulnerability Assessment:** Third-party components shall be regularly scanned for known security vulnerabilities using automated Software Composition Analysis (SCA) tools.

- **Update Management:** Third-party components with known security vulnerabilities shall be updated promptly or replaced with secure alternatives per the patch management timelines in Section 3.6.

- **Component Approval:** New third-party components shall be reviewed for security before incorporation into applications.

### 3.8 Public-Facing Web Application Security

Public-facing web applications shall be protected against attacks per PCI DSS 6.4.

**Application Security Assessment (per PCI DSS 6.4.1):**
- Public-facing web applications are reviewed via manual or automated application vulnerability security assessment tools:
  - At least once every 12 months and after significant changes
  - By an entity that specializes in application security
  - Including all common software attacks in Section 3.2
  - All vulnerabilities are ranked per Section 3.6
  - All vulnerabilities are corrected and the application is re-evaluated

**Web Application Firewall (per PCI DSS 6.4.2):**
- An automated technical solution (e.g., WAF) is deployed that continually detects and prevents web-based attacks:
  - Installed in front of public-facing web applications
  - Configured to detect and prevent web-based attacks
  - Actively running and up to date
  - Generating audit logs
  - Configured to either block attacks or generate immediate alerts

### 3.9 Payment Page Script Management

All payment page scripts shall be managed per PCI DSS 6.4.3.

- **Authorization:** A method is implemented to confirm that each script is authorized.

- **Integrity:** A method is implemented to assure the integrity of each script (e.g., Subresource Integrity, Content Security Policy).

- **Inventory:** An inventory of all scripts is maintained with written justification as to why each is necessary.

- **Minimization:** Only scripts necessary for payment page functionality are loaded.

### 3.10 Change Management

Changes to all system components in the production environment shall follow established procedures per PCI DSS 6.5.1.

- **Change Documentation:** Changes include:
  - Reason for, and description of, the change
  - Documentation of security impact
  - Documented change approval by authorized parties

- **Testing:** Changes are tested to verify they do not adversely impact system security. For bespoke and custom software, all updates are tested for compliance with Section 3.2 before deployment.

- **Rollback Procedures:** Procedures to address failures and return to a secure state are documented and available.

- **PCI DSS Validation (per PCI DSS 6.5.2):** Upon completion of a significant change, all applicable PCI DSS requirements are confirmed to be in place on new or changed systems, and documentation is updated.

### 3.11 Environment Separation

Pre-production environments shall be separated from production environments per PCI DSS 6.5.3.

- **Environment Separation:** Development, testing, and staging environments are logically or physically separated from production environments.

- **Access Controls:** Separation is enforced with access controls that prevent unauthorized access between environments.

- **Role Separation (per PCI DSS 6.5.4):** Roles and functions are separated between production and pre-production environments to provide accountability such that only reviewed and approved changes are deployed.

### 3.12 Production Data Protection

Live PANs and production data shall be protected in pre-production environments per PCI DSS 6.5.5 and 6.5.6.

- **No Live PANs:** Live PANs are not used in pre-production environments, except where those environments are included in the CDE and protected in accordance with all applicable PCI DSS requirements.

- **Test Data:** Test PANs are used for development and testing purposes. Test PANs are obtained from payment networks or generated using approved test card number ranges.

- **Data Masking:** Where production data is needed for testing, it is masked or anonymized before use in pre-production environments.

- **Cleanup:** Test data and test accounts are removed from system components before the system goes into production.

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 6.1.1, 6.2.1 |
| 3.1 | SOC 2 TSC | CC8.1 |
| 3.1 | GLBA Safeguards | § 314.4(c)(4) |
| 3.2 | PCI DSS v4.0 | 6.2.4 |
| 3.2 | SOC 2 TSC | CC8.1 |
| 3.3 | PCI DSS v4.0 | 6.2.3 |
| 3.3 | SOC 2 TSC | CC8.1 |
| 3.4 | PCI DSS v4.0 | 6.2.3 |
| 3.4 | SOC 2 TSC | CC6.1, CC8.1 |
| 3.4 | GLBA Safeguards | § 314.4(c)(4) |
| 3.5 | PCI DSS v4.0 | 6.2.2 |
| 3.5 | SOC 2 TSC | CC1.4 |
| 3.6 | PCI DSS v4.0 | 6.3.1, 6.3.3 |
| 3.6 | SOC 2 TSC | CC7.1 |
| 3.7 | PCI DSS v4.0 | 6.3.2 |
| 3.7 | SOC 2 TSC | CC8.1 |
| 3.8 | PCI DSS v4.0 | 6.4.1, 6.4.2 |
| 3.8 | SOC 2 TSC | CC6.6 |
| 3.9 | PCI DSS v4.0 | 6.4.3 |
| 3.10 | PCI DSS v4.0 | 6.5.1, 6.5.2 |
| 3.10 | SOC 2 TSC | CC8.1 |
| 3.10 | GLBA Safeguards | § 314.4(c)(7) |
| 3.11 | PCI DSS v4.0 | 6.5.3, 6.5.4 |
| 3.11 | SOC 2 TSC | CC8.1 |
| 3.12 | PCI DSS v4.0 | 6.5.5, 6.5.6 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Automated Security Scanning** | Tools that automatically analyze code, dependencies, and applications for security vulnerabilities. |
| **Bespoke Software** | Software developed specifically for an entity's unique requirements, either in-house or by a third party. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Code Review** | The systematic examination of source code by peers to identify defects and security vulnerabilities before deployment. |
| **Content Security Policy (CSP)** | An HTTP header that allows website operators to declare approved origins of content that browsers should be allowed to load. |
| **Custom Software** | Software developed specifically for an entity's unique requirements, including modifications to third-party software. |
| **Live PAN** | A valid Primary Account Number that has the potential to be used to conduct payment transactions. |
| **Pre-production Environment** | Development, testing, or user acceptance testing (UAT) environments that are not used for production processing. |
| **Secure Coding** | Programming practices that prevent common security vulnerabilities and implement appropriate security controls. |
| **Software Composition Analysis (SCA)** | Tools that analyze third-party and open-source components for known vulnerabilities. |
| **Static Application Security Testing (SAST)** | Tools that analyze source code for security vulnerabilities without executing the code. |
| **Subresource Integrity (SRI)** | A security feature that enables browsers to verify that resources they fetch are delivered without unexpected manipulation. |
| **Web Application Firewall (WAF)** | A security solution that filters and monitors HTTP traffic between a web application and the Internet. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Approve secure development policies. Oversee application security program. Ensure compliance with PCI DSS, SOC 2, and GLBA requirements. |
| **IT Security Team** | Maintain security scanning tools. Define secure coding guidelines. Conduct application security assessments. Manage WAF configuration and monitoring. |
| **Development Team Lead** | Ensure team compliance with secure development practices. Coordinate code reviews. Ensure team members receive security training. Review and approve changes before production deployment. |
| **Software Developers** | Follow secure coding practices. Participate in code reviews. Complete required security training. Report security vulnerabilities. Implement security controls in bespoke and custom software. |
| **PCI Program Manager** | Ensure development practices meet PCI DSS requirements. Coordinate with QSA on development-related assessment activities. Maintain documentation for PCI compliance. |
| **DevOps/Platform Team** | Implement automated security scanning in CI/CD pipelines. Maintain environment separation. Manage access controls between environments. |
| **QA Team** | Test for security vulnerabilities. Verify test data is removed before production. Validate security controls are functioning as designed. |

