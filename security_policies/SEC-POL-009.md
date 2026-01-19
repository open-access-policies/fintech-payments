# Network Security Policy (SEC-POL-009)

## 1. Objective

This policy establishes requirements for installing and maintaining network security controls (NSCs) to protect the cardholder data environment (CDE) and customer financial information in accordance with PCI DSS v4.0 Requirement 1, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that network traffic to and from the CDE is controlled, unauthorized access is prevented, and network security controls are properly configured and maintained.

## 2. Scope

This policy applies to all **[Company Name]** workforce members responsible for designing, implementing, and maintaining network infrastructure. It encompasses:

- All network security controls (firewalls, routers, cloud network controls, etc.)
- All systems within the cardholder data environment (CDE)
- All systems connected to the CDE
- All connections between trusted and untrusted networks
- Wireless networks and wireless access points
- Network segmentation controls

## 3. Policy

**[Company Name]** implements network security controls to protect the CDE from unauthorized access and to control network traffic per PCI DSS Requirement 1.

### 3.1 Network Security Control Standards

Configuration standards for NSC rulesets are defined, implemented, and maintained per PCI DSS 1.2.1.

**Configuration Standard Requirements:**
- Standards cover all types of NSCs in the environment
- Standards define acceptable protocols, ports, and configuration requirements
- Standards address requirements for CDE protection
- Standards are documented and kept up to date

**NSC Types Covered:**
- Physical and virtual firewalls
- Routers with access control lists
- Cloud virtual networks and security groups
- Software-defined networking controls
- Host-based firewalls
- Container network policies

### 3.2 Change Management for Network Controls

All changes to network connections and NSC configurations follow formal change control per PCI DSS 1.2.2.

**Change Control Requirements:**
- Changes are approved before implementation
- Changes are documented with business justification
- Changes are tested to verify they do not adversely impact security
- Network documentation is updated after changes
- Changes follow the Change Management Policy (ENG-POL-002) and PCI DSS 6.5.1

**Change Types Requiring Approval:**
- New network connections to or from the CDE
- Modifications to firewall rules or access control lists
- Changes to network topology affecting the CDE
- Product upgrades or replacements of NSCs

### 3.3 Network Documentation

Accurate network and data-flow diagrams are maintained per PCI DSS 1.2.3 and 1.2.4.

**Network Diagram Requirements:**
- Shows all connections between the CDE and other networks
- Includes wireless network connections
- Documents all system components within the CDE
- Clearly labels network segments and security zones
- Identifies all NSCs with unique identifiers
- Documents out-of-scope areas
- Includes date of last update and approver

**Data-Flow Diagram Requirements:**
- Shows all account data flows across systems and networks
- Updated upon changes to the environment
- Documents all processing flows (authorization, capture, settlement)
- Identifies acceptance channels (card-present, card-not-present, e-commerce)
- Shows where account data is transmitted, processed, and stored

### 3.4 Services, Protocols, and Ports

All services, protocols, and ports allowed are identified, approved, and justified per PCI DSS 1.2.5.

**Documentation Requirements:**
- List of all allowed services, protocols, and ports
- Business justification for each allowed service
- Approval by personnel independent of those managing configuration
- Security risk associated with each service understood

**Insecure Services (per PCI DSS 1.2.6):**
For any insecure services, protocols, or ports in use:
- Business justification is documented
- Security features are defined and implemented to mitigate risk
- Risk is formally accepted by management

### 3.5 NSC Configuration Review

Configurations of NSCs are reviewed to confirm relevance and effectiveness per PCI DSS 1.2.7.

**Review Frequency:**
- At least once every six months
- After significant changes to the network

**Review Process:**
- Verify all rules and configurations have valid business justification
- Remove or update rules no longer supported by business need
- Confirm configurations match approved documentation
- Document review findings and actions taken

**Configuration File Security (per PCI DSS 1.2.8):**
- Configuration files are secured from unauthorized access
- Files are kept consistent with active network configurations

### 3.6 CDE Traffic Restriction

Network access to and from the CDE is restricted per PCI DSS 1.3.

**Inbound Traffic (per PCI DSS 1.3.1):**
- Inbound traffic to the CDE is limited to only traffic that is necessary
- All other traffic is specifically denied (explicit or implicit deny)

**Outbound Traffic (per PCI DSS 1.3.2):**
- Outbound traffic from the CDE is limited to only traffic that is necessary
- All other traffic is specifically denied

**Wireless Network Controls (per PCI DSS 1.3.3):**
- NSCs are installed between all wireless networks and the CDE
- All wireless traffic into the CDE is denied by default
- Only wireless traffic with authorized business purpose is allowed

### 3.7 Trusted and Untrusted Network Controls

Network connections between trusted and untrusted networks are controlled per PCI DSS 1.4.

**NSC Implementation (per PCI DSS 1.4.1):**
- NSCs are implemented between all trusted and untrusted networks
- DMZ architecture separates public-facing systems from internal systems

**Inbound Traffic Controls (per PCI DSS 1.4.2):**
- Inbound traffic from untrusted networks is restricted to:
  - Communications with authorized publicly accessible services
  - Stateful responses to communications initiated by trusted network components
