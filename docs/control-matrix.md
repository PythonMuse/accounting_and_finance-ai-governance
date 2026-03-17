# AI Control Matrix

## Overview

This matrix defines the core controls applied to AI workflows in Finance. Every approved AI use case must map to at least one control from this matrix. Controls are categorized by type: preventive controls stop problems before they happen, detective controls catch problems after they occur, and monitoring controls track patterns over time.

## Control Matrix

| Control ID | Control Type | Description | Related Use Cases |
|------------|-------------|-------------|-------------------|
| AI-01 | Preventive | Only approved use cases may be used in production Finance workflows. Unapproved workflows must not produce outputs used in financial reporting or record-keeping. | All |
| AI-02 | Preventive | Sensitive data must be masked or anonymized before AI processing. Data classification must be determined before any data is shared with an AI tool. | All |
| AI-03 | Detective | AI outputs require human review before use in any financial process. The reviewer must have sufficient knowledge to evaluate the output for accuracy and completeness. | All |
| AI-04 | Detective | Evidence files must be retained for every AI workflow run. Evidence includes inputs provided, outputs received, reviewer identity, and review disposition. | All |
| AI-05 | Monitoring | AI exception rates (errors, rejections, overrides) are tracked and reviewed on a regular cadence. Trends that exceed defined thresholds trigger escalation to the Controller. | All |

## How to Use This Matrix

1. **When registering a new use case:** Identify which controls apply and document them in the use case registration.
2. **When designing a workflow:** Build the control steps directly into the workflow. Do not treat controls as an afterthought.
3. **When running a workflow:** Follow the controls as documented. Retain the evidence specified.
4. **When reviewing a workflow:** Verify that controls were executed and evidence exists.

## Adding New Controls

If a use case requires a control not covered by this matrix, propose it via pull request. New controls should follow the same format:

- Assign the next sequential Control ID (e.g., AI-06)
- Classify as Preventive, Detective, or Monitoring
- Write a clear, actionable description
- Identify the use cases it applies to

The Controller must approve any additions to this matrix.

---

*Document Owner: Controller*
*Last Updated: March 2026*
