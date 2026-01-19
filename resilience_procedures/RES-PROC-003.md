# Post-Incident Review Procedure (RES-PROC-003)

### 1. Purpose

To outline the process for conducting a formal 'lessons learned' review after a significant incident is resolved and for tracking resulting action items to completion, ensuring continuous improvement of incident response capabilities per PCI DSS 12.10.6.

### 2. Scope

This procedure applies to all major information security incidents as determined by the Incident Commander, including:

- Incidents affecting the cardholder data environment (CDE)
- Incidents involving customer financial information (NPI)
- Incidents requiring regulatory notification
- Incidents with significant business impact

### 3. Overview

This procedure ensures that after a significant incident, a formal review is conducted to analyze the response, identify improvements, update documentation, and track corrective actions per PCI DSS 12.10.4 and 12.10.6 to enhance future incident response capabilities.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Incident Commander | Schedules a formal post-incident review meeting within **[Duration, e.g., 2 weeks]** of incident resolution. |
| **2** | Incident Commander | Prepares a draft incident timeline and summary for review meeting. |
| **3** | Incident Response Team (IRT) | During the meeting, analyzes: |
| | | - Incident timeline (detection, escalation, containment, resolution) |
| | | - Effectiveness of response actions |
| | | - Communication effectiveness (internal and external) |
| | | - Tool and resource availability |
| | | - Areas for improvement |
| **4** | IT Security Team | Identifies specific improvements needed: |
| | | - Updates to incident response plan |
| | | - Additional training requirements |
| | | - Tool or process enhancements |
| | | - Detection capability improvements |
| **5** | IT Security Team | Updates the Incident Response Plan and any other relevant procedures based on findings per PCI DSS 12.10.6. |
| **6** | Incident Commander | Assigns action items to specific owners with due dates and tracks to completion. |
| **7** | PCI Program Manager | For CHD incidents: Documents lessons learned and plan updates for PCI DSS compliance evidence per PCI DSS 12.10.4. |
| **8** | Incident Commander | Finalizes and files the Post-Incident Report including lessons learned section. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-8** | SOC 2 TSC | CC7.5 |
| **5, 7** | PCI DSS v4.0 | 12.10.4, 12.10.6 |
| **1-8** | NIST CSF | RC.IM |

### 6. Artifact(s)

- Post-Incident Report with lessons learned section
- Updated Incident Response Plan
- Action item tracking log
- Meeting minutes or notes
- PCI DSS compliance documentation (for CHD incidents)

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Post-Incident Review** | A formal analysis of an incident response to identify what worked well, what didn't, and what improvements should be made. |
| **Lessons Learned** | Knowledge gained from analyzing the incident that can be applied to improve future response capabilities. |
| **Action Item Tracking Log** | A formal record used to document, assign, and monitor the status of corrective actions identified during a review. |
| **CHD** | Cardholder Data - at minimum, the full Primary Account Number (PAN). |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Incident Commander** | Chairs the post-incident review meeting, ensures action items are assigned and tracked, and finalizes the report. |
| **Incident Response Team (IRT)** | Actively participates in the review, providing insights into the response process. |
| **IT Security Team** | Responsible for updating security documentation and incident response plan based on outcomes. |
| **PCI Program Manager** | Ensures CHD incident documentation meets PCI DSS requirements. |

