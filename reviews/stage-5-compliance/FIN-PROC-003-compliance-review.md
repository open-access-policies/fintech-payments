# Compliance Review: FIN-PROC-003 - OFAC Screening Procedure

**Reviewer**: PCI/GLBA/AML Regulatory SME (Stage 5)
**Review Date**: 2026-01-13
**Document Version**: 1.0

## Review Summary

| Framework | Status | Notes |
|-----------|--------|-------|
| OFAC Regulations | Pass | 31 CFR Parts 500-599 |
| OFAC Reporting | Pass | 31 CFR 501.603 blocking reports |
| OFAC Framework | Pass | Compliance commitments |
| Overall | **Pass** | Ready for editorial review |

## Screening Program Compliance

| Requirement | Section | Status | Notes |
|-------------|---------|--------|-------|
| SDN List screening | 4.1 Step 1 | Complete | Primary list |
| Consolidated Sanctions List | 4.1 Step 1 | Complete | Comprehensive coverage |
| SSI List | 4.1 Step 1 | Complete | Sectoral sanctions |
| List update timing | 4.1 Step 3 | Complete | 24-hour requirement |
| Match threshold configuration | 4.1 Step 2 | Complete | Sensitivity settings |

## Screening Points Compliance

| Screening Point | Section | Status | Notes |
|-----------------|---------|--------|-------|
| Customer onboarding | 4.2 | Complete | Pre-account opening |
| Transaction screening | 4.3 | Complete | Wire transfers, high-risk |
| Periodic rescreening | 4.6 | Complete | List updates trigger |
| Counterparty screening | 4.3 Step 1 | Complete | Beneficiary, intermediary |

## Match Handling Process

| Step | Section | Status | Notes |
|------|---------|--------|-------|
| Initial review | 4.4 Steps 1-2 | Complete | Name, DOB, address comparison |
| False positive documentation | 4.4 Step 4-5 | Complete | Rationale required |
| True match escalation | 4.4 Step 6 | Complete | To BSA/AML Officer |
| Inconclusive handling | 4.4 Step 6 | Complete | Escalation path |

## Blocking and Reporting Compliance

| Requirement | Section | Status | Notes |
|-------------|---------|--------|-------|
| Immediate blocking | 4.5 Steps 2-3 | Complete | Account, funds |
| No customer notification | 4.5 Step 3 | Complete | No tipping |
| Interest-bearing account | 4.5 Step 4 | Complete | Blocked funds |
| 10-day blocking report | 4.5 Step 5 | Complete | 31 CFR 501.603 |
| Annual report | 4.5 Step 7 | Complete | September 30 deadline |

## Critical Issues

None identified.

## Major Issues

None identified.

## Minor Issues

| # | Section | Framework | Issue | Recommendation |
|---|---------|-----------|-------|----------------|
| m-1 | 4.6 | OFAC | Rescreening frequency placeholder should specify minimum (daily recommended upon list changes) | Clarify that list-update-triggered screening should be automated within 24 hours |
| m-2 | 4.1 | OFAC | 50% Rule screening implications should be addressed | Add note that entities 50%+ owned by SDNs are blocked even if not listed |

## Transaction Screening SLAs

| Transaction Type | Section | Response Time | Status |
|------------------|---------|---------------|--------|
| Wire transfers | 4.3 Step 4 | Placeholder hours | Adequate |
| Customer onboarding | 4.2 Step 3 | Placeholder hours | Adequate |

## Approval Status

- [x] **Approved** - Ready for editorial review
- [ ] **Approved with minor changes** - Can proceed, address minors in parallel
- [ ] **Requires revision** - Must address critical/major issues before proceeding

