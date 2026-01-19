# Change Management Policy (ENG-POL-002)

## 1. Objective

This policy establishes requirements for managing changes to systems, networks, and applications in the cardholder data environment (CDE) and supporting infrastructure in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that all changes are properly evaluated, authorized, tested, documented, and implemented to minimize risk and maintain security controls.

## 2. Scope

This policy applies to all **[Company Name]** workforce members responsible for requesting, evaluating, implementing, or reviewing changes. It encompasses:

- All system components within the cardholder data environment (CDE)
- All systems connected to the CDE
- All systems storing or processing customer financial information
- Network infrastructure and security controls
- Production applications and databases
- Security configurations and access controls
- Operational procedures and documentation

## 3. Policy

**[Company Name]** implements formal change management processes that ensure all changes are evaluated for security impact and properly controlled per PCI DSS 6.5.1.

### 3.1 Change Control Process

All changes to system components in the production environment are controlled per PCI DSS 6.5.1.

**Process Requirements:**
- Documented change control procedures exist and are followed
- Changes are approved by appropriate parties
- Security impact is assessed before implementation
- Rollback procedures exist for changes
- Changes are documented and retained

**Change Request Requirements:**
- Documented reason and description of change
- Business justification and expected benefits
- Documentation of security impact analysis
- Documented change approval by authorized parties

### 3.2 Change Classification

Changes are classified by type and risk to determine appropriate review and approval levels.

**Change Types:**

**Standard Changes:**
- Pre-approved, routine changes with established procedures
- Low risk with well-understood impact
- Examples: Password resets, user account creation, patch application per approved schedule

**Normal Changes:**
- Non-routine changes requiring individual review and approval
- Medium risk or impact requiring evaluation
- Examples: Application updates, configuration changes, new system deployments

**Emergency Changes:**
- Changes required to address critical incidents or security vulnerabilities
- Expedited approval process with post-implementation review
- Examples: Critical security patches, incident response actions, production fixes

**Risk Classification:**

| **Risk Level** | **Impact** | **Approval Level** |
|---|---|---|
| Low | Minimal impact, routine changes | Technical Lead |
| Medium | Moderate impact, requires testing | IT Manager and Security |
| High | Significant impact, affects CDE | Change Advisory Board |
| Critical | Major impact, affects payment processing | CAB + Executive Approval |

### 3.3 Security Impact Analysis

Security impact is documented for all changes per PCI DSS 6.5.1.

**Analysis Requirements:**
- Identification of security implications for all changes
- Assessment of impact on existing security controls
- Evaluation of impact on PCI DSS scope and compliance
- Review by qualified security personnel for significant changes

**Impact Assessment Areas:**
- Effect on network segmentation and CDE boundaries
- Impact on access controls and authentication
- Changes to encryption or key management
- Effect on logging and monitoring capabilities
- Impact on vulnerability management and patching
- Third-party service provider implications

### 3.4 Change Approval

Changes are approved before implementation by appropriate authorities.

**Approval Requirements:**
- Approval by parties separate from those requesting the change
- All approvals documented and retained
- Approval authority based on change classification

**Approval Roles:**

**Change Advisory Board (CAB):**
- Reviews high-risk and significant changes
- Includes representation from Security, IT, Business, and PCI Program
- Meets on scheduled basis and as needed for emergency changes
- Documents approval decisions and conditions

**Technical Approval:**
- Technical leads approve low and medium-risk changes
- Security team reviews changes affecting security controls
- PCI Program Manager reviews changes affecting CDE scope

### 3.5 Testing Requirements

Changes are tested before deployment to production per PCI DSS 6.5.3.

**Testing Requirements:**
- All changes are tested for potential security impact
- Functionality testing validates expected behavior
- Rollback or back-out procedures are tested
- Test results documented and reviewed before approval

**Testing Environments:**
- Development environments isolated from production
- Test/staging environments mirror production configuration
- Production data is not used for testing (or is masked/tokenized)
- CDE changes tested in CDE-equivalent test environment

### 3.6 Documentation Requirements

All changes are documented and change records maintained per PCI DSS 6.5.1.

**Change Record Contents:**
- Change identifier and description
- Business justification
- Security impact analysis
- Test results
- Approval documentation
- Implementation date and personnel
- Verification of successful implementation
- Rollback procedures

