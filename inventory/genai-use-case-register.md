# GenAI Use Case Register

## Overview

This register is the official inventory of all generative AI use cases in Finance. Every AI workflow must appear here before it is used in production. See [Approved AI Use Cases](../docs/approved-use-cases.md) for the full policy on registration and approval.

## Use Case Inventory

| Use Case ID | Process | Description | Owner | Data Classification | AI Capability | Risk Level | Approval Status |
|-------------|---------|-------------|-------|--------------------|---------------|------------|-----------------|
| UC-001 | Bank Reconciliation | AI-assisted review of recon variance explanations | Controller | Masked Internal | Analysis | Medium | Approved |
| UC-002 | Flux Analysis | AI-assisted generation of variance explanations | Controller | Internal Financial | Analysis | Medium | Pilot |
| UC-003 | Invoice Extraction | AI extraction of vendor invoice fields | AP Manager | Vendor Data | Data Processing | High | Proposed |

## Column Definitions

- **Use Case ID**: Unique identifier. Sequential, prefixed with UC-.
- **Process**: The accounting or finance process this use case supports.
- **Description**: Brief description of what the AI does in this workflow.
- **Owner**: The Finance Process Owner responsible for the workflow.
- **Data Classification**: The highest data classification level involved (see [Data Classification](../docs/data-classification.md)).
- **AI Capability**: The type of AI capability used (Analysis, Data Processing, Generation, etc.).
- **Risk Level**: Assessed risk level per the [Risk Assessment Methodology](../docs/risk-methodology.md).
- **Approval Status**: Current status -- Proposed, Pilot, Approved, or Retired.

## Approval Status Definitions

| Status | Meaning |
|--------|---------|
| **Proposed** | Use case has been submitted but has not completed the risk assessment and control design process. Not approved for any use. |
| **Pilot** | Use case has been assessed and is approved for testing and internal analysis only. Outputs must not be used in production financial processes. |
| **Approved** | Use case has completed the full governance process and is approved for production use, subject to all applicable controls. |
| **Retired** | Use case was previously approved but is no longer in use. Retained for historical reference. |

## Adding a New Use Case

1. Assign the next sequential Use Case ID
2. Complete all columns in the table above
3. Submit a pull request with the updated register
4. Complete the [risk assessment](../assessments/templates/risk-template.md)
5. Map controls from the [control matrix](../docs/control-matrix.md)
6. Obtain Controller approval before changing status to Approved

---

*Register Owner: Controller*
*Last Updated: March 2026*
