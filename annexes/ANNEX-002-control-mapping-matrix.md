# ANNEX-002: Control Mapping Matrix

## Purpose

This annex maps **[Company Name]** policies and procedures to applicable regulatory frameworks, enabling gap analysis, compliance tracking, and audit support.

---

## Framework Coverage Summary

| **Framework** | **Total Requirements** | **Policies Mapped** | **Procedures Mapped** |
|---------------|------------------------|---------------------|----------------------|
| PCI DSS v4.0 | 204 requirements | All applicable | All applicable |
| SOC 2 TSC | 69 criteria | All | All |
| GLBA Safeguards | 16 elements | All | All |
| GLBA Privacy | 8 sections | PRV-POL-001, PRV-POL-002 | PRV-PROC-001 |
| BSA/AML | 5 pillars | FIN-POL-001 through FIN-POL-004 | FIN-PROC-001 through FIN-PROC-005 |

---

## PCI DSS v4.0 Requirement Mapping

### Requirement 1: Install and Maintain Network Security Controls

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 1.1 Processes and mechanisms defined | SEC-POL-009 | - |
| 1.2 Network security controls configured | SEC-POL-009 | - |
| 1.3 Network access restricted | SEC-POL-009, AC-POL-001 | - |
| 1.4 Cardholder data environment access controlled | SEC-POL-009 | PAY-PROC-001 |
| 1.5 Risks to CDE mitigated | SEC-POL-009 | - |

### Requirement 2: Apply Secure Configurations

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 2.1 Processes and mechanisms defined | ENG-POL-001 | ENG-PROC-005 |
| 2.2 System components configured securely | ENG-POL-001 | ENG-PROC-005 |
| 2.3 Wireless environments configured securely | SEC-POL-009 | - |

### Requirement 3: Protect Stored Account Data

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 3.1 Processes and mechanisms defined | PAY-POL-001, SEC-POL-004 | - |
| 3.2 Account data storage minimized | PAY-POL-001, SEC-POL-004 | - |
| 3.3 SAD not stored after authorization | PAY-POL-001 | - |
| 3.4 PAN display and copy restricted | PAY-POL-001, PAY-POL-004 | - |
| 3.5 PAN secured wherever stored | PAY-POL-001, PAY-POL-004 | PAY-PROC-003 |
| 3.6 Cryptographic keys secured | OP-POL-001, PAY-POL-001 | OP-PROC-001 |
| 3.7 Key management procedures | OP-POL-001 | OP-PROC-001 |

### Requirement 4: Protect Cardholder Data During Transmission

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 4.1 Processes and mechanisms defined | PAY-POL-001, OP-POL-001 | - |
| 4.2 PAN protected during transmission | PAY-POL-001, OP-POL-001 | - |

### Requirement 5: Protect Systems from Malware

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 5.1 Processes and mechanisms defined | SEC-POL-008 | - |
| 5.2 Malware prevented or detected | SEC-POL-008 | - |
| 5.3 Anti-malware mechanisms active | SEC-POL-008 | - |
| 5.4 Anti-phishing mechanisms protect users | SEC-POL-008 | - |

### Requirement 6: Develop and Maintain Secure Systems

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 6.1 Processes and mechanisms defined | ENG-POL-001 | - |
| 6.2 Software developed securely | ENG-POL-001, ENG-POL-002 | ENG-PROC-001 |
| 6.3 Security vulnerabilities identified and addressed | ENG-POL-001 | ENG-PROC-002, SEC-PROC-008 |
| 6.4 Public-facing web applications protected | ENG-POL-001 | ENG-PROC-001 |
| 6.5 Changes managed securely | ENG-POL-001 | ENG-PROC-003, ENG-PROC-004 |

### Requirement 7: Restrict Access to Cardholder Data

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 7.1 Processes and mechanisms defined | AC-POL-001 | AC-PROC-003 |
| 7.2 Access appropriately restricted | AC-POL-001 | AC-PROC-003, AC-PROC-004 |
| 7.3 Access managed via access control system | AC-POL-001 | AC-PROC-004 |

### Requirement 8: Identify Users and Authenticate Access

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 8.1 Processes and mechanisms defined | AC-POL-001, AC-POL-002 | - |
| 8.2 User identification managed | AC-POL-001 | AC-PROC-004 |
| 8.3 Strong authentication established | AC-POL-001, AC-POL-002 | - |
| 8.4 MFA implemented | AC-POL-001 | - |
| 8.5 MFA systems configured properly | AC-POL-001 | - |
| 8.6 Authentication mechanisms managed | AC-POL-001 | - |

### Requirement 9: Restrict Physical Access

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 9.1 Processes and mechanisms defined | SEC-POL-006 | SEC-PROC-006 |
| 9.2 Physical access controls | SEC-POL-006 | SEC-PROC-006 |
| 9.3 Physical access authorized | SEC-POL-006 | SEC-PROC-006 |
| 9.4 Media physically secured | SEC-POL-004, OP-POL-002 | OP-PROC-004 |
| 9.5 POI devices protected | PAY-POL-005 | PAY-PROC-002 |

### Requirement 10: Log and Monitor Access

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 10.1 Processes and mechanisms defined | SEC-POL-005, OP-POL-003 | - |
| 10.2 Audit logs implemented | SEC-POL-005, OP-POL-003 | - |
| 10.3 Audit logs protected | SEC-POL-005 | - |
| 10.4 Audit logs reviewed | SEC-POL-005 | - |
| 10.5 Audit log history retained | SEC-POL-005, OP-POL-003 | - |
| 10.6 Time synchronization | SEC-POL-005 | - |
| 10.7 Critical failures detected | SEC-POL-005 | - |

