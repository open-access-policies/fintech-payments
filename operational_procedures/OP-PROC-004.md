# Secure Media Disposal Procedure (OP-PROC-004)

### 1. Purpose

To provide step-by-step instructions for securely destroying or sanitizing different types of electronic media and physical documents to prevent the unauthorized disclosure of cardholder data, customer financial information, and other sensitive data per PCI DSS 9.4.6 and GLBA § 314.4(c)(6).

### 2. Scope

This procedure applies to all company-owned and managed media, both electronic and physical, that contains or may have contained:

- Cardholder data (CHD) or sensitive authentication data (SAD)
- Customer financial information (NPI)
- Confidential company information

Media types include:
- Hard drives and solid-state drives (SSDs)
- USB drives and removable media
- Backup tapes
- Mobile devices
- Paper documents containing sensitive data
- POI (Point of Interaction) devices

### 3. Overview

This procedure outlines the mandated methods for disposing of or sanitizing media based on the classification level and type of data contained, per PCI DSS 9.4.6 requirements. It ensures that all cardholder data and customer financial information is rendered unrecoverable, in compliance with PCI DSS, GLBA, and industry standards.

### 4. Procedure

#### 4.1 Electronic Media (Hard Drives, SSDs)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Asset Custodian / IT Team | Identify media that is at end of lifecycle, being decommissioned, or being reassigned. |
| **2** | IT Team | Verify whether media ever contained cardholder data, SAD, or NPI by reviewing asset inventory. |
| **3** | IT Team | For media containing CHD, SAD, or NPI: |
| | | - Perform cryptographic erasure per NIST SP 800-88 guidelines, OR |
| | | - Physically destroy media (shredding, degaussing, incineration) |
| **4** | IT Team | For media that cannot be cryptographically erased or contained SAD: Physically destroy the media per PCI DSS 9.4.6. |
| **5** | IT Team | Document the disposal in the asset management system including: |
| | | - Asset identifier |
| | | - Data classification |
| | | - Disposal method used |
| | | - Date of disposal |
| | | - Personnel involved |
| **6** | IT Team | If third-party vendor used, obtain and file certificate of destruction. |

#### 4.2 Removable Media (USB, Backup Tapes)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Team | Identify removable media containing CHD, NPI, or confidential data. |
| **2** | IT Team | For reusable media: Perform secure wipe per NIST SP 800-88 before reuse. |
| **3** | IT Team | For disposal: Physically destroy media (shredding). |
| **4** | IT Team | Document disposal and update media inventory. |

#### 4.3 Paper Documents

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | All Employees | Identify paper documents containing CHD, NPI, or confidential information no longer required. |
| **2** | All Employees | Place documents in designated secure shredding bins (cross-cut shredding required per PCI DSS 9.4.6). |
| **3** | Approved Disposal Vendor | Collects contents of shredding bins on scheduled basis for secure, off-site destruction. |
| **4** | Facilities / IT Team | Obtain and file certificate of destruction from vendor. Retain for **[Duration, e.g., 1 year]**. |

#### 4.4 POI Devices (Payment Terminals)

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | IT Team / PCI Program Manager | Identify POI devices being decommissioned. |
| **2** | IT Team | Perform factory reset to remove all configuration and keys. |
| **3** | IT Team | Physically destroy devices or return to vendor for certified destruction. |
| **4** | PCI Program Manager | Update POI inventory and document destruction. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1-4.4** | PCI DSS v4.0 | 9.4.6 |
| **4.1-4.3** | SOC 2 TSC | CC6.5 |
| **4.1-4.3** | GLBA Safeguards | § 314.4(c)(6) |
| **4.1-4.2** | NIST | SP 800-88 |

### 6. Artifact(s)

- Disposal records in asset management system
- Certificates of destruction from third-party vendors
- Updated media and asset inventory
- POI device destruction documentation

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Cryptographic Erasure** | The process of using encryption to render targeted data unreadable by destroying the encryption keys. |
| **Degaussing** | The process of reducing or eliminating magnetic data stored on tape and disk media. |
| **Physical Destruction** | The process of rendering media unusable by physically altering it (shredding, pulverizing, incineration). |
| **POI (Point of Interaction)** | Devices used to capture payment card data, such as terminals, PIN pads, and card readers. |
| **Cross-cut Shredding** | A shredding method that cuts paper both lengthwise and crosswise, making reconstruction virtually impossible. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **IT Team** | Responsible for secure sanitization and destruction of electronic media and managing disposal vendors. |
| **All Employees** | Responsible for properly disposing of sensitive paper documents in secure shred bins. |
| **Approved Disposal Vendor** | Responsible for secure collection and destruction of media and providing certificates of destruction. |
| **PCI Program Manager** | Ensures disposal procedures meet PCI DSS requirements and maintains compliance evidence. |

