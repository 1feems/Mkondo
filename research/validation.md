# FlowOS — Validation Against Stacks Builder Grant Program

FlowOS forms and evaluation logic were tested against the Stacks Endowment grant program — including the live application form (Getting Started and Builder tracks), the published eligibility and evaluation guide, the Stacks rubric criteria, and an approved application (BNS One, SIP-31 #31) — to validate that the platform accurately captures what grant programs need to run structured intake and review, and to identify where current grant infrastructure falls short.

---

## What Was Tested

- **Program Info Form** — validated against Stacks program-level configuration: ecosystem identity, eligibility criteria, outcome focus, vertical, and expected deliverables
- **Round Intent Form** — validated against Stacks round-level setup: grant type, budget, target applicants, project types in scope, and impact metrics
- **Pre-Screening** — validated against Stacks eligibility gate: three questions map cleanly to program eligibility criteria and outcome focus
- **Rubric** — validated against Stacks evaluation criteria: FlowOS's six rubric criteria match Stacks exactly — same names, same 0–5 scale
  - Strategic Alignment, Ecosystem Impact, Feasibility, Budget Reasonableness, Risk Profile, Ecosystem Commitment
- **Application Form** — BNS One application used as a completed reference to confirm form fields capture what reviewers need to make consistent decisions

---

## How Stacks Currently Runs Grants

Testing against the live program revealed the current infrastructure:

- **Intake** — Google Forms, no pre-screening, any application enters the queue regardless of fit
- **Review** — GitHub Issues (sip31-interim-grants repo), reviewers comment informally, no shared rubric surfaced in the review thread
- **Decisions** — informal back-and-forth in GitHub comments, outcome depends on which reviewers engage on a given thread
- **Post-approval tracking** — milestone check-ins via GitHub comment thread on an informal cadence, no structured outcome record

The BNS One thread (#31) shows multiple reviewers engaging without a visible shared rubric, revision requests made informally through comments, and milestone updates posted as free-text replies. There is no structured record linking the approved amount to the outcome metrics the round was supposed to produce.

---

## Problems Uncovered

Testing against a live, approved application exposed structural gaps common across ecosystem grant programs:

| Problem | What It Reveals |
|---|---|
| No pre-screening before intake | Any application — regardless of fit — reaches a human reviewer. Ineligible submissions consume review time |
| No structured rubric in the review queue | Reviewers evaluate against program criteria informally. Decisions vary by reviewer, not by criteria |
| Compliance requirements surface post-approval | KYC/KYB and wallet screening requirements appear after approval, not at submission. Ineligible applicants reach the decision stage |
| No "What We Don't Fund" at intake | Exclusions exist in program documentation but are not surfaced to applicants before they apply |
| Milestone tracking is comment-based | Post-approval progress is tracked via GitHub comment threads — no structured outcome record tied to the KPIs defined at the round level |
| No registry of what rounds produced | Each round closes with no structured record of funded projects and their outcomes. Programs cannot compare what different rounds or tracks produced over time |

These are not Stacks-specific failures — they are structural gaps in how grant programs capture and communicate intent. FlowOS moves this information upstream into the program config so it drives intake, screening, and review from the start.

---

## What Validated Cleanly

- **Rubric criteria and scoring scale** — matched without modification. FlowOS's six criteria map exactly to Stacks' evaluation framework
- **Pre-screening questions** — three questions map cleanly to Stacks eligibility fields
- **Form structure** — fields captured the information reviewers need to evaluate strategic alignment, feasibility, ecosystem impact, and budget reasonableness
- **Registry KPI fields** — aligned with the outcome metrics Stacks tracks post-approval

---

## New Gaps Identified for Future Form Iterations

| Gap | What Stacks Captures | Not Yet in FlowOS |
|---|---|---|
| Ecosystem fit question | "Why is Stacks the right home for this project?" | No dedicated ecosystem alignment field in Form 1 or Form 2 |
| Long-term commitment | 6–12 months / 1–2 years / 3+ years dropdown | Not captured at intake |
| Sustainability plan | What is your plan for maintaining this after the grant ends? | Not captured at intake |
| Prior grants history | Have you received Stacks grants before? | Not captured at intake |
| KYC/KYB willingness | Surfaced on page 1 before applicant continues | Not in pre-screening gate |
| Milestone disbursement structure | 20% upfront, 30/30/20 on milestones | No field for operators to define tranche logic |

---

*Tested against: Stacks Endowment live application form, eligibility and evaluation guide (stacksendowment.co/grants-docs/eligibility-evaluation-guide), Builder Grant program track (stacksendowment.co/grants-docs/builder-grant-program-track), and approved BNS One application (github.com/stacksgov/sip31-interim-grants/issues/31).*
