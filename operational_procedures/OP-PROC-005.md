# Legal Hold Procedure (OP-PROC-005)

### 1. Purpose

To outline the steps for issuing, tracking, and releasing a legal hold on information that is relevant to reasonably anticipated or actual litigation, government investigation, regulatory examination, or audit, including special considerations for cardholder data and customer financial information.

### 2. Scope

This procedure applies to all employees and systems where company data is stored, including:

- Electronic documents, emails, and databases
- Physical records and documents
- Cardholder data and transaction records
- Customer financial information (NPI)
- Audit logs and security records
- Third-party service provider data

### 3. Overview

This procedure ensures that all potentially relevant information is preserved and protected from destruction or modification when the company is notified of a legal action, regulatory examination (PCI DSS, GLBA, BSA/AML), or investigation. It details the formal process managed by the Legal team to suspend normal data retention and disposal schedules for the duration of the legal matter.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Legal Team | Identifies the need for a legal hold based on notification of: |
| | | - Lawsuit or potential litigation |
| | | - Government investigation or subpoena |
| | | - Regulatory examination (PCI DSS QSA assessment, GLBA examination, BSA/AML review) |
| | | - Internal investigation |
| **2** | Legal Team | Issues a formal Legal Hold Notice to all relevant employees (custodians) and system administrators, specifying: |
| | | - Subject matter and scope of data to be preserved |
| | | - Time period of relevant data |
| | | - Types of data included (email, documents, CHD, transaction logs, etc.) |
| | | - Duration of hold (if known) |
| **3** | IT Team | Upon receipt of the notice: |
| | | - Suspends all automated deletion and data disposal processes for identified data |
| | | - Ensures backup retention schedules are extended for relevant systems |
| | | - Preserves audit logs and security records for specified period |
| **4** | PCI Program Manager | If cardholder data is within scope, ensures CHD retention follows hold requirements while maintaining PCI DSS controls. |
| **5** | Custodians | Acknowledge receipt of the hold notice and take necessary steps to preserve all relevant information under their control. |
| **6** | Legal Team | Maintains an inventory of all data subject to the hold and sends periodic reminders to custodians to ensure ongoing compliance. |
| **7** | Legal Team | When the legal matter is fully resolved, issues a formal Hold Release Notice to all custodians and the IT team, authorizing resumption of normal data retention policies. |
| **8** | IT Team | Upon release, resumes normal retention schedules and disposes of data that exceeded retention periods during the hold (unless otherwise required). |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC2.1 |
| **3-4** | PCI DSS v4.0 | 3.2.1 |
| **3-4** | GLBA Safeguards | § 314.4(c)(6) |

### 6. Artifact(s)

- Formal Legal Hold Notice with list of custodians
- Formal Hold Release Notice
- Acknowledgement receipts from custodians
- Data preservation inventory
- IT hold implementation records

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Legal Hold** | A process that an organization uses to preserve all forms of relevant information when litigation or investigation is reasonably anticipated. |
| **Custodian** | An individual who has possession, custody, or control of potentially relevant information. |
| **CHD** | Cardholder Data - at minimum, the full Primary Account Number (PAN). |
| **NPI** | Nonpublic Personal Information - personally identifiable financial information as defined under GLBA. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Legal Team** | Responsible for identifying the need for a legal hold, issuing notices, tracking compliance, and releasing the hold. |
| **IT Team** | Responsible for implementing technical measures to suspend data disposal and preserve backups for information on hold. |
| **PCI Program Manager** | Ensures cardholder data preservation maintains PCI DSS compliance. |
| **Custodians** | Responsible for preserving all information relevant to the legal hold notice. |

