# FlowOS — Site Map

---

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
│       ├── Step 1 — Program Info Form        Name, ecosystem, mission, eligibility, rubric
│       ├── Step 2 — Program Round Intent     Dates, budget, goals, outcomes, metrics
│       │           └── Application Form: [ Use existing ▾ ] or [ + Create new ]
│       │           └── Rubric:           [ Use existing ▾ ] or [ + Create new ]
│       ├── Step 3 — Application Form Setup   (skipped if reusing existing)
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

──────────────────────────────────────────────────
PUBLIC (no login required)
    ├── /apply/[round-id]           Live application form — generated per round
    └── /confirm                    Submission confirmation + application ID
```

---

## Key Rules

| Rule | Description |
|---|---|
| Program is permanent | Created once. Rounds are created per cycle |
| No builder login | Applicants access via public URL only |
| Pre-screening first | 3 questions before full form loads |
| Agent runs async | Applicant does not wait for agent result |
| Human decision always final | Agent triages, operator approves |
| Forms are reusable | Saved in Forms Library — reuse across rounds |
| Registry auto-updates | Approved applications create registry rows automatically |
