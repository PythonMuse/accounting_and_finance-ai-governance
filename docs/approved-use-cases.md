# Approved AI Use Cases

## Overview

All AI workflows used in Finance must be registered in the use case inventory before use. This is not optional. If a workflow is not in the register, it is not approved for production accounting work.

## What "Approved" Means

An approved use case has completed the full governance process:

1. **Registered** in the use case inventory with a unique ID
2. **Risk assessed** using the standard methodology
3. **Controls designed** and mapped to the control matrix
4. **Signed off** by the Controller

Only workflows with an approval status of **Approved** in the register may be used in production accounting processes.

## What About Experimental Use?

Workflows with a status of **Pilot** or **Proposed** are considered experimental. They may be explored and tested, but their outputs must not be used in:

- Financial statements or SEC filings
- Journal entries or ledger adjustments
- External reporting of any kind
- Audit support documentation

Pilot workflows can be used for internal analysis, learning, and proof-of-concept work, provided they follow the data classification rules.

## The Use Case Register

The official inventory of all AI use cases is maintained here:

**[GenAI Use Case Register](../inventory/genai-use-case-register.md)**

This register includes:

- Use case ID and description
- Process owner
- Data classification
- AI capability type
- Risk level
- Current approval status

## Adding a New Use Case

To register a new AI workflow:

1. Open a pull request adding the use case to the register
2. Complete the [risk assessment](../assessments/templates/risk-template.md)
3. Map controls from the [control matrix](control-matrix.md)
4. Request Controller review and approval

Do not begin using a workflow in production until the Controller has approved it and the register has been updated.

## Questions

If you are unsure whether your AI usage requires registration, the answer is yes. Register it. The overhead is minimal and the protection is significant.

---

*Document Owner: Controller*
*Last Updated: March 2026*
