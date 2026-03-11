# FlowOS — Product Requirements Document

Early Proof of Concept

---

## 01 — Product Overview

FlowOS is a funding coordination platform that helps ecosystems design clear grant programs, run AI-assisted intake and review, and maintain a program-level registry of rounds, funded projects, and their agreed impact metrics.

We turn chaotic, fragmented grant activity into a structured funding lifecycle — one that lets ecosystems aim capital at the right projects and learn from every round.

**What FlowOS lets funders do**

| Action | What it means |
|---|---|
| Design | Define program intent — goals, tracks, eligibility — in a clear, reusable schema |
| Screen | Run AI-powered intake that pre-filters and labels applications — Pass / Needs Revision / Not a Fit |
| Review | Review with consistent rubrics instead of ad-hoc criteria |
| Learn | Keep a registry of programs, rounds, and funded projects with pre-defined impact metrics |

**What FlowOS is not**
FlowOS does not do milestone tracking, payment processing, or end-to-end grant ops. It does one thing well: structured program design, AI-assisted triage, consistent review, and a registry that lets ecosystems compare what their capital actually produced.

---

## 02 — Problem Statement

FlowOS serves crypto and Web3 ecosystems that run non-dilutive funding programs — foundations, DAOs, L2s, treasuries — and the operators who manage those programs.

**The four core breakdowns**

| Problem | Description |
|---|---|
| No unified lifecycle | Funding programs are scattered across forums, Notion pages, forms, and spreadsheets. No unified flow from program intent → applications → approvals → outcomes |
| Inconsistent review | Funders drown in proposals evaluated against ad-hoc criteria — decisions are slow, inconsistent, and impossible to compare across rounds |
| No outcome visibility | Ecosystems publish spend data but rarely have structured outcome data. They cannot tell which programs or tracks are actually working |
| No program-level learning | Data about rounds and funded projects is scattered — ecosystems cannot see, compare, or iterate on what their programs actually produce over time |

---

## 03 — Target Users

| User | Role | What FlowOS gives them |
|---|---|---|
| Grant / Ecosystem Funding Operators | Design programs, run rounds, coordinate reviewers | Structured intent forms, AI pre-filtering, clear review queue |
| Ecosystem / Growth Leads | Decide where non-dilutive capital goes | Program registry and metrics to compare rounds and tracks |
| Foundations / Governance Committees | Approve budgets, accountable for impact | At-a-glance view of what funded projects are delivering |
| Builders / Applicants | Submit applications | Public form with no login required. Structured feedback if revision needed |

---

## 04 — Product Scope

**In scope**
- Program creation wizard — Program Intent Form, Application Form Setup, Rubric Setup
- Public-facing application form — builder-facing, no login required
- Application Intake API — validates, stores, triggers agent
- Screening agent — Pass / Needs Revision / Not a Fit triage against program intent
- Operator review queue — full application + AI evaluation + rubric scoring + decision
- Program registry — programs, rounds, funded projects, KPI rollups

**Out of scope**
- Grantee milestone tracking
- Payment processing or on-chain disbursements
- Multi-tenant architecture
- Full authentication system
- Real-time collaboration between reviewers
- Mobile-optimized views

---

## 05 — Key User Flows

**Core demo flow**
1. Operator creates a program and defines KPIs in the registry
2. Builder submits an application via the public form URL — no login
3. Agent runs eligibility and fit check — returns Pass / Needs Revision / Not a Fit
4. Operator clicks Approve — auto-creates the Grant Profile and updates the registry
5. Registry shows the funded project with KPI fields ready to fill

**Operator flow**
1. Creates program — name, ecosystem, mission, budget, eligibility, logo
2. Creates round — dates, funding range, tracks, max applications
3. Completes Program Intent Form — goals, user outcomes, evaluation criteria
4. Configures Application Form — loads vertical template, sets required fields
5. Sets Rubric — criteria, score ranges, weights
6. Publishes program — system generates a public application URL
7. Shares URL — builders submit via public page — no login
8. Receives applications in queue — post-agent screening, sorted by triage label
9. Reviews Pass applications — sees full application + AI evaluation + pre-scores
10. Makes decision — Approve / Reject / Request Info

