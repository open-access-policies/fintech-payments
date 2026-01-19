# Privileged Access Review Procedure (ENG-PROC-006)

### 1. Purpose

To outline the steps for conducting and documenting the required reviews of all user accounts with privileged access to production infrastructure, ensuring the principle of least privilege is maintained per PCI DSS 7.2.4 and GLBA requirements.

### 2. Scope

This procedure applies to all user accounts, service accounts, and roles with administrative or privileged access to:

- Production systems and databases
- Cardholder data environment (CDE) systems
- Payment processing infrastructure
- Systems handling customer financial information (NPI)
- Network devices and security systems

### 3. Overview

This procedure describes the privileged access review process per PCI DSS 7.2.4 and GLBA 314.4(c). For CDE systems, reviews are conducted at least every six months. For other production systems, reviews are conducted quarterly. It begins with the Security Team generating a list of privileged accounts, which is then distributed to system owners for review. Managers attest to the continued need for each access right. Any unnecessary access is then revoked, and the completed attestations are stored for audit purposes.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Security Team | On the required frequency (quarterly for production, every six months for CDE per PCI DSS 7.2.4), generates a report from the identity and access management system listing all users and service accounts with privileged access. |
| **2** | IT Security Team | Sends the access report to the relevant system owners or managers responsible for the systems listed, noting which systems are CDE or NPI. |
| **3** | System Owner / Manager | Reviews each user's access rights on the report and attests in writing that: |
| | | - The access is still required for their job function |
| | | - Access level is appropriate (least privilege) |
| | | - For CDE access: User still requires access to cardholder data |
| **4** | IT Team / System Administrator | Upon notification from the manager or Security Team, revokes any access that is no longer necessary or has been denied during the review. |
| **5** | IT Security Team | Collects and stores the completed, signed attestations as an audit record of the review. |
| **6** | PCI Program Manager | For CDE systems: Ensures review documentation meets PCI DSS 7.2.4 requirements and is included in compliance evidence. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-6** | SOC 2 TSC | CC6.1, CC6.2 |
| **1-6** | PCI DSS v4.0 | 7.2.4, 7.2.5 |
| **1-6** | GLBA Safeguards | § 314.4(c) |

### 6. Artifact(s)

- Signed access review attestation forms
- Completed access review tickets with documented approvals
- Access revocation records
- PCI DSS compliance documentation (for CDE systems)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Privileged Access** | Access rights beyond those of a standard user. This includes administrative rights to servers, databases, applications, or network devices. |
| **Least Privilege** | The principle of restricting access rights for users to the minimum permissions they need to perform their work. |
| **Attestation** | The act of formally confirming that something is true, correct, or has been completed. |
| **CDE** | Cardholder Data Environment - the people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **IT Security Team** | Manages the overall access review process, generates reports, distributes them, and stores the final attestations. |
| **System Owner / Manager** | Reviews the access for their systems and personnel, and attests to the ongoing need for privileged access. |
| **IT Team / System Administrator** | Revokes access rights as directed by the outcome of the review. |
| **PCI Program Manager** | Ensures CDE access reviews meet PCI DSS 7.2.4 requirements. |

