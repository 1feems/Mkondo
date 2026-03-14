# Mkondo — User Flows

Operator flows and applicant flow.

---

## Operator Flow — First Time

```text
OPERATOR LOGS INTO MKONDO
    │
    ▼
[ Step 1 ] PROGRAM INFO FORM  ← done once, never repeated for this program
    │   ├── Program name
    │   ├── Ecosystem / chain
    │   ├── Outcome Focus + Area of Focus
    │   ├── Vertical
    │   ├── Eligibility criteria
    │   └── Rubric selection
    │
    ▼
[ Step 2 ] PROGRAM ROUND INTENT FORM  ← done each funding cycle
    │   ├── Funding Round ID
    │   ├── Grant type, open/close dates, total budget
    │   ├── Area of Focus (this round)
    │   ├── Target applicants + Projects we fund
    │   ├── Program impact metrics
    │   ├── Application Form:  [ + Create new ]
    │   └── Rubric:            [ + Create new ]
    │
    ▼
[ Step 3 ] CONFIGURE APPLICATION FORM
    │   ├── Load vertical template
    │   ├── Add / remove / reorder fields
    │   └── Mark required fields
    │
    ▼
[ Step 4 ] CONFIGURE RUBRIC
    │   ├── Add criteria with scoring guidance
    │   ├── Set score range
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

```text
OPERATOR LOGS IN → goes to existing Program page
    │
    ▼
[ Step 1 ] PROGRAM INFO FORM  ← SKIP (already exists)
    │   Pre-filled. Edit only if program details have changed.
    │
    ▼
[ Step 2 ] PROGRAM ROUND INTENT FORM  ← update for this round
    │   ├── Pre-filled from previous round
    │   ├── Update goals, budget, dates, and metrics
    │   ├── Application Form:  [ Use existing ] or [ + Create new ]
    │   └── Rubric:            [ Use existing ] or [ + Create new ]
    │
    ▼
[ Step 3 ] REVIEW & PUBLISH
    └── New public URL: /apply/[new-round-id]

Previous round data preserved in registry.
```

---

## Applicant Flow — Public, No Login

```text
APPLICANT receives link or finds via registry
    │
    ▼
PROGRAM PAGE  /apply/[round-id]
    │   ├── Program name, description, and scope
    │   ├── Eligibility requirements
    │   ├── Funding range and deadline
    │   └── [ Apply Now ]
    │
    ▼
PRE-SCREENING
    │   ├── Basic fit questions
    │   └── Eligibility check
    │
    ▼
FULL APPLICATION FORM
    │   ├── Project details
    │   ├── Team information and links
    │   ├── Project stage and funding request
    │   └── Milestones and supporting information
    │
    ▼
SUBMISSION CONFIRMATION
    │   └── Application recorded
```

---

## Operator Review Flow

```text
APPLICATIONS QUEUE
    │   ├── Filtered by screening result
    │   └── Applications organized for review
    │
    ▼
APPLICATION DETAIL
    │   ├── Full application
    │   └── Evaluation summary
    │
    ▼
DECISION
    ├── APPROVE       → project enters registry
    ├── REJECT        → decision recorded
    └── REQUEST INFO  → applicant invited to revise
```
