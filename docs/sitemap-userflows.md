# FlowOS — Site Map & User Flows

Operator flows · Applicant flow · Program vs Round logic · Data flows

---

## 1. The Mental Model

Three roles. One system. Everything flows from this.

| Role | What they do |
|---|---|
| Operator | Creates the program, sets intent, reviews applications, makes decisions |
| Applicant / Builder | Submits via public form — no login required |
| Agent | Reads program context + application, returns triage label and scores |

---

## 2. Program vs Round

A Program is a parent container — created once, reused across many rounds. A Round is a single funding cycle within that program.

| | Program | Round |
|---|---|---|
| Created | Once | Each funding cycle |
| Contains | Name, ecosystem, eligibility, rubric | Dates, budget, intent, forms |
| Example | Stacks Builder Grant | SBG-Q2-2026 |

---

## 3. Site Map

```
FlowOS
│
├── Dashboard
│   ├── Overview                    Stats: programs, applications, funded, pending review
│   ├── Applications to Review      Reviewer queue — pre-screened by agent
│   ├── Active Programs             Programs currently open for applications
│   └── Recent Activity             Feed of submissions and decisions
│
├── Create
│   └── Create Program (wizard)
│       ├── Step 1 — Program Info         Name, ecosystem, mission, eligibility, logo
│       ├── Step 2 — Program Round Intent Dates, budget, goals, outcomes, criteria
│       │           └── Application Form: [ Use existing ▾ ] or [ + Create new ]
│       │           └── Rubric:           [ Use existing ▾ ] or [ + Create new ]
│       ├── Step 3 — Application Form Setup  (skipped if reusing existing)
│       ├── Step 4 — Rubric Setup             (skipped if reusing existing)
│       └── Step 5 — Review & Publish  → generates public application URL
│
├── Forms  (library of saved forms — reusable across rounds)
│   ├── Program Info Forms
│   ├── Program Round Intent Forms
│   ├── Application Forms
│   └── Rubrics
│
├── Applications
│   ├── Applications Queue          All incoming — filtered by status
│   ├── Application Detail          Full submission view
│   ├── AI Evaluation               Agent output: scores, strengths, risks, recommendation
│   ├── Decision                    Approve / Reject / Request Info
│   └── Funded Applications         Internal list of approved grants
│
└── Registry  (public-facing)
    ├── Programs Table              Total rounds, applications, funded, $ distributed
    └── Program Page                Rounds summary · Funding stats · Funded projects

PUBLIC (no login required)
    ├── /apply/[round-id]           Live application form — generated per round
    └── /confirm                    Submission confirmation + application ID
```

---

## 4. Operator Flow — First Time

The operator is setting up FlowOS for the first time. Everything is created from scratch.

```
OPERATOR LOGS INTO FLOWOS
    │
    ▼
[ Step 1 ] PROGRAM INFO FORM  ← done once, never repeated for this program
    │   ├── Program name
    │   ├── Ecosystem / chain
    │   ├── Mission and description
    │   ├── Outcome Focus + Area of Focus
    │   ├── Vertical
    │   ├── Eligibility criteria (3 required)
    │   └── Rubric selection
    │
    ▼
[ Step 2 ] PROGRAM ROUND INTENT FORM  ← done each funding cycle
    │   ├── Funding Round ID
    │   ├── Grant type
    │   ├── Open date / close date
    │   ├── Total budget
    │   ├── Area of Focus (this round)
    │   ├── Target applicants
    │   ├── Projects we fund
    │   ├── Program impact metrics
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
    │   ├── Add criteria (Strategic Alignment, Feasibility, Ecosystem Impact, etc.)
    │   ├── Set score range (1–5)
    │   └── Set weights per criterion
    │
    ▼
[ Step 5 ] REVIEW & PUBLISH
    │   ├── Summary of program + round + intent + forms
    │   ├── Operator clicks PUBLISH
    │   └── System generates: public URL  /apply/[round-id]
    │
    ▼
PROGRAM IS LIVE — operator shares URL with builders
```

---

## 5. Operator Flow — Returning (New Round)

The Program already exists. The operator is starting a new funding cycle.