**Documentation Retention:**
- Change records retained for at least **[Period, e.g., 12 months]**
- Documentation available for audit and review
- Version history maintained for configurations

### 3.7 Implementation Controls

Changes are implemented with appropriate controls to minimize risk.

**Implementation Requirements:**
- Changes implemented by authorized personnel only
- Implementation during approved maintenance windows where appropriate
- Verification that change was implemented as approved
- Documentation of any deviations from planned change

**Production Deployment:**
- Production changes follow established deployment procedures
- Separation of duties between developers and production personnel where feasible
- Production access limited to personnel with business need

### 3.8 Back-out and Rollback

Procedures exist for backing out changes that fail or cause issues per PCI DSS 6.5.4.

**Rollback Requirements:**
- Back-out procedures documented for all changes
- Backups taken before changes where appropriate
- Criteria defined for initiating rollback
- Rollback tested before production implementation

**Rollback Process:**
- Trigger conditions documented (test failures, performance issues, security concerns)
- Communication plan for rollback situations
- Verification steps after rollback completion
- Post-rollback analysis and documentation

### 3.9 Emergency Changes

Emergency changes follow expedited procedures while maintaining appropriate controls.

**Emergency Change Criteria:**
- Critical security vulnerability requiring immediate remediation
- Production outage affecting payment processing
- Incident response action requiring immediate implementation
- Legal or regulatory mandate with urgent deadline

**Emergency Process:**
- Verbal approval from appropriate authority (documented immediately after)
- Minimum documentation during implementation
- Full documentation completed within **[Duration, e.g., 24 hours]** post-implementation
- Post-implementation review by Change Advisory Board

### 3.10 Network and NSC Changes

Changes to network connections and network security controls follow additional requirements per PCI DSS 1.2.2.

**NSC Change Requirements:**
- All changes to network connections approved and managed per this policy
- All changes to NSC configurations approved and managed per this policy
- Network documentation updated after changes
- NSC configuration reviews identify changes for validation

**Network Change Types:**
- New network connections to or from the CDE
- Firewall rule modifications
- Network topology changes
- NSC upgrades or replacements

### 3.11 Post-Implementation Review

Changes are verified after implementation to confirm success.

**Verification Requirements:**
- Confirmation that change was implemented as approved
- Security controls verified functioning properly
- No unintended side effects observed
- Documentation updated to reflect current state

**Review Process:**
- Technical verification by implementation team
- Security verification for security-impacting changes
- Business verification of functionality
- Lessons learned captured for significant changes

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 6.5.1 |
| 3.1 | SOC 2 TSC | CC8.1 |
| 3.3 | PCI DSS v4.0 | 6.5.1 |
| 3.4 | PCI DSS v4.0 | 6.5.2 |
| 3.5 | PCI DSS v4.0 | 6.5.3 |
| 3.6 | PCI DSS v4.0 | 6.5.1 |
| 3.8 | PCI DSS v4.0 | 6.5.4 |
| 3.10 | PCI DSS v4.0 | 1.2.2 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Change Advisory Board (CAB)** | Cross-functional group responsible for reviewing and approving significant changes. |
| **Change Control** | The process of controlling modifications to hardware, software, firmware, and documentation. |
| **Emergency Change** | A change that must be implemented immediately to restore service or prevent imminent security breach. |
| **Normal Change** | A non-routine change that requires individual assessment and authorization. |
| **Rollback** | The process of reverting a system to its previous state after a failed or problematic change. |
| **Standard Change** | A pre-approved change that is low risk, relatively common, and follows a procedure or work instruction. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own change management policy. Ensure security is integrated into change processes. Approve security-impacting changes. |
| **Change Advisory Board (CAB)** | Review and approve high-risk changes. Assess change schedules. Conduct post-implementation reviews. |
| **IT Management** | Approve changes within delegated authority. Manage change schedule. Ensure adequate testing. |
| **PCI Program Manager** | Review changes affecting CDE scope. Ensure PCI DSS compliance is maintained. Update scope documentation. |
| **IT Security Team** | Review security impact of changes. Verify security controls after implementation. Approve security-related changes. |
| **Change Requestors** | Submit complete change requests. Provide business justification. Participate in testing and verification. |
| **Change Implementers** | Implement approved changes per documentation. Follow rollback procedures when needed. Document implementation. |

