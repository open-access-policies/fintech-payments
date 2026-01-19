# Point-of-Interaction Security Policy (PAY-POL-005)

## 1. Objective

This policy establishes **[Company Name]**'s requirements for securing point-of-interaction (POI) devices including payment terminals, point-of-sale (POS) systems, and unattended payment terminals. It ensures that all devices that accept payment cards are protected against tampering, unauthorized modification, and skimming attacks in accordance with PCI DSS v4.0 Requirements 9 and 12.

## 2. Scope

This policy applies to:

- All point-of-sale (POS) terminals and payment acceptance devices
- All unattended payment terminals (kiosks, vending machines, fuel dispensers)
- All mobile point-of-sale (mPOS) devices
- All PIN entry devices (PEDs)
- All systems that process card-present transactions
- All personnel who install, service, or interact with POI devices
- All locations where POI devices are deployed

## 3. Policy

**[Company Name]** shall protect all point-of-interaction devices against tampering and substitution to prevent the capture of cardholder data through skimming or other attacks.

### 3.1 POI Device Standards

Only approved POI devices shall be used for payment acceptance.

**Device Requirements:**
- Devices are listed on the PCI SSC approved PTS devices list
- Devices use current, non-expired PTS approval (SRED or POI)
- Devices support point-to-point encryption (P2PE) where available
- Devices meet payment brand requirements for transaction type

**Device Approval:**
- New device types require security review before deployment
- Device approval is documented and maintained
- Approved device list is maintained by the PCI Program Manager
- Non-standard devices require CISO approval with compensating controls

**Device Procurement:**
- Devices are purchased only from authorized sources
- Supply chain integrity is verified
- Devices are shipped securely with tamper-evident packaging
- Device serial numbers are verified upon receipt

### 3.2 POI Device Inventory

A comprehensive inventory of all POI devices shall be maintained per PCI DSS 9.5.1.

**Inventory Requirements:**
- Device make, model, and serial number
- Location of deployment
- Date of deployment
- Current software/firmware version
- Last inspection date
- Assigned device ID

**Inventory Maintenance:**
- Inventory is updated upon device deployment, movement, or retirement
- Inventory is reconciled at least annually
- Discrepancies trigger investigation and incident response
- Inventory is protected as confidential information

**Tracking:**
- Device movements require documented approval
- Chain of custody is maintained for device transfers
- Lost or stolen devices are reported immediately
- Device retirement follows secure disposal procedures

### 3.3 Physical Security of POI Devices

POI devices shall be physically protected against tampering and substitution per PCI DSS 9.5.

**Tamper Protection:**
- Devices are secured to prevent unauthorized removal
- Tamper-evident seals or locks are applied where appropriate
- Devices are positioned to minimize access to connection cables
- Surveillance coverage is provided where feasible

**Substitution Prevention:**
- Devices are inspected for evidence of tampering before use
- Staff are trained to recognize signs of device substitution
- Device appearance is documented for comparison
- Unexpected devices are reported and investigated

**Environmental Controls:**
- Devices are protected from environmental damage
- Devices are not left unattended during business hours
- After-hours storage follows security requirements
- Portable devices are secured when not in use

### 3.4 POI Device Inspection

Periodic inspection of POI devices shall detect tampering or substitution per PCI DSS 9.5.1.

**Inspection Frequency:**
- Devices in high-risk locations: inspected **[Frequency, e.g., daily]**
- Standard retail locations: inspected **[Frequency, e.g., weekly]**
- Unattended terminals: inspected **[Frequency, e.g., monthly]**
- Risk-based adjustments per targeted risk analysis

**Inspection Procedures:**
- Compare device to reference images
- Check for unauthorized attachments or overlays
- Verify serial number matches inventory
- Check tamper-evident seals/labels
- Examine card reader slot and keypad
- Check cable connections for unauthorized devices

**Inspection Documentation:**
- Inspections are logged with date, time, inspector, and results
- Checklists are used for consistency
- Anomalies are documented and reported
- Inspection records are retained for **[Number, e.g., 12]** months

**Training:**
- Personnel performing inspections are trained on procedures per PCI DSS 9.5.1.3
- Training includes recognition of tampering techniques
- Training is refreshed annually
- Training completion is documented

### 3.5 Unattended Payment Terminal Security

Unattended payment terminals require additional security controls.

**Physical Protection:**
- Terminals are housed in secure, tamper-resistant enclosures
- Enclosures are locked and access is controlled
- Video surveillance monitors terminals where feasible
- Terminals are positioned to prevent unauthorized access

**Remote Monitoring:**
- Terminals are monitored for availability and anomalies
- Alerts are generated for offline terminals
- Transaction patterns are monitored for skimming indicators
- Remote diagnostics allow for security verification

**Service Access:**
- Service technicians are verified before access
- Service visits are scheduled and logged
- Technicians are accompanied where feasible
- Post-service inspection is performed

### 3.6 Mobile POS (mPOS) Security

Mobile point-of-sale solutions shall meet specific security requirements.

