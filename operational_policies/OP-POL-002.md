# Asset Management Policy (OP-POL-002)

## 1. Objective

This policy establishes requirements for identifying, classifying, and managing information assets throughout their lifecycle in accordance with PCI DSS v4.0, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that all assets within and connected to the cardholder data environment (CDE) are inventoried, tracked, and appropriately protected.

## 2. Scope

This policy applies to all **[Company Name]** workforce members responsible for procuring, managing, or using information assets. It encompasses:

- All system components within the cardholder data environment (CDE)
- All systems connected to the CDE
- Hardware assets (servers, workstations, network devices, mobile devices)
- Software assets (applications, operating systems, utilities)
- Cloud resources and services
- Data assets containing cardholder data or customer financial information
- Media containing sensitive information

## 3. Policy

**[Company Name]** maintains a comprehensive asset management program to ensure all assets are identified, inventoried, and protected according to their classification per PCI DSS and GLBA requirements.

### 3.1 Asset Inventory

An inventory of system components in scope for PCI DSS is maintained per PCI DSS 12.5.1.

**Inventory Requirements:**
- All in-scope system components are documented
- Description of function/use is included for each asset
- Inventory is kept current and updated when changes occur

**Inventory Contents:**
- Asset identifier (serial number, asset tag, or unique ID)
- Asset type and description
- Make, model, and version information
- Physical or logical location
- Owner and custodian
- Classification level
- CDE scope status (in-scope, connected-to, out-of-scope)
- Installation date and warranty information

**Asset Types:**

**Hardware:**
- Servers (physical and virtual)
- Workstations and laptops
- Network devices (firewalls, routers, switches)
- Point-of-interaction (POI) devices
- Mobile devices
- Storage systems
- Backup media

**Software:**
- Operating systems
- Applications (commercial and custom)
- Databases
- Security tools
- Cloud services

### 3.2 CDE Scope Inventory

System components within the CDE are specifically identified per PCI DSS 12.5.1.

**CDE Asset Documentation:**
- All systems that store, process, or transmit cardholder data
- All systems connected to the CDE
- Systems that could impact the security of the CDE
- Security systems (firewalls, IDS/IPS, anti-malware, logging)

**Scope Categories:**
- **In-Scope (CDE):** Systems storing, processing, or transmitting CHD/SAD
- **Connected-To:** Systems that can connect to CDE systems
- **Security-Impacting:** Systems that could affect CDE security
- **Out-of-Scope:** Systems with no connectivity or impact to CDE

### 3.3 Hardware and Software Review

Hardware and software technologies are reviewed for continued support per PCI DSS 12.3.4.

**Annual Review:**
- Analysis confirms technologies continue to receive security fixes promptly
- Analysis confirms technologies support PCI DSS compliance
- Industry announcements (including vendor "end of life" plans) are documented
- Remediation plan for outdated technologies is approved by senior management

**End-of-Life Management:**
- Systems approaching end-of-life are identified
- Migration or replacement plans are developed
- Unsupported systems are documented with compensating controls
- Exceptions require executive approval and risk acceptance

### 3.4 Mobile Device Management

Mobile devices accessing company information are managed per secure requirements.

**Mobile Device Inventory:**
- Company-owned mobile devices are inventoried
- BYOD devices with company access are registered
- Mobile device management (MDM) enrollment required

**Mobile Device Requirements:**
- Device encryption mandatory
- Passcode/PIN protection required
- Remote wipe capabilities enabled
- Automatic screen lock configured
- Approved operating system versions only

**Prohibited Devices:**
- Jailbroken or rooted devices
- Devices with unsupported operating systems
- Devices with known unpatched vulnerabilities

### 3.5 Asset Classification

Assets are classified based on the sensitivity of data they process or store.

**Classification Levels:**
- **Regulated:** Assets processing cardholder data or customer NPI
- **Confidential:** Assets processing sensitive business information
- **Internal:** Assets processing general business information
- **Public:** Assets processing public information only

**Classification Assignment:**
- Asset owners assign classification based on data processed
- Classification drives security control requirements
- Higher classification levels inherit lower level requirements

### 3.6 Asset Ownership

All assets have designated owners accountable for their security.

**Owner Responsibilities:**
- Approve access to the asset
- Ensure appropriate security controls are applied
- Review asset classification annually
- Authorize changes to the asset
- Ensure proper disposal at end of life

