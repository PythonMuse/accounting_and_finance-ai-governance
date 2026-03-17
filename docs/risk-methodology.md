# AI Risk Assessment Methodology

## Overview

This document describes how Finance assesses risk for AI-enabled workflows. The approach is built on the COSO Internal Control framework (2026 alignment), applied specifically to AI use cases. The goal is not to create new bureaucracy -- it is to use the same risk language controllers already know and apply it to a new category of tools.

Every AI use case in the [GenAI Use Case Register](../inventory/genai-use-case-register.md) must complete a risk assessment before moving to Approved status.

## COSO Framework Applied to AI

The five COSO components provide the structure for our AI risk assessment. For each component, we ask targeted questions that surface the risks specific to AI-assisted finance workflows.

### 1. Control Environment

The foundation. Does the organization have the right tone, structure, and accountability for AI use?

**Questions for the Controller:**

- Is there a clear owner for this AI workflow, and do they understand they are accountable for its outputs?
- Does the team using this workflow have adequate training on both the AI tool and the associated data handling requirements?

### 2. Risk Assessment

Identify what could go wrong with this specific AI use case and how likely it is.

**Questions for the Controller:**

- What is the worst-case outcome if this AI workflow produces an incorrect result that goes undetected?
- What data does this workflow consume, and what is the exposure if that data is mishandled?

### 3. Control Activities

The specific controls designed to mitigate identified risks.

**Questions for the Controller:**

- Is there a human review step before any AI output is used in a financial process?
- Are the controls mapped to this workflow documented in the [AI Control Matrix](control-matrix.md), and is evidence being retained?

### 4. Information and Communication

How information about AI risks and controls flows through the organization.

**Questions for the Controller:**

- Does the team know where to find the approved use cases, data classification rules, and escalation procedures?
- Are AI-related incidents or near-misses being reported and communicated to the right people?

### 5. Monitoring

Ongoing evaluation of whether controls are working as designed.

**Questions for the Controller:**

- Are AI workflow outputs being sampled and reviewed on a regular basis?
- Are exception rates and error rates being tracked, and is there a threshold that triggers escalation?

## Risk Levels

Each use case is assigned a risk level based on the assessment:

| Risk Level | Criteria |
|------------|----------|
| **Low** | No financial data involved. Output is informational only. Errors are easily detected and have no reporting impact. |
| **Medium** | Involves internal financial data (masked or aggregated). Output supports but does not determine financial reporting. Human review is in place. |
| **High** | Involves sensitive or transaction-level financial data. Output directly supports financial reporting, audit, or external disclosures. |

## Assessment Template

Use the standard template for all risk assessments:

**[AI Risk Assessment Template](../assessments/templates/risk-template.md)**

The completed assessment should be stored in the `assessments/` directory and linked from the use case register.

---

*Document Owner: Controller*
*Last Updated: March 2026*
