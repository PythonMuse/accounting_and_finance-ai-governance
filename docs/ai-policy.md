# Finance AI Policy

## Purpose

This policy enables responsible AI adoption within Finance while maintaining strong internal controls. The goal is straightforward: let the team use AI tools where they add value, but keep the same rigor around financial data and reporting that we already expect from every other process.

This policy applies to all Finance team members and any third parties operating within Finance workflows.

## Scope

This policy covers:

- **Claude and other LLMs** used for analysis, drafting, or summarization
- **AI copilots** embedded in development tools (e.g., GitHub Copilot, Cursor)
- **Automated AI agents** that execute multi-step workflows
- **AI-generated financial analysis** including variance explanations, reconciliation support, and report drafting

If a tool uses a language model or generative AI in any part of its workflow, this policy applies.

## Key Principles

### AI May Assist With

- :white_check_mark: Summarizing financial data and reports
- :white_check_mark: Identifying anomalies or outliers in transaction data
- :white_check_mark: Generating draft documentation (memos, variance explanations, process narratives)
- :white_check_mark: Analyzing patterns across large datasets
- :white_check_mark: Writing and reviewing code for accounting automation
- :white_check_mark: Drafting reconciliation variance explanations

### AI May NOT

- :x: Post journal entries or adjustments to the general ledger
- :x: Modify financial records in any system of record
- :x: Execute payments, wire transfers, or disbursements
- :x: Access sensitive data (PII, bank details, payroll) without proper masking
- :x: Make final decisions on accounting treatment or disclosure
- :x: Bypass any existing approval workflow

**The line is clear: AI assists, humans decide and act.**

## Governance Structure

| Role | Responsibility |
|------|---------------|
| **Controller** | Policy owner. Approves all AI use cases for Finance. Final authority on whether a workflow meets control standards. |
| **IT / Information Security** | Technical security. Reviews AI tools for data handling, access controls, and infrastructure risk. |
| **Legal / Compliance** | Regulatory oversight. Evaluates AI use cases against applicable regulations, contracts, and data privacy requirements. |
| **Finance Process Owner** | Workflow owner. Designs and operates AI-assisted workflows within their area. Responsible for day-to-day compliance with this policy. |

The Controller owns this policy and is responsible for its maintenance, interpretation, and enforcement.

## Approval Process

Every AI workflow in Finance must go through four steps before production use:

### 1. Use Case Registration

Submit the workflow to the [GenAI Use Case Register](../inventory/genai-use-case-register.md). Include a clear description of what the AI does, what data it touches, and who owns it.

### 2. Risk Assessment

Complete a risk assessment using the [AI Risk Assessment Template](../assessments/templates/risk-template.md). Identify what could go wrong and how likely it is.

### 3. Control Design

Design controls that address the risks identified. Map each risk to at least one control from the [AI Control Matrix](control-matrix.md). Document the evidence that will be retained for each workflow run.

### 4. Controller Approval

The Controller reviews the use case, risk assessment, and control design. Approval is documented in the use case register. No workflow moves to production without this signoff.

---

*Policy Owner: Controller*
*Last Updated: March 2026*
*Review Frequency: Quarterly, or upon material change*
