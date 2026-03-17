---
name: variance-analysis
description: Generate draft monthly variance analysis commentary
---

# Approved Use Case
Use Case ID: UC-002

# Allowed Inputs
- Monthly P&L export
- Budget vs. actual summary
- Prior month comparison
- Prior year comparison
- Masked departmental expense reports

# Prohibited Inputs
- Social Security Numbers (SSNs)
- Bank account numbers
- Credentials or access tokens
- Unmasked payroll detail
- Tax identification numbers (EIN, ITIN)

# Required Working Method
1. Confirm UC-002 is approved in the use-case register
2. Confirm all input files are sample data, masked, or explicitly approved for AI processing
3. Identify comparison basis (budget vs. actual, month-over-month, year-over-year)
4. Calculate variances for each line item (absolute dollar and percentage)
5. Apply materiality thresholds -- default: >= $10,000 absolute AND >= 10% percentage change
6. Separate facts (what changed) from assumptions (why it may have changed)
7. Flag items that exceed materiality thresholds for reviewer attention
8. Produce output in the format specified below

# Output Format

## Revenue
- Total revenue variance (actual vs. budget, actual vs. prior month)
- Material line-item variances with dollar and percentage amounts
- Favorable/unfavorable designation for each item

## Gross Margin
- Gross margin dollar and percentage variance
- Cost of sales drivers if material

## Operating Expenses
- Material variances by expense category
- One-time vs. recurring classification where identifiable
- Department-level detail if available

## EBITDA
- EBITDA variance summary
- Key drivers (revenue, COGS, operating expenses)

## Items Requiring Review
- Any variance exceeding materiality thresholds
- Items where the cause is unclear or requires management input
- Unusual or non-recurring items

## Assumptions
- Clearly state any assumptions made during the analysis
- Distinguish between data-supported conclusions and inferences

## Reviewer Checklist
- [ ] Verified input files are masked or approved for AI use
- [ ] Confirmed variance calculations against source data
- [ ] Reviewed materiality threshold application
- [ ] Checked favorable/unfavorable designations
- [ ] Validated one-time vs. recurring classifications
- [ ] Confirmed assumptions are reasonable and clearly labeled
- [ ] Approved draft commentary for distribution

# Style Rules
- Use clear, professional controller language
- No dramatic wording (avoid "skyrocketed", "plummeted", "massive", etc.)
- State whether each variance is favorable or unfavorable
- Distinguish one-time items from recurring trends where possible
- Present numbers with consistent formatting (dollar signs, commas, two decimal places)
- Keep commentary factual -- flag uncertainties rather than speculating

# Evidence
Save outputs to: evidence/run-logs/
Suggested naming: YYYY-MM-DD_UC-002_variance-analysis.md

# Human Review
Required reviewer: Controller, Accounting Manager, or FP&A Lead
