# FlowOS — User Flows

Operator flows and applicant flow.

---

## Operator Flow — First Time

```
OPERATOR LOGS INTO FLOWOS
    │
    ▼
[ Step 1 ] PROGRAM INFO FORM  ← done once, never repeated for this program
    │   ├── Program name
    │   ├── Ecosystem / chain
    │   ├── Outcome Focus + Area of Focus
    │   ├── Vertical
    │   ├── Eligibility criteria (3 required)
    │   └── Rubric selection
    │
    ▼
[ Step 2 ] PROGRAM ROUND INTENT FORM  ← done each funding cycle
    │   ├── Funding Round ID
    │   ├── Grant type, open/close dates, total budget
    │   ├── Area of Focus (this round)
    │   ├── Target applicants + Projects we fund
    │   ├── Program impact metrics (1 required)
    │   ├── Application Form:  [ + Create new ]
    │   └── Rubric:            [ + Create new ]
    │
    ▼
[ Step 3 ] CONFIGURE APPLICATION FORM
    │   ├── Load vertical template (Consumer Apps / DeFi / Protocols)
    │   ├── Add / remove / reorder fields
    │   └── Mark required fields
    │
    ▼
[ Step 4 ] CONFIGURE RUBRIC
    │   ├── Add criteria with scoring guidance
    │   ├── Set score range (1–5)
    │   └── Set weights per criterion
    │
    ▼
[ Step 5 ] REVIEW & PUBLISH
    │   └── System generates: /apply/[round-id]
    │
    ▼
PROGRAM IS LIVE — operator shares URL with builders
```

---

## Operator Flow — Returning (New Round)

```
OPERATOR LOGS IN → goes to existing Program page
    │
    ▼
[ Step 1 ] PROGRAM INFO FORM  ← SKIP (already exists)
    │   Pre-filled. Edit only if program details have changed.
    │
    ▼
[ Step 2 ] PROGRAM ROUND INTENT FORM  ← update for this round
    │   ├── Pre-filled from previous round
    │   ├── Update goals, budget, dates, metrics
    │   ├── Application Form:  [ Use existing ▾ ] or [ + Create new ]
    │   └── Rubric:            [ Use existing ▾ ] or [ + Create new ]
    │
    ├── IF reusing → skip Steps 3 & 4
    ├── IF new Application Form → Step 3
    └── IF new Rubric → Step 4
    │
    ▼
[ Step 5 ] REVIEW & PUBLISH
    └── New public URL: /apply/[new-round-id]

Previous round data preserved in registry.
```

---

## Applicant Flow — Public, No Login

```
APPLICANT receives link or finds via registry
    │
    ▼
PROGRAM PAGE  /apply/[round-id]
    │   ├── Program name, description, scope
    │   ├── Eligibility requirements
    │   ├── Funding range and deadline
    │   └── [ Apply Now ]
    │
    ▼
PRE-SCREENING
    │   ├── What type of project are you building? (Dropdown)
    │   ├── Which outcome does your project primarily target? (Dropdown)
    │   └── Do you meet the following requirements? (Checklist — must check all)
    │
    ▼
FULL APPLICATION FORM
    │   ├── Project details, team info, wallet address
    │   ├── Short + long description
    │   ├── Project stage, requested amount
    │   ├── Milestone plan, prior funding, links
    │   └── Dynamic outcome response fields (if set by operator)
    │
    ▼
SUBMISSION CONFIRMATION
    │   ├── Application ID displayed
    │   └── Confirmation email sent
    │
    ▼  (applicant flow ends — agent runs async in background)
```

---

## Operator Review Flow

```
APPLICATIONS QUEUE
    │   ├── Filtered by: Pass / Needs Revision / Not a Fit
    │   └── Pass applications reviewed first
    │
    ▼
APPLICATION DETAIL
    │   ├── Left panel:  full application
    │   └── Right panel: AI Evaluation
    │           ├── Triage label + confidence
    │           ├── Rubric pre-scores per criterion
    │           ├── Strengths + Risks
    │           └── Plain-language summary
    │
    ▼
DECISION
    ├── APPROVE       → Grant Profile auto-created in registry
    ├── REJECT        → Reason recorded for program learning
    └── REQUEST INFO  → Feedback sent → applicant resubmits → re-evaluated
```
