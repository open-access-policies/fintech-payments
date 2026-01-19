# ANNEX-003: Placeholder Quick Reference

## Purpose

This annex provides a quick reference guide for completing placeholders in **[Company Name]** policy and procedure documents. All placeholders use the format `**[Description, e.g., example]**`.

---

## Standard Placeholders

### Company Information

| **Placeholder** | **Description** | **Example** |
|-----------------|-----------------|-------------|
| `**[Company Name]**` | Legal entity name | Acme Payments, Inc. |
| `**[Company Name, trading as DBA]**` | Trade name if different | PayEasy |

### Roles and Titles

| **Placeholder** | **Description** | **Example** |
|-----------------|-----------------|-------------|
| `**[Role Title, e.g., Chief Information Security Officer]**` | Person responsible for the policy | Chief Information Security Officer |
| `**[Role Title, e.g., Chief Executive Officer]**` | Approving authority | Chief Executive Officer |
| `**[Role Title, e.g., VP of Engineering]**` | Technical policy owner | VP of Engineering |
| `**[Role Title, e.g., BSA/AML Officer]**` | Compliance officer | Chief Compliance Officer |
| `**[Role Title, e.g., Privacy Officer]**` | Privacy function owner | General Counsel |

### Dates

| **Placeholder** | **Description** | **Example** |
|-----------------|-----------------|-------------|
| `**[Date, e.g., 2026-01-15]**` | Effective, review, or approval date | 2026-03-01 |
| `**[Date]**` | Simple date placeholder | January 15, 2026 |

### Timeframes and Durations

| **Placeholder** | **Description** | **Example** |
|-----------------|-----------------|-------------|
| `**[Duration, e.g., 2 weeks]**` | Time period | 10 business days |
| `**[Number, e.g., 30]**` | Numeric value | 45 |
| `**[Frequency, e.g., quarterly]**` | Review/action frequency | annually |
| `**[Number, e.g., 7]**` years | Retention period | 7 |

### Financial and Threshold Values

| **Placeholder** | **Description** | **Example** |
|-----------------|-----------------|-------------|
| `**[$Amount, e.g., $50,000]**` | Dollar threshold | $100,000 |
| `**[1/2/3/4, based on transaction volume]**` | PCI DSS merchant level | 2 |

### System and Technical References

| **Placeholder** | **Description** | **Example** |
|-----------------|-----------------|-------------|
| `**[System Name]**` | Internal system name | Jira, ServiceNow |
| `**[Tool Name]**` | Security tool | CrowdStrike, Splunk |

---

## Common Completion Guidance

### Policy Owner
Select the most senior person accountable for the policy domain:
- Security policies: CISO
- Engineering policies: VP of Engineering or CTO
- Operational policies: COO or IT Director
- Compliance policies: CCO or General Counsel
- Privacy policies: Privacy Officer or General Counsel

### Review Dates
- **Last Reviewed:** Set to actual review date
- **Next Review:** Typically 12 months from last review

### Timeframes
Consider organizational capabilities when setting timeframes:
- Incident response timelines should be achievable
- Remediation timelines should align with risk tolerance
- Review frequencies should be sustainable

### Thresholds
Set financial thresholds based on:
- Materiality for your organization
- Regulatory requirements (e.g., BSA $10,000 CTR threshold is fixed)
- Risk tolerance

---

## Placeholder by Document Type

### Policies (Standard Set)

All policies include:
- `**[Company Name]**` - Multiple occurrences
- `**[Role Title...]**` - Policy Owner, Approved By
- `**[Date...]**` - Effective Date, Last Reviewed, Next Review

### Procedures (Standard Set)

All procedures include:
- `**[Role Title...]**` - Procedure Owner
- `**[Date...]**` - Last Reviewed, Next Review
- `**[Number...]**` or `**[Duration...]**` - Various timeframes

---

## Bulk Replacement Approach

When customizing for your organization:

1. **Search and replace** `**[Company Name]**` with your legal entity name
2. **Review role titles** and map to your organizational structure
3. **Set all dates** to appropriate values
4. **Evaluate timeframes** against your operational capabilities
5. **Adjust thresholds** based on your risk profile and business scale

---

**Document ID:** ANNEX-003
**Version:** 1.0
**Last Updated:** **[Date, e.g., 2026-01-15]**
