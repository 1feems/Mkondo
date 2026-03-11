# FlowOS

Program design and intake infrastructure for ecosystem grant programs — structured intake, AI-assisted screening, and a registry of what each round produced.

---

## The Problem

Ecosystem grant programs have no structured way to define what they're funding before intake opens. Applications arrive with no pre-filtering. Reviews happen against ad-hoc criteria that change every round. When a round closes, there's no record of what the capital actually produced.

Every round is rebuilt from scratch. Performance is invisible. Nothing carries forward.

---

## What FlowOS Does

FlowOS gives grant operators a connected system for the full funding lifecycle:

- **Program Intent Builder** — Define goals, eligibility, tracks, and KPI metrics before intake opens
- **AI-Assisted Pre-Filtering** — Every application is evaluated against program intent and labelled Pass / Needs Revision / Not a Fit before any human reviews it
- **Structured Review Queue** — Operators and reviewers work from the same rubric every round, with AI pre-scores already surfaced
- **Funding Program Registry** — A structured record of every round, funded project, and outcome — comparable across rounds and programs over time

---

## Proof of Concept

| Evidence | Document |
|---|---|
| Working prototype — core screens, mock agent pipeline, DB seed | [PRD — Current State](docs/prd.md#09--current-state) |
| Technical spec — stack, data flow, agent schema | [Technical Architecture](docs/technical-architecture.md) |
| Problem validation — direct professional experience across 4 ecosystems | [Problem Validation](research/problem-validation.md) |
| User validation — forms tested against live Stacks grant program and an accepted application (BNS One) | [User Validation](research/user-validation.md) |

---

## Documentation

**Product**

| Document | Description |
|---|---|
| [PRD](docs/prd.md) | Product requirements, scope, user flows, current build state |
| [Technical Architecture](docs/technical-architecture.md) | Stack, data flow, agent design, entity relationships |
| [Forms Specification](docs/forms-spec.md) | Field reference for all operator and applicant forms |
| [Sitemap](docs/sitemap.md) | Full screen map — operator and public sections |
| [User Flows](docs/userflows.md) | Step-by-step flows for operator setup, builder submission, and review |

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
