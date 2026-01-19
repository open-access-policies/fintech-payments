# Standard Change Deployment Procedure (ENG-PROC-003)

### 1. Purpose

To detail the end-to-end process for a standard, non-emergency change to a production application or its configuration, ensuring that all changes are properly developed, tested, reviewed, and approved per PCI DSS 6.5.

### 2. Scope

This procedure applies to all standard, non-emergency changes to:

- Production applications and infrastructure
- Cardholder data environment (CDE) systems
- Payment processing systems
- Systems handling customer financial information (NPI)
- Related system configurations

### 3. Overview

This procedure outlines the standard workflow for managing changes per PCI DSS 6.5.1. It begins with a developer creating a ticket and feature branch, followed by code development, peer and security review via pull request, QA testing, and final approval from an Engineering Lead before being merged for deployment.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Developer | Creates an issue ticket documenting: |
| | | - Description of the planned change |
| | | - Reason and business justification |
| | | - Systems affected (including CDE/NPI classification) |
| | | - Creates a new feature branch in the source code repository |
| **2** | Developer | Submits a pull request when development is complete, filling out the required template including: |
| | | - Security checklist |
| | | - Testing performed |
| | | - Rollback procedure |
| | | - Security impact assessment (for CDE changes) per PCI DSS 6.5.1 |
| **3** | Peer Reviewer | Reviews the code for correctness, quality, adherence to coding standards, and provides approval. |
| **4** | IT Security Team | For changes affecting security controls, CDE, or NPI: Reviews for security implications and provides approval per PCI DSS 6.5.2. |
| **5** | QA Team | Tests changes in staging environment to verify functionality and ensure no regressions. Provides sign-off. |
| **6** | Engineering Lead | Provides final review and approval to merge the pull request, authorizing deployment per PCI DSS 6.5.2. |
| **7** | DevOps / SRE Team | Deploys to production during approved maintenance window (for CDE systems). |
| **8** | Developer / SRE Team | Verifies successful deployment and monitors for issues. |
| **9** | PCI Program Manager | For CDE changes: Documents the change for PCI DSS compliance evidence. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-9** | SOC 2 TSC | CC8.1 |
| **1-8** | PCI DSS v4.0 | 6.5.1, 6.5.2, 6.5.3 |

### 6. Artifact(s)

- Issue ticket with change documentation
- Merged pull request with all reviews and approvals
- Test results and QA sign-off
- Deployment records
- PCI DSS change documentation (for CDE changes)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Pull Request** | A mechanism for a developer to notify team members of completed changes for review, discussion, and approval before merging. |
| **Feature Branch** | A source-control branch used to develop a new feature in isolation before merging to the main branch. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Developer** | Implements the change, creates the pull request, documents security impact, and responds to feedback. |
| **Peer Reviewer** | Conducts thorough review of code changes. |
| **IT Security Team** | Assesses security impact of changes affecting CDE or security controls. |
| **QA Team** | Validates functionality and quality before release. |
| **Engineering Lead** | Provides final authorization for deployment. |
| **DevOps / SRE Team** | Deploys changes and monitors for issues. |
| **PCI Program Manager** | Ensures CDE change documentation meets PCI DSS requirements. |

