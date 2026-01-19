# CDE Scoping Procedure (PAY-PROC-001)

### 1. Purpose

To define the process for identifying, documenting, and validating the cardholder data environment (CDE) scope, ensuring that all systems storing, processing, or transmitting cardholder data are identified and protected per PCI DSS 12.5.

### 2. Scope

This procedure applies to all systems, networks, and processes that may interact with cardholder data, including:

- Systems within the CDE
- Connected systems that could impact CDE security
- Third-party service providers with CHD access
- Network segmentation controls

### 3. Overview

This procedure outlines the annual and triggered scope validation process per PCI DSS 12.5.1 and 12.5.2. It begins with identifying all account data flows, documenting system components, validating network segmentation, and concluding with formal approval of the scope documentation.

### 4. Procedure

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | PCI Program Manager | Initiates the annual CDE scope review process or triggers review upon significant infrastructure changes. |
| **2** | PCI Program Manager | Gathers current documentation: |
| | | - Network diagrams |
| | | - Data flow diagrams |
| | | - System inventory |
| | | - Previous scope documentation |
| **3** | IT/Network Team | Documents all locations where account data is stored, processed, or transmitted, including: |
| | | - Databases and file systems |
| | | - Applications and middleware |
| | | - Network paths |
| | | - Backup and archive locations |
| **4** | IT Security Team | Identifies all system components in the CDE and connected systems per PCI DSS 12.5.1: |
| | | - Servers and databases |
| | | - Network devices |
| | | - Security systems |
| | | - Third-party connections |
| **5** | IT Security Team | Reviews network segmentation controls and validates that out-of-scope systems cannot access the CDE per PCI DSS 12.5.2. |
| **6** | PCI Program Manager | Documents any third-party service providers (TPSPs) with access to CHD or connectivity to CDE. |
| **7** | PCI Program Manager | Creates or updates: |
| | | - CDE network diagram |
| | | - Cardholder data flow diagram |
| | | - In-scope system inventory |
| | | - TPSP responsibility matrix |
| **8** | IT Security Team | Validates scope through data discovery scans to identify undocumented PAN storage. |
| **9** | CISO | Reviews and approves the scope documentation. |
| **10** | PCI Program Manager | Distributes approved scope documentation to relevant stakeholders and archives for PCI DSS compliance evidence. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **1-10** | PCI DSS v4.0 | 12.5.1, 12.5.2 |
| **3-4** | PCI DSS v4.0 | 1.2.3, 1.2.4 |
| **5** | PCI DSS v4.0 | 11.4.5 |
| **6** | PCI DSS v4.0 | 12.8.1 |
| **1-10** | SOC 2 TSC | CC6.1 |

### 6. Artifact(s)

- Approved CDE scope documentation
- Updated network diagrams
- Cardholder data flow diagrams
- In-scope system inventory
- TPSP responsibility matrix
- Data discovery scan results
- CISO approval documentation

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Connected System** | A system that is connected to or provides services to the CDE and could impact its security. |
| **Network Segmentation** | Isolation of the CDE from other networks to reduce PCI DSS scope. |
| **Scope** | The systems, networks, processes, and people that are subject to PCI DSS requirements. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **PCI Program Manager** | Coordinates the scoping process, maintains documentation, and tracks approvals. |
| **IT/Network Team** | Provides network diagrams and data flow information. Implements segmentation controls. |
| **IT Security Team** | Validates scope accuracy, conducts data discovery, and tests segmentation. |
| **CISO** | Reviews and approves scope documentation. Authorizes scope changes. |
| **Application Owners** | Provide information about application data handling and CHD interactions. |