### Requirement 11: Test Security Regularly

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 11.1 Processes and mechanisms defined | SEC-POL-003 | - |
| 11.2 Wireless access points identified | SEC-POL-009 | - |
| 11.3 Vulnerabilities identified and managed | SEC-POL-003 | SEC-PROC-008, PAY-PROC-005 |
| 11.4 Penetration testing performed | SEC-POL-003 | ENG-PROC-001 |
| 11.5 Intrusions detected and responded to | SEC-POL-005 | - |
| 11.6 Changes to payment pages detected | ENG-POL-001 | - |

### Requirement 12: Support Information Security with Policies

| **Requirement** | **Policy** | **Procedure** |
|-----------------|------------|---------------|
| 12.1 Information security policy established | SEC-POL-001 | - |
| 12.2 Acceptable use policies defined | AC-POL-002 | AC-PROC-001 |
| 12.3 Risks to CDE formally identified | SEC-POL-003 | SEC-PROC-004 |
| 12.4 PCI DSS responsibilities assigned | PAY-POL-002 | - |
| 12.5 PCI DSS scope documented | PAY-POL-002 | PAY-PROC-001 |
| 12.6 Security awareness program | SEC-POL-001 | - |
| 12.7 Personnel screened | OP-POL-004 | OP-PROC-006 |
| 12.8 TPSP managed | SEC-POL-001, PAY-POL-002 | SEC-PROC-005, PAY-PROC-006 |
| 12.9 Service provider compliance | PAY-POL-002 | PAY-PROC-006 |
| 12.10 Security incidents responded to | RES-POL-001 | RES-PROC-001, RES-PROC-002, PAY-PROC-004 |

---

## SOC 2 Trust Services Criteria Mapping

| **Criteria** | **Description** | **Primary Policies** |
|--------------|-----------------|---------------------|
| CC1.1-CC1.5 | Control Environment | SEC-POL-001 |
| CC2.1-CC2.3 | Communication & Information | SEC-POL-001, OP-POL-003 |
| CC3.1-CC3.4 | Risk Assessment | SEC-POL-003 |
| CC4.1-CC4.2 | Monitoring | SEC-POL-005 |
| CC5.1-CC5.3 | Control Activities | All policies |
| CC6.1-CC6.8 | Logical & Physical Access | AC-POL-001, SEC-POL-006 |
| CC7.1-CC7.5 | System Operations | RES-POL-001, OP-POL-003 |
| CC8.1 | Change Management | ENG-POL-001 |
| CC9.1-CC9.2 | Risk Mitigation | SEC-POL-003, SEC-POL-001 |
| C1.1-C1.2 | Confidentiality | SEC-POL-004 |
| PI1.1-PI1.5 | Processing Integrity | ENG-POL-001 |
| P1.1-P8.1 | Privacy | PRV-POL-001, PRV-POL-002 |

---

## GLBA Safeguards Rule Mapping

| **Section** | **Requirement** | **Primary Policy** | **Primary Procedure** |
|-------------|-----------------|-------------------|-----------------------|
| § 314.4(a) | Qualified Individual | PRV-POL-002, SEC-POL-001 | - |
| § 314.4(b) | Risk Assessment | SEC-POL-003, PRV-POL-002 | SEC-PROC-004 |
| § 314.4(c)(1) | Access Controls | AC-POL-001 | AC-PROC-003, AC-PROC-004 |
| § 314.4(c)(2) | Physical Security | SEC-POL-006 | SEC-PROC-006 |
| § 314.4(c)(3) | Encryption | OP-POL-001 | OP-PROC-001 |
| § 314.4(c)(4) | Secure Development | ENG-POL-001 | ENG-PROC-001 |
| § 314.4(c)(5) | MFA | AC-POL-001 | - |
| § 314.4(c)(6) | Disposal | SEC-POL-004 | OP-PROC-004 |
| § 314.4(c)(7) | Change Management | ENG-POL-001 | ENG-PROC-003 |
| § 314.4(c)(8) | Monitoring | SEC-POL-005 | - |
| § 314.4(d) | Testing | SEC-POL-003 | SEC-PROC-002 |
| § 314.4(e) | Training | SEC-POL-001 | - |
| § 314.4(f) | Service Provider Oversight | SEC-POL-001 | SEC-PROC-005 |
| § 314.4(g) | Program Updates | PRV-POL-002 | - |
| § 314.4(h) | Incident Response | RES-POL-001 | RES-PROC-001 |
| § 314.4(i) | Board Reporting | PRV-POL-002 | - |

---

## BSA/AML Five Pillars Mapping

| **Pillar** | **Requirement** | **Primary Policy** | **Primary Procedure** |
|------------|-----------------|-------------------|-----------------------|
| 1 | Internal Controls | FIN-POL-001 | FIN-PROC-001 through FIN-PROC-005 |
| 2 | Independent Testing | FIN-POL-001 | FIN-PROC-004 |
| 3 | BSA/AML Officer | FIN-POL-001 | - |
| 4 | Training | FIN-POL-001 | - |
| 5 | Customer Due Diligence | FIN-POL-002 | FIN-PROC-001 |

---

**Document ID:** ANNEX-002
**Version:** 1.0
**Last Updated:** **[Date, e.g., 2026-01-15]**