```
OPERATOR LOGS IN → goes to existing Program page
    │
    ▼
[ Step 1 ] PROGRAM INFO FORM  ← SKIP (already exists)
    │   Pre-filled. Operator can edit if program details have changed.
    │
    ▼
[ Step 2 ] PROGRAM ROUND INTENT FORM  ← update for this round
    │   ├── Pre-filled from previous round
    │   ├── Update goals, budget, dates
    │   ├── Application Form:  [ Use existing ▾ ] or [ + Create new ]
    │   └── Rubric:            [ Use existing ▾ ] or [ + Create new ]
    │
    ├── IF reusing existing forms → skip Steps 3 & 4
    ├── IF creating new Application Form → Step 3
    └── IF creating new Rubric → Step 4
    │
    ▼
[ Step 5 ] REVIEW & PUBLISH
    └── New public URL generated: /apply/[new-round-id]

Previous round data preserved in registry.
```

---

## 6. Applicant Flow — Public, No Login

```
APPLICANT receives link from operator or finds via registry
    │
    ▼
PROGRAM PAGE  /apply/[round-id]
    │   ├── Program name and description
    │   ├── What we fund (scope)
    │   ├── Eligibility requirements
    │   ├── Funding range and deadline
    │   └── [ Apply Now ] button
    │
    ▼
PRE-SCREENING  (before full form loads)
    │   ├── What type of project are you building? (Dropdown)
    │   ├── Which outcome does your project primarily target? (Dropdown)
    │   └── Do you meet the following requirements? (Checklist — must check all)
    │
    ▼
FULL APPLICATION FORM
    │   ├── Project details (name, website, GitHub, vertical)
    │   ├── Team info (name, size, builder names, wallet address)
    │   ├── Short description (1–2 sentences)
    │   ├── Long description / problem statement
    │   ├── Project stage (Idea / Prototype / Live)
    │   ├── Requested grant amount
    │   ├── Milestone plan
    │   ├── Prior funding received
    │   └── Relevant links
    │
    ▼
SUBMISSION CONFIRMATION
    │   ├── Application ID displayed (e.g. APP-2026-0042)
    │   └── Confirmation email sent
    │
    ▼  (system continues automatically — applicant flow ends here)
    │
    ▼
AGENT TRIGGERED (async)
    └── Evaluates application → returns Pass / Needs Revision / Not a Fit
    └── Result saved → application appears in operator queue
```

---

## 7. Operator Review Flow

```
OPERATOR OPENS APPLICATIONS QUEUE
    │   ├── Filtered by: Pass / Needs Revision / Not a Fit
    │   └── Pass applications reviewed first
    │
    ▼
OPERATOR OPENS APPLICATION DETAIL
    │   ├── Left panel: full application
    │   └── Right panel: AI Evaluation
    │           ├── Triage label
    │           ├── Confidence
    │           ├── Rubric pre-scores
    │           ├── Strengths + Risks
    │           └── Plain-language summary
    │
    ▼
OPERATOR DECISION
    │
    ├── APPROVE → Grant Profile auto-created in registry
    ├── REJECT  → Reason recorded for program learning
    └── REQUEST INFO → Feedback sent to applicant → resubmit → re-evaluated
```

---

## 8. Data Flow

```
OPERATOR SETUP
  Program Info Form       →  program_id, name, ecosystem, eligibility, rubric
  Program Round Intent    →  round_id, dates, budget, goals, outcomes, metrics

PUBLIC FORM → APPLICATION INTAKE API
  Builder submits         →  POST /apply/[round-id]
  Validation              →  required fields checked
  Application created     →  application_id linked to program_id + round_id
  Confirmation            →  application ID + email sent to applicant

AGENT PIPELINE (async)
  Context loaded          →  program + intent + rubric pulled by round_id
  Evaluation run          →  application fields evaluated against context
  AgentResult saved       →  triage_label, scores, strengths, risks, tags
  Queue updated           →  application appears in operator queue

OPERATOR REVIEW
  Decision saved          →  APPROVED / REJECTED / REVISION_REQUESTED
  If APPROVED             →  RegistryProject row auto-created

REGISTRY
  Program Page            →  aggregates all rounds + funded projects
  KPI fields              →  filled by operator post-funding
  Round Summary           →  pass rate, avg score, top tracks (on round close)
```

---

## 9. Key Rules

| Rule | Description |
|---|---|
| Program is permanent | Created once. Rounds are created per cycle |
| No builder login | Applicants access via public URL only |
| Pre-screening first | 3 questions before full form loads |
| Agent runs async | Applicant does not wait for agent result |
| Human decision always final | Agent triages, operator approves |
| Forms are reusable | Saved in Forms Library — reuse across rounds |
| Registry auto-updates | Approved applications create registry rows automatically |
| Round data is preserved | Closing a round does not delete data |