**Device Requirements:**
- mPOS card readers are PCI PTS approved
- Mobile devices running mPOS apps meet security requirements
- Payment applications are PA-DSS or PCI SSS validated
- Device pairing uses secure methods

**Mobile Device Security:**
- Mobile devices are enrolled in mobile device management (MDM)
- Devices are configured per security baseline
- Only approved applications are installed
- Devices are updated with security patches

**Operational Controls:**
- Devices are assigned to specific users
- Devices are secured when not in use
- Lost or stolen devices are reported immediately
- Remote wipe capability is enabled

### 3.7 POS System Security

Point-of-sale systems shall be secured per PCI DSS requirements.

**System Configuration:**
- POS systems run on hardened operating systems
- Unnecessary services and software are disabled
- Anti-malware protection is implemented
- Systems are patched per vulnerability management procedures

**Network Segmentation:**
- POS systems are segmented from other networks
- Only necessary network traffic is permitted
- Segmentation is validated through testing
- Wireless POS uses WPA3 or WPA2 with strong keys

**Application Security:**
- POS applications are PA-DSS or PCI SSS validated where applicable
- Applications are obtained from trusted sources
- Application integrity is verified
- Application updates are tested before deployment

### 3.8 Skimming Prevention

Controls shall prevent and detect skimming attacks.

**Prevention Measures:**
- Regular device inspections per Section 3.4
- Staff training on skimming recognition
- Point-to-point encryption (P2PE) implementation
- EMV chip preference over magnetic stripe

**Detection Measures:**
- Unusual transaction patterns may indicate skimming
- Customer complaints are investigated
- Payment brand alerts are monitored
- Industry threat intelligence is reviewed

**Response:**
- Suspected skimming triggers immediate device isolation
- Incident response procedures are initiated
- Law enforcement is notified as appropriate
- Payment brands are notified per their requirements

### 3.9 Service and Repair

POI device service and repair shall maintain security.

**Authorized Service:**
- Repairs are performed only by authorized personnel
- Third-party service providers are vetted
- Service provider employees are verified
- Service activity is logged

**On-Site Service:**
- Service technicians present valid identification
- Visits are verified against scheduled appointments
- Staff observe service activities
- Devices are inspected after service

**Off-Site Repair:**
- Device chain of custody is documented
- Devices are shipped securely
- Repaired devices are inspected before deployment
- Devices are tested for proper function

### 3.10 Device Retirement

POI devices shall be securely retired and disposed.

**Retirement Procedures:**
- Device is removed from inventory
- All keys and sensitive data are securely erased
- Device is physically destroyed or returned to manufacturer
- Retirement is documented

**Data Destruction:**
- Any stored cardholder data is securely deleted
- Encryption keys are destroyed
- Audit logs are archived per retention requirements
- Destruction is verified and documented

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 12.3.4 |
| 3.1 | PCI SSC | PTS Device Security Requirements |
| 3.2, 3.3 | PCI DSS v4.0 | 9.5.1 |
| 3.4 | PCI DSS v4.0 | 9.5.1.2, 9.5.1.3 |
| 3.5 | PCI DSS v4.0 | 9.5.1.2.1 |
| 3.6 | PCI DSS v4.0 | 9.5.1 |
| 3.7 | PCI DSS v4.0 | 2.2, 6.2, 11.3 |
| 3.8 | PCI DSS v4.0 | 9.5.1, 12.10.1 |
| 3.9 | PCI DSS v4.0 | 9.5.1 |
| 3.10 | PCI DSS v4.0 | 9.4.6 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **EMV** | A global standard for chip-based payment cards providing enhanced security over magnetic stripe. |
| **mPOS (Mobile Point of Sale)** | A payment acceptance solution using a mobile device (smartphone/tablet) with a card reader attachment. |
| **Point-of-Interaction (POI)** | The initial point where data is read from a card or payment instrument. |
| **Point-to-Point Encryption (P2PE)** | A standard that encrypts card data from the point of interaction until it reaches the secure decryption environment. |
| **POS (Point of Sale)** | The location and system where a retail transaction is completed. |
| **PTS (PIN Transaction Security)** | PCI SSC program for validating the security of POI devices. |
| **Skimming** | The unauthorized capture of card data from a payment device through overlay devices or internal modifications. |
| **Tamper-Evident** | A device or seal that shows visible evidence if tampering has been attempted. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Approve POI security controls. Authorize device exceptions. Oversee security incidents. |
| **PCI Program Manager** | Maintain device inventory. Ensure PCI DSS compliance. Coordinate inspections. Manage device approval. |
| **IT Security Team** | Configure device security. Monitor for tampering indicators. Investigate security incidents. Conduct risk assessments. |
| **Operations/Retail Team** | Perform daily device inspections. Report anomalies. Secure devices during operations. |
| **Store/Location Managers** | Ensure inspection schedules are followed. Verify service technicians. Report missing devices. |
| **Service Technicians** | Follow approved service procedures. Document service activities. Report security concerns. |

