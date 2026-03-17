# Finance AI Operating Rules

## Purpose
This repository supports approved finance AI workflows under company policy.

## Non-negotiable boundaries
- Do not use live production data unless the use case register explicitly allows it.
- Never post journal entries, vendor changes, or payment actions directly.
- Never send secrets, passwords, API keys, payroll SSNs, bank account numbers, or tax IDs to external tools.
- If source data is unclassified, stop and ask for classification.
- If a workflow is not in the approved-use-case register, treat it as unapproved.

## Required working method
- Start by checking the approved-use-case register.
- Use the relevant risk assessment and control matrix before proposing automation.
- Save output to the evidence folder with date/time and use-case ID.
- Include assumptions, source files used, and reviewer checklist.

## Output requirements
- Separate facts from assumptions.
- Cite the files used.
- Flag missing support.
- Mark every draft as "Not posted / human review required" unless explicitly approved.

## Data restrictions
Never process:
- Bank account numbers
- SSNs or tax IDs
- Payroll personal data
- Passwords or credentials

If detected, stop the workflow and request masked data.

## Evidence
Each workflow execution should produce:
- Exception summary
- Supporting analysis
- Reviewer checklist
- Timestamped output file
