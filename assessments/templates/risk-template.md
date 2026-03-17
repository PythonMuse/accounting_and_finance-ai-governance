# Risk Assessment Template

Use this template to document a risk assessment for any AI use case. Complete each section before submitting for approval.

---

## Use Case Summary

| Field                | Value                                                         |
|----------------------|---------------------------------------------------------------|
| **Use Case ID**      | UC-___                                                        |
| **Process**          |                                                               |
| **Owner**            |                                                               |
| **Business Objective** | What process improvement is expected?                       |
| **Data Sources**     | List systems used (GL, bank statements, AP exports, etc.)     |
| **Data Sensitivity** | Public / Internal / Confidential / Regulated                  |
| **Risk Rating**      | Low / Medium / High                                           |
| **Assessment Date**  |                                                               |

---

## COSO-Aligned Risk Assessment

### 1. Control Environment

**Does the organization support responsible AI use with tone from the top?**

- Is there an approved AI governance policy?
- Has leadership communicated expectations for AI use in this process?
- Are staff trained on what AI can and cannot do in this workflow?

> _Your answer here._

### 2. Risk Assessment

**What risks does this use case introduce, and how significant are they?**

Consider the following categories:
- **Data exposure**: Could sensitive data be sent to the AI model? What is the worst-case scenario?
- **Over-reliance**: Could staff skip verification steps because the AI produced an answer?
- **Accuracy**: What happens if the AI output is wrong? What is the downstream impact?
- **Regulatory**: Are there compliance requirements that affect how this data can be processed?

> _List each risk, its likelihood, impact, and planned mitigation._

Residual risk after controls: **Low / Medium / High**

### 3. Control Activities

**What controls are in place to manage the identified risks?**

| Control | Type (Preventive / Detective / Monitoring) | Description |
|---------|---------------------------------------------|-------------|
|         |                                             |             |
|         |                                             |             |
|         |                                             |             |

### 4. Information & Communication

**How is relevant information captured and shared?**

- How are AI run logs stored?
- How is the use case documented so others can understand the boundaries?
- How are review results communicated to stakeholders?

> _Your answer here._

### 5. Monitoring

**How will the organization monitor this use case over time?**

- How often will run logs be reviewed?
- What metrics will be tracked (accuracy, time saved, exceptions)?
- When will the risk rating be reassessed?

> _Your answer here._

---

## Approved Controls Summary

| Requirement             | Status (Yes / No / N/A) |
|-------------------------|-------------------------|
| Data masking required   |                         |
| Human review required   |                         |
| Evidence retained       |                         |
| Skill boundary defined  |                         |
| Testing on sample data  |                         |

---

## Approval

| Role          | Name | Date | Signature |
|---------------|------|------|-----------|
| Process Owner |      |      |           |
| Controller    |      |      |           |
| IT / Security |      |      |           |
