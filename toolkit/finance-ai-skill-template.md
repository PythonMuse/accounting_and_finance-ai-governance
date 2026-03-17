# Finance AI Skill Template

Use this template to define a new AI skill. Each skill maps to one approved use case and specifies exactly what the AI can do, what data it can access, and what output it produces. Save completed skills in `skills/[skill-name]/SKILL.md`.

---

```
---
name: [skill-name]
description: [brief description]
---

# Approved Use Case
Use Case ID: [UC-XXX]

# Allowed Inputs
- [list allowed data sources]

# Prohibited Inputs
- [list restricted data]

# Required Working Method
1. [steps]

# Output Format
[describe expected output]

# Evidence
Save outputs to: evidence/run-logs/
Suggested naming: YYYY-MM-DD_UC-XXX_[skill-name].md

# Human Review
Required reviewer: [role]
```

---

## Instructions

1. **Name**: Use lowercase with hyphens. This becomes the folder name under `skills/`.
2. **Description**: One sentence explaining what the skill does. Write it for someone who has not seen the use case.
3. **Approved Use Case**: Must reference an approved entry in the use-case register. Do not create skills for unapproved use cases.
4. **Allowed Inputs**: Be specific. List file types, system names, and any masking requirements.
5. **Prohibited Inputs**: List data that must never be provided to the AI, even accidentally. Common examples: SSNs, bank account numbers, credentials, unmasked payroll.
6. **Required Working Method**: Number each step. Start with confirming the use case is approved and data is classified correctly.
7. **Output Format**: Describe the sections and structure of the expected output. Be specific enough that a reviewer knows what to look for.
8. **Evidence**: Always save to `evidence/run-logs/`. Use the naming convention `YYYY-MM-DD_UC-XXX_skill-name.md`.
9. **Human Review**: Name the role (not the person) required to review and approve the output.
