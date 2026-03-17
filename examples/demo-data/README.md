# Demo Data

This folder contains sample datasets for testing AI governance skills. All data is fictitious. No real account numbers, customer names, or financial figures are included.

These files are intended for:
- Testing skills before running them on production data
- Demonstrating the governance workflow to stakeholders
- Training team members on how skills and evidence retention work

---

## Files

| File                         | Description                                      | Used By  |
|------------------------------|--------------------------------------------------|----------|
| `bank_statement_masked.csv`  | Masked bank statement with sample transactions   | UC-001   |
| `gl_cash_activity.csv`       | General ledger cash account activity             | UC-001   |
| `variance_demo_pnl.csv`     | Monthly P&L with actual, budget, and prior month | UC-002   |

---

## Usage

1. Do not modify these files -- they serve as a stable baseline for testing.
2. When testing a skill, reference these files as inputs.
3. Save all test outputs to `evidence/testing/` rather than `evidence/run-logs/` (run-logs is reserved for production evidence).
