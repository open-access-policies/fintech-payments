# Technical Review: OP-PROC-006 - Background Check Procedure

**Reviewer**: Fintech Controls SME (Stage 4)
**Review Date**: 2026-01-13
**Document Version**: 1.0

## Review Summary

| Category | Status | Notes |
|----------|--------|-------|
| Technical Accuracy | Pass | Comprehensive screening workflow |
| PCI DSS Alignment | Pass | 12.7.1 addressed |
| Implementation Feasibility | Pass | Practical tiered approach |
| Security Architecture | Pass | Risk-based screening levels |

## Detailed Findings

### Critical Issues
None identified.

### Major Issues
None identified.

### Minor Issues

| ID | Section | Issue | Recommendation | Priority |
|----|---------|-------|----------------|----------|
| OP6-001 | 4 Step 2 | Key custodian role screening not explicitly mentioned | Add key custodian to enhanced screening | Low |

## Technical Validation

### PCI DSS v4.0 Coverage
- **Requirement 12.7.1**: Background checks before hire for CDE access - Enhanced screening tier

### Screening Tiers
- **Standard**: Criminal, employment, education verification
- **Enhanced (CDE/NPI)**: Standard + credit check, additional references
- **Financial (BSA/AML)**: Enhanced + OFAC screening

### CDE-Specific Requirements
- Enhanced screening for CDE access roles
- Credit check where legally permitted
- Additional reference checks
- PCI DSS compliance documentation

### GLBA Integration
- § 314.4(e): Personnel screening requirements

### FCRA Compliance
- Written consent required
- Adverse action process defined
- Pre-adverse and final adverse notices

## Recommendation

**APPROVED** - Solid background check procedure with appropriate PCI DSS 12.7.1 tiered screening approach.

---

**Reviewer Signature**: Fintech Controls SME
**Date**: 2026-01-13
