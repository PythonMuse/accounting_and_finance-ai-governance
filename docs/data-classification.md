# Data Classification for AI Workflows

## Purpose

This document defines what data can and cannot be used with AI tools. Every Finance team member using AI in their work needs to know these categories. When in doubt, assume the most restrictive classification.

Data classification is the single most important control in AI workflows. Getting this wrong creates real risk. Getting it right makes AI adoption straightforward.

## Classification Categories

### Category 1 -- Safe for AI

This data can be shared with AI tools without modification.

| Data Type | Examples |
|-----------|----------|
| File structures | Folder layouts, directory trees, file naming conventions |
| Column names and field labels | "vendor_name", "invoice_date", "gl_account" |
| Workflow descriptions | Process narratives, procedure documentation |
| Documentation drafts | Policy drafts, memo templates, training materials |
| Code snippets | Python scripts, SQL queries, automation logic |
| Public reference data | GAAP standards, regulatory guidance, published benchmarks |

**Rule of thumb:** If you would put it on a whiteboard during a team meeting, it is probably Category 1.

### Category 2 -- Mask Before Sharing

This data may be used with AI tools only after masking or anonymizing identifying details.

| Data Type | Examples |
|-----------|----------|
| Vendor names | Replace with "Vendor A", "Vendor B", etc. |
| Invoice numbers | Replace with sequential placeholders |
| Transaction amounts | Use representative sample amounts or ranges |
| Internal project identifiers | Replace with generic codes |
| Customer names | Replace with "Customer 001", etc. |
| Internal account numbers | Replace with descriptive labels |

**Masking means:** Replace actual values with synthetic or generic equivalents that preserve the structure and logic of the data without revealing real identities or amounts.

See [Article 06: How to Use AI in Accounting Without Sending the Wrong Data](../../articles/06-safe-ai-data-workflows/) for practical masking techniques and scripts.

### Category 3 -- Do Not Share

This data must never be shared with AI tools under any circumstances.

| Data Type | Examples |
|-----------|----------|
| Social Security Numbers | SSNs, TINs, EINs tied to individuals |
| Bank account details | Account numbers, routing numbers, wire instructions |
| Payroll records | Salary data, compensation details, tax withholdings |
| Personal addresses | Employee or customer home addresses |
| Confidential contracts | Executed agreements with non-disclosure terms |
| Authentication credentials | Passwords, API keys, access tokens |
| Protected health information | Any data covered by HIPAA or equivalent |

**There are no exceptions to Category 3.** If data falls in this category, it does not go into an AI tool. Period.

## Default Rule

**If you are unsure how to classify a piece of data, treat it as Category 3.**

It is always better to over-restrict than to accidentally expose sensitive information. If you believe data should be reclassified, raise it with the Controller for a determination before proceeding.

## Responsibilities

- **Finance Process Owners** are responsible for classifying data in their workflows before AI use.
- **The Controller** resolves classification disputes and can reclassify data when warranted.
- **All Finance team members** are expected to apply these categories every time they use an AI tool.

---

*Document Owner: Controller*
*Last Updated: March 2026*
