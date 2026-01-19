# System Configuration and Hardening Policy (OP-POL-006)

## 1. Objective

This policy establishes requirements for applying secure configurations to all system components in the cardholder data environment (CDE) and connected systems in accordance with PCI DSS v4.0 Requirement 2, SOC 2, and GLBA Safeguards Rule requirements. This policy ensures that systems are configured securely, vendor defaults are changed, and unnecessary services are removed to reduce the attack surface.

## 2. Scope

This policy applies to all **[Company Name]** workforce members responsible for deploying, configuring, and maintaining system components. It encompasses:

- All system components within the cardholder data environment (CDE)
- All systems connected to the CDE
- All systems storing or processing customer financial information
- Servers (physical and virtual), workstations, network devices
- Operating systems, databases, applications
- Cloud resources and container environments
- Wireless environments

## 3. Policy

**[Company Name]** implements secure configuration standards for all system components to reduce security vulnerabilities and protect the CDE per PCI DSS Requirement 2.

### 3.1 Configuration Standards

Configuration standards are developed, implemented, and maintained for all system components per PCI DSS 2.2.1.

**Standard Requirements:**
- Cover all system components
- Address all known security vulnerabilities
- Consistent with industry-accepted hardening standards or vendor recommendations
- Updated as new vulnerability issues are identified (per PCI DSS 6.3.1)
- Applied when new systems are configured
- Verified before or immediately after connecting to production

**Standard Sources:**
Industry-accepted hardening guides are used as baselines:
- Center for Internet Security (CIS) Benchmarks
- NIST security configuration guides
- Cloud Security Alliance guidance
- Vendor security recommendations
- DISA Security Technical Implementation Guides (STIGs)

### 3.2 Vendor Default Management

Vendor default accounts and settings are managed to eliminate common attack vectors per PCI DSS 2.2.2.

**Default Account Requirements:**
If vendor default accounts will be used:
- Default password changed per password policy (minimum 12 characters per AC-POL-001)
- Account permissions reviewed and restricted to minimum necessary

If vendor default accounts will not be used:
- Account removed or disabled
- Removal/disabling verified and documented

**Default Settings:**
- Default credentials changed before system enters production
- Unnecessary default users and groups removed
- Default encryption keys changed (especially for wireless environments)
- SNMP community strings changed from defaults
- Sample applications and scripts removed

### 3.3 Function Separation

Primary functions requiring different security levels are properly managed per PCI DSS 2.2.3.

**Separation Requirements:**
One of the following approaches is implemented:
- Only one primary function exists on a system component, OR
- Primary functions with differing security levels are isolated from each other, OR
- Primary functions on the same system are all secured to the highest required level

**Examples:**
- Web servers, database servers, and application servers on separate systems
- CDE systems not co-located with less secure systems
- Virtualization or containerization used to isolate functions where appropriate

### 3.4 Unnecessary Functionality Removal

Only necessary services, protocols, daemons, and functions are enabled per PCI DSS 2.2.4.

**Requirements:**
- Necessary services documented in configuration standards
- Unnecessary functionality removed or disabled
- Only required functionality enabled

**Removal Targets:**
- Unused services and daemons
- Unnecessary protocols
- Unused device drivers
- Unneeded default features
- Sample files, scripts, and applications
- Unnecessary interfaces (USB, Bluetooth where not needed)
- Unused web server modules

### 3.5 Insecure Services Mitigation

Where insecure services, protocols, or daemons are necessary, they are documented and secured per PCI DSS 2.2.5.

**Requirements:**
If any insecure services, protocols, or daemons are present:
- Business justification documented
- Additional security features documented and implemented
- Risk formally accepted by management

**Mitigation Examples:**
- SSH instead of Telnet
- SFTP instead of FTP
- TLS encryption for necessary legacy protocols
- Network segmentation to limit exposure
- Monitoring and logging of insecure service usage

### 3.6 System Security Parameters

System security parameters are configured to prevent misuse per PCI DSS 2.2.6.

**Configuration Areas:**
- Audit and logging settings enabled
- Account lockout parameters configured
- Session timeout settings implemented
- Error message verbosity minimized (no sensitive data exposure)
- File permissions appropriately restricted
- Registry/system settings secured

**Cloud-Specific Parameters:**
- Secure settings for cloud management portals
- Infrastructure-as-code templates include security settings
- Cloud-native security features enabled
- Resource policies properly configured

### 3.7 Administrative Access Encryption

All non-console administrative access uses strong cryptography per PCI DSS 2.2.7.

**Requirements:**
- All remote administrative access encrypted using strong cryptography
- Insecure remote login services disabled (Telnet, unencrypted VNC)
- SSH, RDP with TLS, HTTPS required for remote administration
- Strong cryptography implemented per industry best practices

**Protocols:**
- SSH version 2 for command-line administration
- HTTPS with TLS 1.2+ for web-based administration
- IPsec or TLS VPN for remote console access
- RDP with Network Level Authentication

