# POI Device Inspection Procedure (PAY-PROC-002)

### 1. Purpose

To define the process for conducting periodic inspections of point-of-interaction (POI) devices to detect tampering or unauthorized substitution, ensuring the integrity of payment acceptance devices per PCI DSS 9.5.1.

### 2. Scope

This procedure applies to all POI devices including:

- Point-of-sale (POS) terminals
- PIN entry devices (PEDs)
- Unattended payment terminals (kiosks, fuel dispensers)
- Mobile POS (mPOS) devices
- Any device that reads payment card data

### 3. Overview

This procedure outlines the systematic inspection of POI devices per PCI DSS 9.5.1.2. Personnel inspect devices for signs of tampering, verify serial numbers against inventory, and document findings. Anomalies trigger immediate escalation and incident response procedures.

### 4. Procedure

#### 4.1 Scheduled Inspections

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Location Staff / Technician | Retrieves the POI device inspection checklist and reference images for devices at the location. |
| **2** | Location Staff / Technician | Visually inspects each device for: |
| | | - Unusual attachments or overlays on card slot |
| | | - Loose or damaged components |
| | | - Wires or devices attached to cables |
| | | - Evidence of tampering with seals or screws |
| | | - Changes in appearance from reference images |
| **3** | Location Staff / Technician | Verifies that the device serial number matches inventory records. |
| **4** | Location Staff / Technician | Checks that tamper-evident seals (if applicable) are intact and match documented seal numbers. |
| **5** | Location Staff / Technician | Tests device functionality (card read, keypad response). |
| **6** | Location Staff / Technician | Documents the inspection in the inspection log including: |
| | | - Date and time |
| | | - Inspector name |
| | | - Device ID and location |
| | | - Inspection results (pass/fail) |
| | | - Any anomalies observed |
| **7** | Location Staff / Technician | If anomalies are found, immediately proceeds to Section 4.2. |

#### 4.2 Anomaly Response

| **Step** | **Who** | **What** |
|----------|---------|----------|
| **1** | Location Staff / Technician | Immediately removes the suspicious device from service. |
| **2** | Location Staff / Technician | Does NOT attempt to disassemble or further examine the device. |
| **3** | Location Staff / Technician | Secures the device in a safe location and prevents further use. |
| **4** | Location Staff / Technician | Immediately notifies IT Security Team and Location Manager. |
| **5** | IT Security Team | Initiates incident response per RES-PROC-001. |
| **6** | IT Security Team | Coordinates forensic examination if required. |
| **7** | IT Security Team | Notifies law enforcement if skimming is confirmed. |
| **8** | PCI Program Manager | Notifies payment brands and acquiring bank if CHD compromise is suspected per PCI DSS 12.10.5. |

#### 4.3 Inspection Scheduling

| **Device Type** | **Minimum Frequency** | **Notes** |
|-----------------|----------------------|-----------|
| High-traffic POS | Daily | Before opening |
| Standard POS | Weekly | Documented schedule |
| Unattended terminals | Monthly | Plus after any service |
| mPOS devices | Before each use | User responsibility |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
|-----------------------|------------------------|-----------------------|
| **4.1** | PCI DSS v4.0 | 9.5.1.2, 9.5.1.2.1 |
| **4.2** | PCI DSS v4.0 | 12.10.1, 12.10.5 |
| **4.3** | PCI DSS v4.0 | 9.5.1.2 |
| **4.1-4.3** | SOC 2 TSC | CC6.4 |

### 6. Artifact(s)

- Completed inspection checklists
- Inspection logs with date/time/inspector
- Reference images for each device type
- Anomaly reports and incident tickets
- Training completion records

### 7. Definitions

| **Term** | **Definition** |
|----------|----------------|
| **Skimming** | The unauthorized capture of card data from a payment device through overlay devices or internal modifications. |
| **Overlay Device** | A fraudulent device placed over a legitimate card reader to capture card data. |
| **Tamper-Evident Seal** | A seal that shows visible evidence if tampering has been attempted. |
| **POI (Point of Interaction)** | The initial point where data is read from a card or payment instrument. |

### 8. Responsibilities

| **Role** | **Responsibility** |
|----------|-------------------|
| **Location Staff / Technician** | Perform scheduled inspections. Document findings. Report anomalies immediately. |
| **Location Manager** | Ensure inspection schedules are followed. Verify staff training. Escalate issues. |
| **IT Security Team** | Respond to anomalies. Coordinate investigations. Update procedures based on threats. |
| **PCI Program Manager** | Maintain inspection schedules. Track compliance. Report to payment brands if required. |

