# Change Management for AI Workflows

## Overview

AI workflows, skills, agents, and governance policies change over time. This document defines how those changes are made, reviewed, and tracked. The core principle is simple: **version control is the change control.**

Every change is a commit. Every production change goes through a pull request. The git history is the audit trail.

## What Is a Change

A change is any modification to:

- **AI skills or agents** -- new capabilities, updated prompts, modified logic
- **Governance policies** -- updates to any document in the `docs/` directory
- **Use case registrations** -- new entries, status changes, or modifications in the `inventory/`
- **Risk assessments** -- new assessments or updates to existing ones in `assessments/`
- **Control definitions** -- additions or changes to the control matrix
- **Evidence templates** -- structural changes to how evidence is captured

If it lives in this repository and it is being modified, it is a change.

## Key Rules

### 1. All Changes Are Committed to the Repository

No governance change happens outside of version control. If it is not in the repo, it did not happen. Email approvals, verbal agreements, and sticky notes do not count.

### 2. Pull Requests Are Required for Production Changes

Every change that affects production workflows must go through a pull request. The PR must include:

- A clear description of what is changing and why
- The relevant use case ID(s) affected, if applicable
- Identification of any new or modified controls

Direct commits to the main branch are not permitted for production-impacting changes.

### 3. Every Change Is Logged

The git commit history serves as the change log. Commit messages must be descriptive enough to understand the nature of the change without reading the diff. Examples:

- "Add UC-004: AI-assisted lease classification"
- "Update data classification: move project codes to Category 2"
- "Revise control AI-03: require two reviewers for high-risk use cases"

### 4. Version Control Is the Change Control

There is no separate change management system. The repository is the system of record. PRs are the approval mechanism. Commit history is the audit trail. Branch protections enforce the process.

## Change Process

### For Policy and Governance Documents

1. Create a branch from main
2. Make the change
3. Open a pull request with a description of the change and its rationale
4. Controller reviews and approves
5. Merge to main

### For Use Case Changes

1. Create a branch from main
2. Update the use case register and any associated assessments or controls
3. Open a pull request
4. Controller reviews and approves (IT and Legal review if scope warrants)
5. Merge to main

### For Skill or Agent Changes

1. Create a branch from main
2. Update the skill/agent code and any related documentation
3. Test the change in a non-production context
4. Open a pull request with test results or evidence
5. Finance Process Owner and Controller review
6. Merge to main

## Emergency Changes

In rare cases, a change may need to be made without the full PR process (e.g., disabling a workflow due to a data incident). Emergency changes must:

- Be committed to the repository as soon as possible
- Include a commit message prefixed with `[EMERGENCY]`
- Be followed by a retroactive PR documenting the change and its justification within 48 hours
- Be reported to the Controller immediately

Emergency changes are the exception, not the norm. If they become frequent, the process needs attention.

## Review Cadence

The Controller reviews the change log (git history) at least quarterly to confirm:

- All changes followed the documented process
- No unauthorized changes were made to production workflows
- The repository reflects the current state of all AI governance artifacts

---

*Document Owner: Controller*
*Last Updated: March 2026*
