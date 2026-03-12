# FlowOS

FlowOS is a funding coordination and strategy platform for ecosystem grants and other equity-free funding programs that helps ecosystems save time, coordinate funding programs, and make better funding decisions. It connects program design, AI-assisted application evaluation, and funded project data into one system so ecosystems can understand what their capital produces and improve funding programs over time.

---

## The Problem

- Grant programs have no structured way to capture goals, criteria, and evaluation standards — so every round is rebuilt from scratch and nothing improves over time.
- At volume, reviewing every application manually creates backlogs, inconsistent decisions, and reviewer burnout — with no way to prioritize what's actually worth reading.
- Funding programs across grants, hackathons, and initiatives run in silos — with no shared structure to coordinate what each program is funding or how they fit together.
- Treasuries and funding decision-makers have no structured record linking funding decisions to outcomes — spend data exists but what it produced doesn't, making it difficult to justify budgets or allocate capital with confidence.

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
- **Funding Program Registry** — Maintain a record of every program, round, funded project, and outcome — allowing ecosystems to compare programs and improve funding strategies over time.

---

## How It Works

1. **Define the Program** — Funding teams configure the program in FlowOS by setting core details such as eligibility, focus areas, desired outcomes, and evaluation criteria.
2. **Configure the Round** — Operators define the round's intent including budget, target applicants, project scope, and the impact metrics the program will track.
3. **Collect Applications** — Builders submit proposals through a public application form generated from the program configuration.
4. **AI-Assisted Evaluation** — Each submission is automatically evaluated against eligibility rules, round goals, expected deliverables, and the scoring rubric, returning a triage label: Pass, Needs Revision, or Not a Fit.
5. **Review & Decision** — Operators review applications in a structured queue with AI summaries and rubric scores surfaced, then approve or reject proposals.
6. **Program Registry** — Approved projects are automatically added to the FlowOS registry, creating a structured record of funding activity including program-level views, project profiles, and an application database with status tracking across all rounds.

---

## Optional Services

Additional services available to support setup, design, and analysis using FlowOS.

- **Program Registry Setup** — Import and structure past grants, hackathons, and funding rounds in FlowOS to create a unified registry of programs and funded projects.
- **Funding Program Design** — Design and configure funding programs in FlowOS, including application forms, evaluation rubrics, builder profiles, and other program assets required to launch a round.
- **Program Assessment & Reporting** — Structure existing funding data in FlowOS and produce reports on program design and funded project outcomes.

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