**Builder flow**
1. Receives application link from operator or program page
2. Opens public form — no account required
3. Answers pre-screening questions — confirms fit before full form loads
4. Fills out application and submits
5. Sees confirmation screen with application ID
6. If Needs Revision — receives structured feedback and resubmits

---

## 06 — Core Features

**Program Intent Builder**
Operators define program goals, target applicants, eligibility criteria, tracks, and KPI metrics in a structured form before any applications are accepted. This intent config drives the application form template, the agent's evaluation lens, the rubric, and the registry's KPI fields.

**Application Intake**
A public-facing form URL is generated per round on publish. Builders submit with no login required. The Application Intake API validates required fields, stores the submission, returns a confirmation with an application ID, and triggers the screening agent asynchronously.

**AI-Assisted Pre-Filtering**
The screening agent reads program intent + rubric + submitted application and returns a structured triage result. Pass → main review queue. Needs Revision → actionable feedback returned to applicant. Not a Fit → recorded with reasons for program learning.

**Application Intake & Review**
All Pass applications enter the review queue. Operators and reviewers see the full application, the agent's evaluation summary and pre-scores, and the rubric. Reviewers score each criterion and make a final decision. Human judgment is always final.

**Funding Program Registry**
Stores program, round, and track records. Approved applications auto-create a funded project row with KPI fields defined at the program level. Registry views show program-level summaries across rounds.

---

## 07 — Screening Agent

The FlowOS screening agent is a program-intent-driven prefilter. It reads program intent, eligibility criteria, and evaluation rubric, then triages each application into Pass / Needs Revision / Not a Fit.

See [agent section in private repo] for full agent PRD, directives, and output schema.

**Agent output fields**

| Field | Description |
|---|---|
| triage_label | Pass / Needs Revision / Not a Fit |
| confidence | High / Medium / Low |
| eligible | true / false |
| rubric_pre_scores | Score per criterion with rationale |
| overall_pre_score | Weighted average across rubric |
| intent_alignment | 1–5 score — fit with program goals |
| strengths | 2–4 specific bullets |
| risks | 2–4 specific bullets |
| revision_feedback | Populated for Needs Revision only |
| not_a_fit_reason | Populated for Not a Fit only |
| tags | Outcome tags feeding the registry |
| summary | 2–3 sentence plain-language summary |

The agent does not make final decisions. Human reviewers score all Pass applications and make every approval decision. Operators retain full control.

---

## 08 — Grant Registry

**Program-level view per round**
- Round ID, Grant Type, Open Date, Close Date
- Total Applications, Approved Grants, Total Allocated, Average Grant Size
- Top tracks, pass rate, common agent flags

**Per-grant profile (auto-created on approval)**
- Program / Round / Track, Grant Type, Approved Amount, Decision Date, Status
- KPI metric slots defined at program level
- External ID link for cross-platform tracking if applicable

---

## 09 — Current State

**What exists today**
- Working prototype with core screens: Dashboard, Applications Queue, Application Detail, AI Evaluation panel, Decision screen
- Functional forms: Program Info, Program Intent, Application Form (public), Rubric
- Application Intake API endpoint
- Mock agent pipeline — hardcoded JSON output per application, identical UI to live agent
- DB seed script with sample programs, rounds, applications, agent results, registry projects
- Registry — Programs Table and Program Page

**What is mocked vs functional**
- Agent outputs are currently deterministic mocks. Grant funding wires the live Claude API call with structured JSON output.

---

## 10 — Risks

| Risk | Mitigation |
|---|---|
| Agent accuracy depends on intent form quality | Structured template with examples and validation |
| Operator adoption requires workflow change | Playbook and documentation lower adoption barrier |
| Builder form completion rates | Clear field guidance, Needs Revision flow returns actionable feedback |
| KPI fields left empty | Registry design makes empty fields visible — social pressure without enforcement |

---

## 11 — Roadmap (Post v1)

- Live LLM agent — replace mocked outputs with Claude API structured JSON calls
- Form builder UI — configurable field builder for custom application forms without code
- Multi-program support — multiple ecosystem programs running simultaneously
- Cross-round registry intelligence — which programs and tracks produced best outcomes over time
- External integrations — on-chain registry hooks, cross-platform export, CSV / API
