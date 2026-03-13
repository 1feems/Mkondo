# FlowOS

FlowOS is a funding coordination and strategy platform for ecosystem grants and other equity-free funding programs.It connects program design, AI-assisted application evaluation, and outcome tracking into a unified system. It serves ecosystem teams, protocol treasuries, and grant operators who need to move from running isolated programs to building a coherent, outcome-driven funding strategy. 


---

## The Problem

- Grant programs have no structured way to capture goals, criteria, and evaluation standards — so every round is rebuilt from scratch and nothing improves over time.
- At volume, reviewing every application manually creates backlogs, inconsistent decisions, and reviewer burnout — with no way to prioritize what's actually worth reading.
- Funding programs across grants, hackathons, and initiatives run in silos — with no shared structure to coordinate what each program is funding or how they fit together.
- Treasuries and funding decision-makers have no structured record linking funding decisions to outcomes — spend data exists but what it produced doesn't, making it difficult to justify budgets or allocate capital with confidence.
- There is no strategy layer above individual programs — no way for ecosystems to compare what different programs produced, identify what's working, and deliberately improve how they deploy capital over time.

---

## Who It's For

- **Funding Program Operators** — design and run grants and other equity-free funding programs, review applications, and make funding decisions.
- **Foundations & Ecosystem Teams** — coordinate funding programs across grants, hackathons, and initiatives and understand what funded projects are producing.
- **Protocol Treasuries & Governance** — view structured records linking funding spend to outcomes to inform reporting and capital allocation decisions.

---

## What FlowOS Does

- **Program Intent Builder** — Define program goals, desired outcomes, eligibility criteria, and funding scope before launching a funding round.
- **Structured Application Builder** — Create application forms that are directly aligned with the program's intent, evaluation criteria, and decision rubric.
- **AI-Assisted Pre-Filtering** — Automatically pre-screen incoming applications against program requirements and rubric criteria. Applications are labeled Pass / Needs Revision / Not a Fit before human review.
- **Application Intake & Review** — Collect and review submissions through a structured workflow where applications, rubrics, and AI pre-scores are already surfaced for reviewers.
- **Funding Program Registry** — The coordination and strategy layer. Connects every program, round, funded project, and outcome into a single structured view — so ecosystems can coordinate across all their funding activity, compare what each program produces, and make better capital allocation decisions over time.

---

## How It Works

1. **Define the Program** — Funding teams configure the program in FlowOS by setting core details such as eligibility, focus areas, desired outcomes, and evaluation criteria.
2. **Configure the Round** — Operators define the round's intent including budget, target applicants, project scope, and the impact metrics the program will track.
3. **Collect Applications** — Builders submit proposals through a public application form generated from the program configuration.
4. **AI-Assisted Evaluation** — Each submission is automatically evaluated against eligibility rules, round goals, expected deliverables, and the scoring rubric, returning a triage label: Pass, Needs Revision, or Not a Fit.
5. **Review & Decision** — Operators review applications in a structured queue with AI summaries and rubric scores surfaced, then approve or reject proposals.
6. **Coordination & Strategy Layer** — Approved projects are added to the registry, building a connected record across all programs and rounds. Ecosystems can see what every program is funding, compare outcomes across rounds and tracks, and allocate capital with confidence — not just spend data, but what it produced.

---

## Optional Services

Additional services available to support setup, design, and analysis using FlowOS.

- **Program Registry Setup** — Import and structure past grants, hackathons, and funding rounds in FlowOS to create a unified registry of programs and funded projects.
- **Funding Program Design** — Design and configure funding programs in FlowOS, including application forms, evaluation rubrics, builder profiles, and other program assets required to launch a round.
- **Program Assessment & Reporting** — Structure existing funding data in FlowOS and produce reports on program design and funded project outcomes.

---

## Current Build & Vision

**v1 — Operator Platform for Grant Programs**
The current build is an operator platform for ecosystem grant programs — program setup, AI-assisted application screening, structured review, and a funded project registry.

**Designed for more than grants**
Grants are the first program type. The architecture is built to support any structured funding program — hackathons, bounties, RFPs, and ecosystem initiatives. The operator layer is the entry point; the registry is what turns individual program activity into ecosystem-level coordination and strategy data over time.

**Agent pipeline**
The current agent pipeline pre-screens applications against program intent. It is designed to support additional AI interactions within the funding workflow as the platform grows.

---

## Proof of Concept

| Evidence | Document |
|---|---|
| Working prototype — core screens, mock agent pipeline, DB seed | [PRD — Current State](docs/prd.md#09--current-state) |
| Prototype — screen designs and user flows | Figma (coming soon) |
| Problem validation — direct professional experience across 4 ecosystems | [Problem Validation](research/problem-validation.md) |
| User validation — forms tested against live Stacks grant program and an accepted application (BNS One) | [User Validation](research/user-validation.md) |

---

## Documentation

**Product**

| Document | Description |
|---|---|
| [PRD](docs/prd.md) | Product requirements, scope, user flows, current build state |
| [Sitemap & System Overview](docs/sitemap.md) | Screen map, system flow, and user flows for operator and public sections |

**Research**

| Document | Description |
|---|---|
| [Problem Validation](research/problem-validation.md) | Problem validated through direct professional experience + published research |
| [User Validation](research/user-validation.md) | FlowOS forms tested against live Stacks grant program and an accepted application (BNS One) |

---

## Status

Early proof of concept — working prototype with core screens built. Agent pipeline runs on mock outputs. Grant funding wires the live Claude API integration and completes the registry layer.

---

## Founder

[Feems](founder/founder.md) — funding design researcher and strategist. Background spans the full grants stack as funder, operator, reviewer, researcher, and grantee across Gitcoin, Arbitrum, POKT, and Polygon. FlowOS is the direct product of that research.
