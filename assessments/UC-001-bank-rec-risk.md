# Risk Assessment: UC-001 Bank Reconciliation Review

## Use Case Summary

| Field                | Value                                                  |
|----------------------|--------------------------------------------------------|
| **Use Case ID**      | UC-001                                                 |
| **Process**          | Bank Reconciliation                                    |
| **Owner**            | Controller                                             |
| **Business Objective** | Improve efficiency of monthly bank reconciliation review |
| **Data Sources**     | GL cash activity, bank statement exports               |
| **Data Sensitivity** | Internal (masked before AI processing)                 |
| **Risk Rating**      | Medium                                                 |
| **Assessment Date**  | March 2026                                             |

---

## COSO-Aligned Risk Assessment

### 1. Control Environment

**Does the organization support responsible AI use with tone from the top?**

Yes. The Controller has approved a pilot program for AI-assisted reconciliation review. An AI governance policy is in place that defines acceptable use, data handling requirements, and reviewer responsibilities. Staff involved in the reconciliation process have been briefed on what AI can and cannot do in this workflow.

### 2. Risk Assessment

**What risks does this use case introduce, and how significant are they?**

- **Data exposure risk**: Bank account numbers and payee details could be sent to an AI model if masking is skipped. Mitigated by mandatory masking before any AI processing.
- **Over-reliance risk**: Staff may accept AI-generated commentary without verifying amounts against source documents. Mitigated by requiring human review and sign-off on every reconciliation.
- **Accuracy risk**: The AI may misclassify reconciling items or produce incorrect variance explanations. Mitigated by treating all AI output as draft and requiring controller approval.

Residual risk after controls: **Medium**. The use case handles internal financial data, not regulated PII, and all outputs are reviewed before use.

### 3. Control Activities

**What controls are in place to manage the identified risks?**

| Control                     | Type        | Description                                               |
|-----------------------------|-------------|-----------------------------------------------------------|
| Data masking                | Preventive  | Bank account numbers masked before AI processing          |
| Human review required       | Detective   | Controller or Accounting Manager reviews all AI output    |
| Evidence retention          | Monitoring  | Run logs saved to `evidence/run-logs/` with date stamps   |
| Skill boundary enforcement  | Preventive  | SKILL.md restricts allowed and prohibited inputs          |
| Sample data testing         | Detective   | New skills tested on demo data before production use      |

### 4. Information & Communication

**How is relevant information captured and shared?**

- AI run logs are saved automatically to `evidence/run-logs/` with standardized naming.
- The use case register documents approval status, data classification, and ownership.
- The SKILL.md file for bank-rec-review defines the exact workflow, allowed inputs, and prohibited inputs so that any team member can understand the boundaries.
- Reviewer checklists are included in every output to ensure consistent review steps.

### 5. Monitoring

**How will the organization monitor this use case over time?**

- Monthly review of run logs to confirm masking was applied and outputs were reviewed.
- Quarterly comparison of AI-assisted reconciliation quality against manual reconciliations.
- Any exceptions or errors flagged during review are documented in `evidence/review-notes/`.
- The Controller will reassess the risk rating after 90 days of use.

---

## Approved Controls Summary

| Requirement             | Status   |
|-------------------------|----------|
| Data masking required   | Yes      |
| Human review required   | Yes      |
| Evidence retained       | Yes      |
| Skill boundary defined  | Yes      |
| Testing on sample data  | Complete |

---

## Approval

| Role        | Name | Date | Signature |
|-------------|------|------|-----------|
| Controller  |      |      |           |
| IT / Security |    |      |           |