- All other traffic is denied

**Anti-Spoofing (per PCI DSS 1.4.3):**
- Anti-spoofing measures detect and block forged source IP addresses
- Internal addresses originating from external networks are blocked

**CHD Storage Protection (per PCI DSS 1.4.4):**
- System components storing cardholder data are not directly accessible from untrusted networks

**IP Address Disclosure (per PCI DSS 1.4.5):**
- Disclosure of internal IP addresses and routing information is limited to authorized parties
- Network Address Translation (NAT) or proxy servers are used where appropriate

### 3.8 Dual-Network Device Controls

Risks from computing devices connecting to both untrusted networks and the CDE are mitigated per PCI DSS 1.5.1.

**Security Controls:**
- Specific configuration settings prevent threats from being introduced
- Security controls are actively running on devices
- Controls are not alterable by users unless authorized by management

**Device Types:**
- Company-owned laptops and desktops
- Employee-owned devices (BYOD) with CDE access
- Mobile devices accessing the CDE

**Required Controls:**
- Personal firewall software or equivalent protection
- Endpoint detection and response (EDR) solutions
- VPN requirements for CDE access
- Configuration management ensuring controls cannot be disabled

### 3.9 Network Segmentation

Network segmentation is implemented to isolate the CDE from other networks where applicable.

**Segmentation Requirements:**
- Segmentation controls are properly configured to isolate the CDE
- Segmentation is validated through penetration testing per SEC-POL-007
- Segmentation controls are documented in network diagrams

**Segmentation Testing (per PCI DSS 11.4.5):**
- Penetration tests validate segmentation controls at least annually
- Testing confirms CDE is isolated from out-of-scope systems
- Service providers test segmentation at least every six months

### 3.10 Wireless Security

Wireless environments connected to the CDE are securely configured per PCI DSS 2.3.

**Wireless Defaults (per PCI DSS 2.3.1):**
For wireless environments connected to the CDE:
- Default wireless encryption keys are changed at installation
- Passwords on wireless access points are changed
- SNMP defaults are changed
- Other security-related vendor defaults are addressed

**Wireless Encryption Key Changes (per PCI DSS 2.3.2):**
Wireless encryption keys are changed:
- Whenever personnel with key knowledge leave or change roles
- Whenever a key is suspected or known to be compromised

**Wireless Access Point Monitoring (per PCI DSS 11.2.1, 11.2.2):**
- Testing for unauthorized wireless access points at least quarterly
- Inventory of authorized wireless access points maintained
- Business justification documented for all authorized access points
- Unauthorized access points addressed per incident response procedures

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 1.2.1 |
| 3.2 | PCI DSS v4.0 | 1.2.2, 6.5.1 |
| 3.3 | PCI DSS v4.0 | 1.2.3, 1.2.4 |
| 3.4 | PCI DSS v4.0 | 1.2.5, 1.2.6 |
| 3.5 | PCI DSS v4.0 | 1.2.7, 1.2.8 |
| 3.6 | PCI DSS v4.0 | 1.3.1, 1.3.2, 1.3.3 |
| 3.7 | PCI DSS v4.0 | 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.4.5 |
| 3.7 | SOC 2 TSC | CC6.1, CC6.6 |
| 3.8 | PCI DSS v4.0 | 1.5.1 |
| 3.9 | PCI DSS v4.0 | 11.4.5, 11.4.6 |
| 3.10 | PCI DSS v4.0 | 2.3.1, 2.3.2, 11.2.1, 11.2.2 |
| 3.10 | GLBA Safeguards | § 314.4(c)(4) |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Network Security Control (NSC)** | Network policy enforcement points that control network traffic between network segments based on pre-defined policies or rules. Includes firewalls, routers with ACLs, and cloud network controls. |
| **Trusted Network** | A network that is within the organization's ability to control and assess for security, such as internal corporate networks. |
| **Untrusted Network** | A network that is outside the organization's ability to control, including the Internet, third-party networks, and out-of-scope corporate networks. |
| **DMZ (Demilitarized Zone)** | A network segment that provides a buffer zone between trusted and untrusted networks, typically hosting publicly accessible services. |
| **Network Segmentation** | Isolating the CDE from other networks to reduce PCI DSS scope and improve security posture. |
| **Anti-Spoofing** | Controls that detect and block network packets with forged source IP addresses. |
| **Stateful Inspection** | Firewall technology that tracks the state of network connections and only allows return traffic for established sessions. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own network security policy. Approve network architecture. Ensure compliance with PCI DSS network requirements. |
| **Network Operations** | Implement and maintain network security controls. Manage firewall rules and configurations. Maintain network documentation. Perform NSC configuration reviews. |
| **IT Security Team** | Define NSC configuration standards. Review and approve firewall rule changes. Conduct network security assessments. Monitor for unauthorized wireless access points. |
| **PCI Program Manager** | Ensure network controls meet PCI DSS requirements. Maintain CDE scope documentation. Coordinate segmentation testing. Track network-related PCI DSS compliance. |
| **System Administrators** | Implement host-based firewall configurations. Ensure endpoint devices meet security control requirements. Report network security issues. |