**Custodian Responsibilities:**
- Implement security controls as directed by owner
- Maintain and operate the asset
- Report security issues to the owner
- Execute approved changes

### 3.7 Asset Procurement

New assets are acquired through approved procurement processes.

**Procurement Requirements:**
- Security requirements defined before procurement
- Vendor security assessed for significant purchases
- Assets from approved vendors only
- Security configuration applied before production deployment

**CDE Asset Procurement:**
- Additional security review for CDE-bound assets
- PCI DSS compliance requirements verified
- Default configuration documented
- Secure baseline applied before deployment

### 3.8 Asset Deployment

Assets are securely deployed according to configuration standards.

**Deployment Process:**
- Security configuration applied per hardening standards
- Asset registered in inventory before production use
- Owner and custodian assigned
- Classification determined based on intended use
- Security testing performed where appropriate

**CDE Deployment:**
- Follows change management procedures (ENG-POL-002)
- Vulnerability scan performed before production
- Access controls configured per AC-POL-001
- Logging enabled per OP-POL-005

### 3.9 Asset Transfers and Changes

Asset transfers and changes are documented and authorized.

**Transfer Requirements:**
- Asset transfers approved by current owner
- Inventory updated to reflect new location/owner
- Access permissions reviewed and updated
- Security configurations verified after transfer

**Change Documentation:**
- Significant changes documented in asset records
- Configuration changes follow change management
- Scope changes (into or out of CDE) require additional review

### 3.10 Asset Disposal

Assets are disposed of securely at end of life.

**Disposal Process:**
- Data securely erased before disposal per SEC-POL-004
- Asset removed from inventory
- Disposal documented with verification
- Media destruction follows approved methods

**CDE Asset Disposal:**
- All cardholder data rendered unrecoverable
- Certificate of destruction obtained for sensitive assets
- PCI Program Manager notified of CDE asset disposal
- Scope documentation updated

### 3.11 Cloud Asset Management

Cloud resources are managed with the same rigor as on-premises assets.

**Cloud Inventory:**
- Cloud instances and services documented
- Resource tags used for classification and tracking
- Infrastructure-as-code templates tracked in version control

**Cloud Asset Lifecycle:**
- Provisioning follows approved templates
- Security groups and access controls configured
- Automated inventory updates where possible
- Deprovisioning includes data removal verification

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 12.5.1 |
| 3.1 | SOC 2 TSC | CC6.1 |
| 3.2 | PCI DSS v4.0 | 12.5.1, 12.5.2 |
| 3.3 | PCI DSS v4.0 | 12.3.4 |
| 3.4 | PCI DSS v4.0 | 1.5.1 |
| 3.4 | GLBA Safeguards | § 314.4(c)(5) |
| 3.5 | PCI DSS v4.0 | 12.5.1 |
| 3.5 | SOC 2 TSC | CC6.1 |
| 3.10 | PCI DSS v4.0 | 9.4.6, 9.4.7 |
| 3.10 | GLBA Safeguards | § 314.4(c)(6) |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Asset** | Any item of value to the organization including hardware, software, data, and cloud resources. |
| **Asset Owner** | Individual accountable for the security and appropriate use of an asset. |
| **Asset Custodian** | Individual responsible for implementing and maintaining security controls on an asset. |
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **End-of-Life (EOL)** | Date when a vendor stops selling a product or providing updates. |
| **End-of-Support (EOS)** | Date when a vendor stops providing security patches and support for a product. |
| **Mobile Device Management (MDM)** | Software that manages, monitors, and secures mobile devices across the organization. |
| **System Component** | Any network component, server, computing device, or application within or connected to the CDE. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own asset management policy. Ensure asset inventory supports security and compliance. Approve asset classification standards. |
| **IT Department** | Maintain asset inventory systems. Manage asset lifecycle from procurement through disposal. Implement MDM solutions. Ensure secure asset deployment. |
| **PCI Program Manager** | Ensure CDE assets are properly identified. Maintain CDE scope documentation. Coordinate with QSA on asset-related assessments. Track CDE asset inventory accuracy. |
| **Asset Owners** | Classify owned assets. Approve access to assets. Review asset security annually. Authorize asset disposal. |
| **Finance/Procurement** | Manage asset procurement process. Track asset financial records. Coordinate with IT on purchase requests. |
| **All Workforce Members** | Report asset issues. Protect assigned assets. Return assets upon termination. Follow acceptable use policies. |

