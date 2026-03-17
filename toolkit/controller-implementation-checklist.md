# Controller Implementation Checklist

Use this checklist to track your progress implementing AI governance over the first four weeks. Check off each item as you complete it.

---

## Week 1: Foundation

- [ ] Approve pilot use case (UC-001) with Controller sign-off
- [ ] Create governance repository (`git init finance-ai-governance`)
- [ ] Write `ai-policy.md` defining approved tools, data rules, review requirements, and evidence retention
- [ ] Write `data-classification.md` defining Public, Internal, Confidential, and Regulated levels
- [ ] Commit both policy files to Git with descriptive commit messages
- [ ] Confirm VS Code, Claude Code, and Git are installed and working

## Week 2: Structure

- [ ] Create use-case register (`inventory/use-case-register.csv`) with UC-001 as the first entry
- [ ] Write `CLAUDE.md` at the repo root with project-level instructions for Claude Code
- [ ] Add `.claude/settings.json` with deny rules for sensitive file patterns (e.g., `*.env`, `*credentials*`)
- [ ] Create folder structure: `assessments/`, `skills/`, `evidence/`, `toolkit/`, `examples/`
- [ ] Review use-case register with accounting team and identify 2-3 additional candidates
- [ ] Commit all structural files to Git

## Week 3: Controls

- [ ] Write risk assessment for UC-001 using `assessments/templates/risk-template.md`
- [ ] Document controls for UC-001 using `assessments/templates/control-template.md`
- [ ] Create `skills/bank-rec-review/SKILL.md` with allowed inputs, prohibited inputs, and workflow
- [ ] Test the skill on sample data from `examples/demo-data/`
- [ ] Review AI output against expected results and document findings
- [ ] Commit risk assessment, controls, and skill files to Git

## Week 4: Validation

- [ ] Run the bank-rec-review skill on masked production data
- [ ] Save AI output to `evidence/run-logs/` with date-stamped filename
- [ ] Have Controller or Accounting Manager complete the reviewer checklist
- [ ] Document review findings in `evidence/review-notes/`
- [ ] Complete reviewer sign-off on UC-001 risk assessment
- [ ] Conduct 30-day retrospective: what worked, what to adjust, next use case
- [ ] Update the use-case register with lessons learned and status changes

---

## Post-Week-4 Ongoing

- [ ] Schedule monthly evidence review
- [ ] Identify and document UC-002
- [ ] Reassess UC-001 risk rating after 90 days
- [ ] Share governance approach with audit committee or external auditors
