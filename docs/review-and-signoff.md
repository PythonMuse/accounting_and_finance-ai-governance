# Review and Signoff Requirements

## Overview

Every AI-generated output used in a Finance process must be reviewed by a qualified person before it is relied upon. This is non-negotiable. AI tools are assistants, not decision-makers. The reviewer is the control.

This document defines who reviews AI outputs, what constitutes adequate review, and how signoff is documented.

## Who Reviews

The reviewer must meet all of the following criteria:

- **Subject matter knowledge:** Understands the accounting process the AI output supports well enough to spot errors.
- **Data awareness:** Knows what data went into the AI workflow and can assess whether the output is consistent with that data.
- **Independence:** Did not solely rely on the AI to form their own judgment. The reviewer must be able to evaluate the output on its merits, not just confirm that the AI ran.

In most cases, the reviewer is the **Finance Process Owner** or a designated senior team member. For high-risk use cases, the **Controller** reviews directly or approves the reviewer designation.

## What Constitutes Adequate Review

Adequate review means the reviewer has done all of the following:

1. **Read the full AI output.** Not skimmed. Read.
2. **Compared the output to source data** or known benchmarks to verify accuracy.
3. **Checked for hallucinations or fabricated details** -- numbers, account names, vendor references, or dates that do not match source records.
4. **Evaluated completeness** -- did the AI address the full scope of the request, or did it omit relevant items?
5. **Applied professional judgment** -- does the output make sense given what the reviewer knows about the business, the period, and the accounts involved?

A review that consists only of confirming "the AI ran successfully" is not adequate.

## Signoff Process

### For Standard Use Cases (Low/Medium Risk)

1. Reviewer completes the review checklist (below)
2. Reviewer records their name, date, and disposition in the evidence file
3. Evidence file is saved to the `evidence/` directory for the relevant workflow run

### For High-Risk Use Cases

1. Reviewer completes the review checklist
2. Reviewer documents any concerns or modifications made to the AI output
3. Controller reviews the evidence file and provides final signoff
4. Both the reviewer and Controller signoff are recorded in the evidence file

## Reviewer Checklist

Use this checklist for every AI output review. All items must be addressed.

- [ ] I have read the complete AI output
- [ ] I have compared the output to the source data or relevant supporting documents
- [ ] I have checked for fabricated or hallucinated details (numbers, names, dates, accounts)
- [ ] I have confirmed the output is complete and addresses the full scope of the request
- [ ] I have applied my professional judgment and the output is reasonable
- [ ] I have documented any corrections or modifications I made to the AI output
- [ ] I have recorded my name, date, and review disposition in the evidence file

**Reviewer:** ___________________________

**Date:** ___________________________

**Disposition:** [ ] Accepted as-is | [ ] Accepted with modifications | [ ] Rejected

**Notes:** ___________________________

## Evidence Retention

All review evidence must be retained in the `evidence/` directory. At minimum, retain:

- The AI input (prompt or data provided)
- The AI output (complete, unmodified)
- The completed reviewer checklist
- Any modifications made before the output was used

Evidence must be retained for the same period as the underlying financial records it supports.

---

*Document Owner: Controller*
*Last Updated: March 2026*
