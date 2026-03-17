---
name: bank-rec-review
description: Analyze bank reconciliation support and produce variance summary
---

# Approved Use Case
UC-001

# Allowed Inputs
- Masked bank statements
- GL cash activity export
- Prior reconciliation file

# Prohibited Inputs
- Unmasked bank account numbers
- Payroll detail
- Credentials or access tokens

# Workflow
1. Confirm use case approval -- verify UC-001 is approved in the use-case register
2. Confirm data classification -- verify all input files are masked or sample data
3. Compare bank and GL activity -- match transactions by reference, date, and amount
4. Identify reconciling items -- flag transactions present in one source but not the other
5. Generate variance explanation summary -- produce draft commentary for each reconciling item

# Output
- Reconciling items summary
- Exception list
- Suggested explanation text
- Reviewer checklist

# Evidence
Save outputs to: evidence/run-logs/
Suggested naming: YYYY-MM-DD_UC-001_bank_rec_review.md

# Human Review
Required reviewer: Controller or Accounting Manager
