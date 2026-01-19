# Technical Review: PAY-POL-005 - Point-of-Interaction Security Policy

**Reviewer**: Fintech Controls SME (Stage 4)
**Review Date**: 2026-01-13
**Document Version**: 1.0

## Review Summary

| Aspect | Status | Notes |
|--------|--------|-------|
| Payment Security Accuracy | Pass | POI security comprehensive |
| PCI DSS v4.0 Alignment | Pass | Requirement 9.5 thoroughly addressed |
| Infrastructure Controls | Pass | POS system hardening included |
| Fraud/Monitoring Controls | Pass | Skimming detection covered |
| Overall | **Pass** | Ready for compliance review |

## Critical Issues

None identified.

## Major Issues

None identified.

## Minor Issues

| # | Section | Issue | Recommendation |
|---|---------|-------|----------------|
| m-1 | 3.1 | PTS device requirements correct but doesn't mention SRED module version requirements | Add "SRED module version must not be expired" |
| m-2 | 3.6 | mPOS references PA-DSS which is retired; should be PCI SSS (Software Security Standard) | Update "PA-DSS or PCI SSS validated" to "PCI SSS/SSF validated" |
| m-3 | 3.7 | POS hardening mentions "anti-malware" generically | Specify endpoint protection requirements including EDR capabilities |
| m-4 | 3.7 | Wireless POS mentions WPA3 or WPA2 - WPA2 should note "with AES-CCMP only" | Clarify WPA2 must use AES-CCMP, not TKIP |
| m-5 | 3.8 | P2PE mentioned as prevention measure but no reference to PCI P2PE validation | Add "PCI P2PE validated solutions preferred" |

## PCI DSS v4.0 Control Verification

| Section | Claimed Requirement | Version | Verification | Notes |
|---------|---------------------|---------|--------------|-------|
| 3.1 | 12.3.4 | v4.0 | ✓ Verified | Device standards documented |
| 3.2, 3.3 | 9.5.1 | v4.0 | ✓ Verified | Inventory and physical security |
| 3.4 | 9.5.1.2, 9.5.1.3 | v4.0 | ✓ Verified | Inspection procedures complete |
| 3.5 | 9.5.1.2.1 | v4.0 | ✓ Verified | Unattended terminal controls |
| 3.7 | 2.2, 6.2, 11.3 | v4.0 | ✓ Verified | System security requirements |
| 3.10 | 9.4.6 | v4.0 | ✓ Verified | Secure disposal |

### POI Device Security

| Aspect | Assessment |
|--------|------------|
| PTS device requirement | ✓ Correct - must be on PCI SSC list |
| SRED/POI approval | ✓ Mentioned - current approval required |
| P2PE support | ✓ Mentioned where available |
| EMV preference | ✓ Correctly prioritized over magstripe |

## Infrastructure Security Review

### POS System Hardening

| Control | Implementation | Assessment |
|---------|----------------|------------|
| OS hardening | Required per policy | ✓ Correct |
| Unnecessary services | Disabled | ✓ Correct |
| Anti-malware | Implemented | ⚠ Consider EDR specification |
| Patching | Per vuln management | ✓ Correct |

### Network Segmentation for POS

| Control | Implementation | Assessment |
|---------|----------------|------------|
| Segment isolation | Required | ✓ Correct |
| Traffic restriction | Only necessary traffic | ✓ Correct |
| Segmentation testing | Validated through testing | ✓ Correct |
| Wireless security | WPA3/WPA2 with strong keys | ⚠ Clarify AES-CCMP for WPA2 |

### Mobile POS Security

| Control | Implementation | Assessment |
|---------|----------------|------------|
| Card reader | PCI PTS approved | ✓ Correct |
| MDM enrollment | Required | ✓ Correct |
| Application validation | PCI SSS reference | ⚠ Update PA-DSS reference |
| Remote wipe | Enabled | ✓ Correct |

## Technical Recommendations

### Implementation Guidance
- Section 3.4: Add reference images best practices (multiple angles, lighting)
- Section 3.6: Include Bluetooth security requirements for mPOS pairing
- Section 3.7: Add specific baseline configuration references (CIS Benchmarks)

### Technology Updates
- Update PA-DSS references to PCI SSS/SSF throughout
- Add Android/iOS hardening guidelines for mPOS devices

### Skimming Prevention
- Policy is comprehensive on physical detection
- Consider adding transaction pattern analysis for skimming detection

### Additional Controls
- Add USB port disabling for POS systems
- Include secure boot requirements for POS devices
- Add tampering detection sensors for high-value terminals

## Approval Status

- [x] **Approved** - Ready for compliance review
- [ ] **Approved with minor changes** - Can proceed, address minors in parallel
- [ ] **Requires revision** - Must address critical/major issues before proceeding