### 3.8 Wireless Configuration

Wireless environments connected to the CDE are securely configured per PCI DSS 2.3.

**Wireless Default Changes (per PCI DSS 2.3.1):**
For wireless environments connected to the CDE:
- Default wireless encryption keys changed at installation
- Default passwords on access points changed
- SNMP defaults changed
- Other security-related vendor defaults addressed

**Wireless Encryption Key Changes (per PCI DSS 2.3.2):**
Wireless encryption keys are changed:
- Whenever personnel with key knowledge leave or change roles
- Whenever a key is suspected or known to be compromised

**Wireless Security:**
- WPA3 or WPA2-Enterprise preferred
- SSID broadcast disabled where appropriate
- Access point firmware kept current
- Wireless traffic into CDE controlled per SEC-POL-009

### 3.9 Configuration Baseline Management

Secure configuration baselines are maintained and applied consistently.

**Baseline Requirements:**
- Documented baseline for each system type
- Baselines stored in version control or configuration management system
- Changes to baselines follow change management (ENG-POL-002)
- Baselines reviewed and updated at least annually

**Baseline Application:**
- New systems built from approved baselines
- Configuration verification before production deployment
- Automated configuration deployment where feasible
- Deviations require documented justification and approval

### 3.10 Configuration Monitoring

System configurations are monitored for unauthorized changes.

**Monitoring Requirements:**
- File integrity monitoring (FIM) on critical system files per SEC-POL-007
- Configuration drift detection identifies unauthorized changes
- Alerts generated for configuration deviations
- Changes investigated per incident response procedures

**Compliance Verification:**
- Periodic scans verify configuration compliance
- Exceptions identified and remediated
- Compliance status reported to management

### 3.11 Container and Cloud Configuration

Container images and cloud resources follow secure configuration standards.

**Container Security:**
- Container images built from trusted, minimal base images
- Images scanned for vulnerabilities before deployment
- Configuration follows CIS benchmarks for container platforms
- Runtime security controls implemented

**Cloud Configuration:**
- Cloud resources provisioned using infrastructure-as-code
- Security groups and network policies follow least privilege
- Cloud security posture management (CSPM) tools deployed
- Misconfiguration alerts investigated promptly

### 3.12 Database Configuration

Databases are configured securely with appropriate hardening.

**Database Security:**
- Default accounts disabled or passwords changed
- Unnecessary features and sample data removed
- Encryption enabled for sensitive data at rest
- Audit logging enabled for privileged actions
- Network access restricted to authorized sources

## 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1 | PCI DSS v4.0 | 2.2.1 |
| 3.1 | SOC 2 TSC | CC6.1 |
| 3.2 | PCI DSS v4.0 | 2.2.2 |
| 3.3 | PCI DSS v4.0 | 2.2.3 |
| 3.4 | PCI DSS v4.0 | 2.2.4 |
| 3.5 | PCI DSS v4.0 | 2.2.5 |
| 3.6 | PCI DSS v4.0 | 2.2.6 |
| 3.7 | PCI DSS v4.0 | 2.2.7 |
| 3.8 | PCI DSS v4.0 | 2.3.1, 2.3.2 |
| 3.10 | PCI DSS v4.0 | 11.5.2 |

## 5. Definitions

| **Term** | **Definition** |
|---|---|
| **Cardholder Data Environment (CDE)** | The people, processes, and technologies that store, process, or transmit cardholder data or sensitive authentication data. |
| **Configuration Baseline** | A documented set of specifications for a system that has been formally approved and against which changes are managed. |
| **Configuration Standards** | Documents that define how systems must be configured to meet security requirements. |
| **Hardening** | The process of securing a system by reducing its surface of vulnerability through configuring security settings and removing unnecessary functionality. |
| **Infrastructure-as-Code (IaC)** | Managing and provisioning infrastructure through machine-readable configuration files rather than manual processes. |
| **System Component** | Any network component, server, computing device, or application within or connected to the CDE. |
| **Vendor Default** | Settings, accounts, or configurations that are pre-configured by a vendor when a product is shipped. |

## 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Chief Information Security Officer (CISO)** | Own configuration policy. Approve configuration standards. Ensure hardening meets compliance requirements. |
| **IT Security Team** | Develop and maintain configuration standards. Review configuration for security. Monitor configuration compliance. Assess new system types for hardening. |
| **System Administrators** | Apply configuration standards to systems. Maintain configuration baselines. Remove unnecessary functionality. Implement security parameters. |
| **Network Operations** | Configure network devices per standards. Remove default settings. Implement wireless security. Maintain network device baselines. |
| **PCI Program Manager** | Ensure configurations meet PCI DSS requirements. Track configuration compliance. Coordinate with QSA on configuration assessments. |
| **Cloud/Platform Team** | Develop cloud configuration standards. Implement IaC templates. Monitor cloud configuration compliance. Manage container security. |

