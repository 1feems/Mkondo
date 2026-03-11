# FlowOS — Product Overview

---

## What It Is

FlowOS is a funding strategy platform for Web3 ecosystems. It gives foundations, DAOs, L2s, and treasuries the infrastructure to design funding programs with clear intent, run them consistently, and build a structured record of what each round actually produced — so capital allocation improves over time instead of resetting every cycle.

The platform implements the full funding lifecycle: Design (program intent and goals), Fund (structured intake, AI-assisted triage, consistent review), and Assess (registry of outcomes linked to spend). Most programs only do Fund. FlowOS closes the loop.

---

## The Problem

Foundations, DAOs, L2s, and treasuries running non-dilutive funding programs are operating without strategic infrastructure — fragmented tools, no shared logic between rounds, and no structured way to see what their capital actually produced. This is happening exactly as grant volume, incentive programs, and scrutiny over impact are all sharply increasing.

**No unified lifecycle**
Funding programs are scattered across forums, Notion pages, forms, and spreadsheets. There is no clear path from program intent → applications → approvals → outcomes. Every round is rebuilt from scratch.

**Inconsistent review**
Funders and reviewers work through large volumes of proposals evaluated against ad-hoc criteria. Decisions are slow, inconsistent, and hard to compare across rounds or programs.

**No outcome visibility**
Ecosystems publish spend data but rarely have structured outcome data — TVL, users, infrastructure readiness. They can't tell which programs or tracks are actually working or which investments delivered.

**No program-level learning**
Data about rounds and funded projects is scattered across tools. Ecosystems can't see, compare, or iterate on what their different programs produce over time. Every round is an island.

The root cause is not a lack of tools. It's a missing strategic layer — no shared logic connecting why a program exists, what it funds, and what it should be measuring.

---

## What FlowOS Does

FlowOS turns program intent into structured configuration that everything downstream reads from — the application form, the AI agent, the rubric, and the registry. When the intent is clear and structured, every part of the program runs from the same source of truth.

**Design — before applications open**
The operator fills out two forms: one that defines the program (goals, eligibility, outcome focus, rubric) and one that sets the specifics for the current round (budget, dates, target applicants, impact metrics). This is the strategic alignment step most programs skip.

**Fund — intake and review**
When applications come in, an AI agent reads each one against the program intent and returns a structured triage result:

- **Pass** — meets eligibility, aligns with round goals, moves to the human review queue
- **Needs Revision** — eligible but incomplete or misaligned — applicant receives specific, actionable feedback and can resubmit
- **Not a Fit** — fails eligibility or is fundamentally misaligned — recorded with reasons for program learning

Reviewers see every Pass application with AI pre-scores and rationale already surfaced — scored against each rubric criterion, with strengths, risks, and a plain-language summary. Human judgment makes every final decision.

**Assess — after approval**
Funded projects are automatically added to a registry with the KPI fields defined at the program level. Over time the registry becomes a structured record of what each program funded and what it produced — comparable across rounds and tracks. This is the intelligence layer that makes the next round better than the last.

---

## Who It's For

**Ecosystem and growth leads** — deciding where non-dilutive capital goes. FlowOS gives them a program-level view of what different rounds and tracks are producing, so allocation decisions are based on structured outcome data, not intuition.

**Foundations and governance committees** — accountable for impact. FlowOS gives them structured outcome data linked to spend, not just a list of who received funding.

**Grant operators** — running programs day to day. FlowOS handles first-pass screening and rubric scoring so they spend their time on applications that actually belong in the review queue.

**Builders and applicants** — submitting through a public link, no account needed. If their application needs work, they receive specific feedback on what to fix rather than a generic rejection.

---

## What Makes It Different

**Intent drives everything.**
The Program Intent Form is filled once per round. It defines goals, eligibility, target applicants, and KPIs. That config drives the application form, the agent's evaluation lens, the rubric, and the registry's outcome fields. There is no gap between what the program says it funds and what it actually evaluates.

**The registry closes the loop.**
Most platforms handle intake. FlowOS also captures what programs produce. Funded projects are stored with operator-defined KPI fields, making outcomes comparable across rounds. A grant program becomes a learning system.

**The AI sits on the program side, not the applicant side.**
Other platforms add AI to help applicants polish submissions. FlowOS's agent is program-aware triage — it reads program intent plus the application and returns Pass / Needs Revision / Not a Fit relative to what this round is trying to fund. The output is framed in terms of fit, not generic quality. Reviewer time goes to applications that are actually in scope.

---

## Services

The platform operationalizes funding strategy. The services produce it. For ecosystems not yet ready to run the platform independently, FlowOS offers direct engagements that deliver the same strategic layer.

### Available Now

**Program Design**
Define program goals, tracks, eligibility, rubric, and KPIs before a round opens. Produces the intent configuration that drives all downstream decisions — and that becomes the program's FlowOS config when the platform is adopted. Directly addresses the most common failure point: programs that launch without clear, structured intent.

**Program Assessment**
Audit an existing grant program against the CAMF lifecycle framework. Identifies where the Design → Fund → Assess loop is broken — missing intent structure, inconsistent review criteria, no outcome tracking. Produces a structured findings report with specific recommendations. Often the first step before Program Design.

### Future

**Impact Reporting**
After a round closes, produce a structured report linking spend to tagged outcomes — which tracks worked, what the capital produced, what to change next round. Requires the registry layer to be populated. Becomes the primary deliverable for governance committees and foundations accountable for impact.

**Cross-Program Benchmarking**
Compare a program's outcomes against others in the same ecosystem or across chains. Requires multi-program registry data. Creates the basis for ecosystem-level funding strategy, not just program-level decisions.

---

## Why Now

Grant volume, incentive programs, and scrutiny over capital allocation are all increasing at the same time. The manual process that worked when programs received 20 applications per round is breaking at 100. More importantly, ecosystems are being asked to demonstrate that their funding produced outcomes — not just that it was distributed. The infrastructure to answer that question doesn't exist yet for most programs. FlowOS builds it.

---

## Current Status

Working prototype with all core screens built. Forms validated against real grant program data. The AI screening pipeline runs on test data with mocked outputs — the next milestone wires it to a live AI model with structured JSON output.

Grant funding supports building the live AI integration and completing the registry layer.

---

## What FlowOS Does Not Do

FlowOS does not process payments, track milestones post-funding, or replace human reviewers. It provides the strategic infrastructure layer — structured program design, consistent intake, AI-assisted triage, and outcome record-keeping — so the humans in the process can focus on decisions that require judgment.
