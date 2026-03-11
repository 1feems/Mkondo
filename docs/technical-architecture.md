# FlowOS — Technical Architecture

Early Proof of Concept

---

## Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js, Tailwind CSS |
| Backend | Next.js API Routes |
| Database | PostgreSQL, Prisma ORM |
| Auth | NextAuth.js |
| AI Agent | Claude API — structured JSON output |
| Hosting | Vercel (frontend) + Railway (database) |

---

## System Overview

```
OPERATOR SETUP
  Program Info Form       →  program config: ecosystem, eligibility, rubric
  Program Round Intent    →  round config: dates, budget, goals, metrics
  Application Form        →  field template per vertical
  Rubric                  →  scoring criteria + weights

PUBLIC FORM → INTAKE API
  Builder submits         →  POST /apply/[round-id]
  Validation              →  required fields checked
  Application created     →  linked to program + round
  Confirmation            →  application ID returned to builder

AGENT PIPELINE (async)
  Context loaded          →  program intent + rubric pulled by round
  Application evaluated   →  fields scored against program context
  Triage result saved     →  Pass / Needs Revision / Not a Fit
  Queue updated           →  application appears in operator review queue

OPERATOR REVIEW
  Decision made           →  Approve / Reject / Request Info
  On approval             →  Grant Profile auto-created in registry

REGISTRY
  Program view            →  rounds, funded projects, KPI fields
  Round summary           →  pass rate, average score, top tracks
```

---

## Data Model

| Entity | Relationships |
|---|---|
| Program | has many Rounds, one Rubric, one ApplicationForm |
| Round | belongs to Program, has many Applications |
| Application | belongs to Round and Program, has one AgentResult and one Review |
| AgentResult | belongs to Application — stores triage label, scores, strengths, risks |
| Review | belongs to Application — stores rubric scores and decision |
| RegistryProject | created on approval — linked to Application, Program, Round |

---

## Agent Design

The screening agent is a program-intent-driven prefilter. It receives structured context — program intent, eligibility criteria, rubric — and evaluates each submitted application against that context.

**Inputs**
- Program Info (ecosystem, eligibility, outcome focus)
- Round Intent (goals, target applicants, impact metrics)
- Rubric (criteria, score range, weights)
- Pre-screening answers
- Submitted application

**Output (structured JSON)**

| Field | Description |
|---|---|
| triage_label | Pass / Needs Revision / Not a Fit |
| eligible | true / false |
| rubric_pre_scores | score + rationale per criterion |
| overall_pre_score | weighted average |
| intent_alignment | 1–5 fit score against program goals |
| strengths | 2–4 specific bullets |
| risks | 2–4 specific bullets |
| revision_feedback | populated for Needs Revision only |
| summary | 2–3 sentence plain-language summary |

The agent does not make final decisions. Human reviewers score all Pass applications and make every approval decision.

---

## Current State

| Component | Status |
|---|---|
| Program setup wizard | Built |
| Public application form | Built |
| Application Intake API | Built |
| Agent pipeline | Mocked — deterministic JSON outputs |
| Operator review queue | Built |
| Registry | Built |
| Live Claude API integration | Funded milestone |

Grant funding wires the live Claude API call with structured JSON output, replacing the current mocked agent pipeline.
