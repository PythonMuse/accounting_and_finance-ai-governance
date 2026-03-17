# Controller's AI Governance Toolkit

A practical step-by-step guide for controllers who want to use AI tools responsibly in their accounting workflows. This is not a theoretical framework -- it is a sequence of concrete actions you can complete in your first 30 days.

---

## 1. Preparing Your Environment

Install three tools: VS Code (your editor), Claude Code (your AI assistant), and Git (your version control system). VS Code gives you a single workspace for writing policies, reviewing AI output, and managing files. Claude Code runs directly in your terminal and follows the rules you define in configuration files. Git tracks every change so you have a clear audit trail of what was written, when, and by whom. If your IT team manages installations, send them the list and ask for local installs -- no cloud accounts are needed for the governance repo itself.

**Action items:**
- Install VS Code, Claude Code CLI, and Git
- Open a terminal in VS Code and confirm each tool runs (`code --version`, `claude --version`, `git --version`)
- Bookmark the Claude Code documentation for reference

---

## 2. Setting Up the Governance Repository

Create a dedicated Git repository for your AI governance artifacts. This is where your policy, use case register, risk assessments, skills, and evidence will live. The repository structure separates concerns cleanly: policies at the root, assessments in their own folder, skills defined individually, and evidence captured with date-stamped logs. Initialize the repo with `git init`, create the folder structure, and make your first commit.

**Action items:**
- Run `git init finance-ai-governance` in your working directory
- Create folders: `assessments/`, `skills/`, `evidence/run-logs/`, `evidence/review-notes/`, `toolkit/`, `examples/`
- Add a `README.md` describing the repository purpose
- Make your first commit: `git add . && git commit -m "Initialize governance repo"`

---

## 3. Writing Your AI Policy

Your AI policy does not need to be long. It needs to answer four questions: what AI tools are approved, what data can be used, who reviews the output, and how evidence is retained. Write this as a plain markdown file called `ai-policy.md` at the repo root. Keep the language direct -- this document should be readable by any member of your accounting team without explanation. Reference your data classification levels (Public, Internal, Confidential, Regulated) and state that Confidential and Regulated data must never be sent to AI tools without explicit masking and approval.

**Action items:**
- Create `ai-policy.md` at the repo root
- Define approved tools, data handling rules, reviewer requirements, and evidence retention
- Have your CFO or equivalent review and approve the policy
- Commit the approved version to Git

---

## 4. Building the Use-Case Inventory

Before you use AI for any accounting task, document it in a use-case register. This is a simple CSV or markdown table that lists each use case with an ID, process name, description, data classification, risk level, and approval status. Start with one use case -- bank reconciliation review is a good first candidate because the data can be easily masked and the output is straightforward to verify. Add more use cases only after the first one is tested and approved.

**Action items:**
- Create `inventory/use-case-register.csv` using the provided template
- Add your first use case (UC-001) with status "Pilot"
- Review the register with your team to identify 2-3 additional candidates
- Commit the register to Git

---

## 5. Designing Controls

Each use case needs controls that match the risks involved. Use the COSO framework as your guide: confirm the control environment supports AI use, assess the specific risks, define control activities (masking, review, evidence), establish communication channels, and set up monitoring. For a medium-risk use case like bank reconciliation, you will typically need a preventive control (data masking), a detective control (human review), and a monitoring control (evidence retention). Document each control using the control design template.

**Action items:**
- Complete a risk assessment for your first use case using `assessments/templates/risk-template.md`
- Document each control using `assessments/templates/control-template.md`
- Link controls back to the use case in the register
- Get sign-off from a second reviewer

---

## 6. Creating Your First Skill

A skill is a set of instructions that tells the AI exactly what it can do, what data it can use, and what output format to produce. Write it as a `SKILL.md` file inside a folder named for the skill (e.g., `skills/bank-rec-review/SKILL.md`). The skill file defines allowed inputs, prohibited inputs, the required workflow, output format, and evidence requirements. This is your guardrail -- the AI follows these instructions, and anyone reviewing the work can see exactly what was permitted.

**Action items:**
- Create `skills/bank-rec-review/SKILL.md` using the filled-in example
- Test the skill against sample data in `examples/demo-data/`
- Review the output and confirm it matches expected results
- Commit the skill and test evidence to Git

---

## 7. Evidence and Monitoring

Every time the AI runs a skill, save the output to `evidence/run-logs/` with a date-stamped filename. This creates a clear trail that auditors and reviewers can follow. Pair run logs with review notes in `evidence/review-notes/` where the reviewer documents what they checked, what they approved, and any exceptions found. Set a monthly cadence to review accumulated evidence and assess whether controls are working as intended. After 90 days, reassess each use case's risk rating based on actual experience.

**Action items:**
- Save every AI output to `evidence/run-logs/` with naming format `YYYY-MM-DD_UC-XXX_skill-name.md`
- Document each review in `evidence/review-notes/`
- Schedule a monthly evidence review on your calendar
- Reassess risk ratings after 90 days of production use

---

## 30-Day Starter Sequence

| Day   | Action                                                          |
|-------|-----------------------------------------------------------------|
| 1-2   | Install VS Code, Claude Code, and Git                          |
| 3     | Initialize the governance repository with folder structure       |
| 4-5   | Write and approve `ai-policy.md`                                |
| 6-7   | Create `data-classification.md` defining your four levels        |
| 8-9   | Set up the use-case register with UC-001                         |
| 10    | Write `CLAUDE.md` with project-level instructions                |
| 11-12 | Complete the risk assessment for UC-001                          |
| 13-14 | Document controls for UC-001 using the control template          |
| 15-16 | Create the `bank-rec-review` skill                               |
| 17-18 | Test the skill on sample data, save evidence                     |
| 19-20 | Have a second reviewer check outputs and sign off                |
| 21-22 | Run the skill on actual masked production data                   |
| 23-24 | Save production evidence and review notes                        |
| 25-26 | Identify your second use case (UC-002)                           |
| 27-28 | Draft UC-002 risk assessment                                     |
| 29-30 | Conduct 30-day retrospective and update the use-case register    |
