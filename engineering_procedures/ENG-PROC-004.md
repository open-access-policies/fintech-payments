# Emergency Change Procedure (ENG-PROC-004)

### 1. Purpose

To outline the expedited process for authorizing, deploying, and retrospectively documenting an emergency change to resolve a critical issue, such as a service outage, severe security vulnerability, or payment processing disruption, while maintaining appropriate controls per PCI DSS 6.5.

### 2. Scope

This procedure applies to all emergency changes required to:

- Restore payment processing services
- Fix critical security vulnerabilities in the cardholder data environment (CDE)
- Address urgent operational issues affecting customer financial transactions
- Resolve incidents impacting systems handling NPI

### 3. Overview

This procedure defines the workflow for emergency changes per PCI DSS 6.5.4. It starts with the identification of a critical issue, followed by obtaining expedited approvals, performing a focused review, deploying the fix, and conducting a formal post-mortem review to ensure proper documentation is completed after the fact.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Engineer | Identifies a critical issue requiring an emergency change and immediately notifies the Engineering Lead, Security Team, and (for CDE issues) PCI Program Manager. |
| **2** | Engineer | Obtains and documents verbal or written approval from: |
| | | - Engineering Lead |
| | | - IT Security Team member |
| | | - For CDE changes: CISO or delegate per PCI DSS 6.5.4 |
| **3** | Engineer / Peer Reviewer | An expedited peer and security review is performed on the proposed change to ensure it is a targeted and necessary fix. For CDE changes, security impact assessment is documented. |
| **4** | Engineer | Deploys the approved change to the production environment to resolve the critical issue. |
| **5** | Engineering & Security Teams | Conduct a formal post-mortem review within **[Duration, e.g., 3 business days]** of the change. The standard change documentation and pull request are completed retroactively per PCI DSS 6.5.2. |
| **6** | PCI Program Manager | For CDE changes: Documents the emergency change for PCI DSS compliance evidence, including deviation from standard change process. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-6** | SOC 2 TSC | CC8.1 |
| **2-6** | PCI DSS v4.0 | 6.5.2, 6.5.4 |

### 6. Artifact(s)

- Emergency change ticket with documented approvals
- Post-mortem report with root cause analysis
- Retroactive pull request with security review
- PCI DSS emergency change documentation (for CDE changes)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Post-Mortem Review** | A formal meeting and report that analyzes an incident or emergency change to understand the cause, impact, and actions taken, and to identify lessons learned to prevent recurrence. |
| **Critical Issue** | An issue that causes a service outage, payment processing failure, data corruption, a severe security vulnerability, or significantly impacts customers' ability to conduct financial transactions. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Engineer** | Identifies the need for an emergency change, implements the fix, and obtains necessary approvals. |
| **Engineering Lead** | Provides approval for the emergency change and participates in the post-mortem review. |
| **IT Security Team** | Provides approval for the emergency change, assesses security risk, and participates in the post-mortem review. |
| **PCI Program Manager** | Ensures CDE emergency changes are documented for PCI DSS compliance. |

