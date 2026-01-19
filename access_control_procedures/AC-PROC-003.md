# User Access Review Procedure (AC-PROC-003)

### 1. Purpose

To define the process for conducting periodic reviews of user access rights to ensure adherence to the principle of least privilege, with enhanced review requirements for access to the cardholder data environment (CDE) and customer financial information.

### 2. Scope

This procedure applies to all user accounts with access to company information systems and the managers or system owners responsible for those accounts. It includes:

- All production systems and applications
- Cardholder data environment (CDE) systems
- Systems processing nonpublic personal information (NPI)
- Third-party and vendor accounts
- Service accounts and system accounts

### 3. Overview

This procedure describes the process for conducting periodic access reviews to ensure users maintain only the access necessary for their current role. Review frequencies are tailored based on access privileges and data sensitivity per PCI DSS 7.2.4:

- **Quarterly:** Privileged/administrative accounts across all systems
- **Every Six Months:** All accounts with CDE or NPI access (per PCI DSS 7.2.4)
- **Annually:** All other standard user accounts

Regular reviews help maintain the principle of least privilege and support PCI DSS, SOC 2, and GLBA compliance.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Security Team | Generates user access reports for all systems according to the review schedule, categorized by access type (CDE, NPI, standard). |
| **2** | IT Security Team | Distributes access review forms to system owners and managers, identifying the review type and deadline. |
| **3** | System Owner / Manager | Reviews each user's access rights to verify they align with current job responsibilities. For CDE systems, verifies access aligns with documented roles per PCI DSS 7.2.1. |
| **4** | System Owner / Manager | Attests whether access is still appropriate for each team member's current role by signing the access review form. |
| **5** | System Owner / Manager | Identifies any inappropriate access or changes needed. |
| **6** | IT Department | Removes or modifies any inappropriate access rights identified during the review. |
| **7** | IT Security Team | Documents the review results, including actions taken, and stores as audit records. |
| **8** | PCI Program Manager | For CDE systems: Validates review completion and tracks in PCI DSS compliance evidence. |

**Escalation:** Failure to complete reviews within **[Number, e.g., 14]** days shall result in escalation to the CISO and potential suspension of unreviewed access.

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-7** | SOC 2 TSC | CC6.1, CC6.2, CC6.3 |
| **1-7** | PCI DSS v4.0 | 7.2.4, 7.2.5 |
| **1-7** | GLBA Safeguards | § 314.4(c)(1) |

### 6. Artifact(s)

- User access review reports (by system category)
- Completed and signed access review attestation forms
- Access modification/revocation tickets
- Escalation records (if applicable)
- Evidence of review completion for PCI DSS audits

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Principle of Least Privilege** | The concept and practice of restricting access rights for users, accounts, and computing processes to only those resources absolutely required to perform routine, authorized activities. |
| **CDE (Cardholder Data Environment)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **NPI (Nonpublic Personal Information)** | Personally identifiable financial information as defined under GLBA. |
| **System Owner** | The individual responsible for the overall operation and maintenance of an information system. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **IT Security Team** | Facilitates the access review process, generates reports, tracks completion, and stores audit records. |
| **System Owners / Managers** | Perform the detailed review of access rights for their systems or direct reports and attest to their necessity. |
| **IT Department** | Implements access changes identified during reviews. |
| **PCI Program Manager** | Ensures CDE access reviews meet PCI DSS 7.2.4 requirements and maintains compliance evidence. |
| **All Workforce Members** | Comply with the process and provide any necessary information to their managers. |

