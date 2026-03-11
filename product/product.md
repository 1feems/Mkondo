# FlowOS — Product Overview

FlowOS is a funding strategy platform for crypto ecosystems. It gives the teams running non-dilutive capital programs a structured way to design programs, run consistent intake and review, and track what their funding produced — so every round builds on the last instead of starting from scratch.

The platform implements your funding strategy. The services produce it.

---

## The Problem

- Funding programs are scattered across forums, Notion pages, forms, and spreadsheets — no unified lifecycle from program intent → applications → approvals → outcomes
- Funders and reviewers drown in proposals evaluated against ad-hoc criteria, making decisions slow, inconsistent, and hard to compare across rounds
- Ecosystems publish spend data but rarely have structured outcome data (TVL, users, infra readiness), so they can't tell which programs or tracks are actually working
- Data about rounds and funded projects is scattered — ecosystems can't see, compare, or iterate on what their different programs actually produce over time

---

## What FlowOS Does

- Define program intent — goals, tracks, eligibility — in a clear, reusable schema that drives everything downstream
- Run AI-powered intake that pre-filters and labels every application — Pass / Needs Revision / Not a Fit — before human review
- Review with consistent rubrics instead of ad-hoc criteria, with AI pre-scores already surfaced for every Pass application
- Keep a registry of programs, rounds, and funded projects with pre-defined impact metrics, so ecosystems can see how each program performs over time — without turning into heavy project management software

---

## Who It's For

**Funding Program Operators**
Running grants, bounties, builder incentives, or any structured non-dilutive program. FlowOS replaces the Notion and spreadsheet stack with a system where program intent drives intake, review, and record-keeping. For small teams managing high volume, it's the difference between drowning and having a process that scales.

**Ecosystem Growth Leads**
Responsible for where non-dilutive capital goes. Right now there's no clean way to compare what different programs and tracks actually delivered across rounds. FlowOS gives a program-level view of outcomes linked to spend.

**Protocol Treasuries**
Accountable for spend reporting to governance or token holders. FlowOS links spend to structured outcomes defined before applications open — not just a record of who received funding, but what it produced.

---

## Platform Features

**Program Intent Builder**
Define program goals, eligibility, tracks, and KPIs in a structured form before any applications open. This config drives the application form, the AI agent, the rubric, and the registry — one source of truth for the whole program.

**Structured Application Forms**
Vertical-specific templates (DeFi / Protocols, Consumer Apps / Wallets) that load from the program config. A short pre-screening confirms fit before the full form loads.

**AI-Assisted Pre-Filtering**
Every application is evaluated against program intent before human review — Pass / Needs Revision / Not a Fit, with pre-scores per rubric criterion, strengths, risks, and a plain-language summary. Needs Revision applications receive specific feedback to resubmit. Human reviewers make every final decision.

**Review Queue**
All Pass applications enter a structured queue with the AI evaluation already surfaced. Reviewers score using the same rubric every time — consistent and comparable across rounds.

**Funding Registry**
Approved projects are automatically added to a registry with the KPI fields defined at the program level. A structured record of what each program funded and what it produced, comparable across rounds and tracks.

---

## Services

The platform operationalises your funding strategy. The services help you build it.

| Service | What it is | When |
|---|---|---|
| Program Design | Define program goals, tracks, eligibility, rubric, and KPIs — produces the intent config that drives FlowOS | Available now |
| Program Assessment | Audit an existing program — where is the Design → Fund → Assess loop broken and what needs to change | Available now |
| Round Strategy | Define what to fund in a specific round — tracks, budget split, outcome targets | Available now |
| Impact Reporting | Structured report after a round closes — what the capital produced, what to change next round | Coming |
| Cross-Program Benchmarking | Compare outcomes across programs or chains | Coming |
| Reviewer Calibration | Reduce scoring variance across distributed review teams | Coming |

---

## Built for Crypto Ecosystems

- Permissionless applications mean anyone can apply with no prior relationship — structured intake is essential at scale
- Small teams managing high volume need the process to do more of the work
- Decentralised review committees need a shared evaluation framework to make consistent decisions
- On-chain data means outcome verification can eventually be pulled directly, not self-reported
- Funded project reputation is public and portable — the registry is built to surface track record as part of future evaluation

---

## Current Status

Working prototype with all core screens built. Forms validated against real grant program data. AI screening pipeline runs on test data with mocked outputs — next milestone wires it to a live AI model with structured JSON output.

Grant funding supports building the live AI integration and completing the registry layer.
