# Sample Bank Reconciliation: UC-001

This example demonstrates the bank-rec-review skill (UC-001) using sample data. All figures are fictitious and intended for testing only.

---

## Scenario

The Controller is reviewing the March 2026 bank reconciliation for the primary operating account. Two data files are used as inputs:

- `demo-data/bank_statement_masked.csv` -- bank statement export with masked account numbers
- `demo-data/gl_cash_activity.csv` -- general ledger cash account activity

The bank statement shows an ending balance of $148,250.00. The GL shows an ending balance of $145,000.00. The difference of $3,250.00 is explained by three reconciling items: one deposit in transit and two outstanding checks.

---

## Reconciliation Summary

| Line Item                 | Amount        |
|---------------------------|---------------|
| Bank ending balance       | $148,250.00   |
| Add: Deposit in transit   | $12,500.00    |
| Less: Outstanding checks  | ($15,750.00)  |
| **Adjusted bank balance** | **$145,000.00** |
| GL ending balance         | $145,000.00   |
| **Difference**            | **$0.00**     |

---

## Reconciling Items

### Deposits in Transit

| Reference   | Date       | Amount     | Description              |
|-------------|------------|------------|--------------------------|
| DEP-0331-A  | 2026-03-31 | $12,500.00 | Customer receipt batch   |

This deposit was recorded in the GL on March 31 but had not cleared the bank by the statement date.

### Outstanding Checks

| Reference | Date       | Amount     | Description     |
|-----------|------------|------------|-----------------|
| CHK-2105  | 2026-03-29 | $8,200.00  | Vendor payment  |
| CHK-2108  | 2026-03-31 | $7,550.00  | Vendor payment  |

Both checks were recorded in the GL but had not cleared the bank by the statement date. Combined outstanding checks total $15,750.00.

---

## AI Draft Commentary

> The March 2026 bank reconciliation for the primary operating account reconciles to zero. The bank statement ending balance of $148,250.00 is adjusted by one deposit in transit ($12,500.00, reference DEP-0331-A) and two outstanding checks ($8,200.00, reference CHK-2105 and $7,550.00, reference CHK-2108) to arrive at an adjusted bank balance of $145,000.00, which agrees to the GL ending balance.
>
> All reconciling items relate to timing differences at month-end. No unusual items or unexplained variances were identified. The deposit in transit represents a customer receipt batch recorded on March 31. Both outstanding checks are vendor payments issued in the last three business days of the month.

---

## Reviewer Checklist

- [ ] Confirmed input files are masked or sample data
- [ ] Verified bank ending balance matches the bank statement
- [ ] Verified GL ending balance matches the trial balance
- [ ] Confirmed each reconciling item is supported by documentation
- [ ] Checked that deposit in transit cleared in the subsequent period
- [ ] Checked that outstanding checks cleared in the subsequent period
- [ ] Verified the adjusted bank balance agrees to the GL balance
- [ ] Reviewed AI-generated commentary for accuracy
- [ ] Approved the reconciliation for filing

**Reviewer:** ____________________
**Date:** ____________________

---

## Controller Notes

This sample reconciliation covers the basic case of deposits in transit and outstanding checks. In production use, consider expanding the analysis to include:

- **Stale checks**: Outstanding checks older than 90 days that may need to be voided
- **Missing deposits**: Deposits recorded on the bank statement but not in the GL
- **Bank errors**: Items that need to be reported to the bank for correction
- **GL adjustments**: Journal entries needed to correct the GL (e.g., bank fees not yet recorded)
- **Multi-account reconciliations**: Extending the workflow to cover payroll, savings, and investment accounts
