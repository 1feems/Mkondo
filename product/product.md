# FlowOS — Product Overview

---

## What It Is

FlowOS is a funding coordination platform for Web3 ecosystems. It gives grant operators a structured way to design programs, screen and review applications consistently, and maintain a registry that links spend to outcomes — so ecosystems can see what their capital actually produced and improve each round instead of starting from scratch.

Today, most grant programs are run in Notion, spreadsheets, and forms, with criteria scattered across docs and reviewers working from different mental models. FlowOS turns program intent and eligibility into structured configurations that everything downstream reads from — the application form, the AI agent, the rubric, and the registry.

---

## The Problem

Foundations, DAOs, L2s, and treasuries running non-dilutive funding programs are drowning in fragmented tools, inconsistent reviews, and no clean way to see what their funding actually produced across rounds. This is happening exactly as grant volume, incentive programs, and scrutiny over impact are all sharply increasing.

**No unified lifecycle**
Funding programs are scattered across forums, Notion pages, forms, and spreadsheets. There is no clear path from program intent → applications → approvals → outcomes. Every round is rebuilt from scratch.

**Inconsistent review**
Funders and reviewers work through large volumes of proposals evaluated against ad-hoc criteria. Decisions are slow, inconsistent, and hard to compare across rounds or programs.

**No outcome visibility**
Ecosystems publish spend data but rarely have structured outcome data — TVL, users, infrastructure readiness. They can't tell which programs or tracks are actually working or which investments delivered.

**No program-level learning**
Data about rounds and funded projects is scattered across tools. Ecosystems can't see, compare, or iterate on what their different programs produce over time. Every round is an island.

---

## What FlowOS Does

**Before applications open**, the operator fills out two forms: one that defines the program (goals, eligibility, vertical, outcome focus, rubric) and one that sets the specifics for the current round (budget, dates, target applicants, impact metrics). Everything else — the application form, the AI agent, the registry — reads from these two configs.

**When applications come in**, an AI agent reads each submission against the program intent and returns a structured triage result:

- **Pass** — meets eligibility, aligns with round goals, moves to the human review queue
- **Needs Revision** — eligible but incomplete or misaligned — applicant receives specific, actionable feedback and can resubmit
- **Not a Fit** — fails eligibility or fundamentally misaligned — recorded with reasons for program learning, doesn't enter the queue

**During review**, operators and reviewers see every Pass application with the AI's pre-scores and rationale already surfaced — scored against each rubric criterion, with strengths, risks, and a plain-language summary. Human judgment makes every final decision.

**After approval**, the funded project is automatically added to the registry with the KPI fields defined at the program level. Over time the registry becomes a structured record of what each program funded and what it produced — comparable across rounds and tracks.

---

## Who Uses It

**Grant operators** — run the program day to day. FlowOS handles first-pass screening so they spend their time on applications that actually belong in the review queue.

**Ecosystem and growth leads** — decide where non-dilutive capital goes. FlowOS gives them a program-level view of what different rounds and tracks are producing, so allocation decisions are based on structured outcome data, not intuition.

**Foundations and governance committees** — accountable for impact. FlowOS gives them structured outcome data linked to spend, not just a list of who received funding.

**Builders and applicants** — submit through a public link, no account needed. If their application needs work, they receive specific feedback on what to fix rather than a generic rejection.

---

## What Makes It Different

**Intent drives everything.** The Program Intent Form is filled once per round. It defines goals, eligibility, target applicants, and KPIs. That config drives the application form template, the agent's evaluation lens, the rubric, and the registry's outcome fields. There is no manual re-entry between steps and no gap between what the program says it funds and what it actually evaluates.

**The registry closes the loop.** Most platforms handle intake. FlowOS also captures what programs produce. Funded projects are stored with operator-defined KPI fields. Over time this creates a comparable record of outcomes across rounds — turning a grant program into a learning system.

**The AI sits on the program side, not the applicant side.** Other platforms add AI to help applicants polish their submissions before they hit the queue. FlowOS's agent is program-aware triage — it reads the program intent plus the application and returns Pass / Needs Revision / Not a Fit relative to what *this round* is trying to fund. The output is framed in terms of fit, not generic quality.

**Intent-aware, not generic.** The agent is explicitly conditioned on a structured program config — goal focus, eligibility, target applicants, round scope. Its pre-scores and summary are framed in terms of fit for this round, not abstract completeness. This means reviewer time goes to Pass applications that are actually in scope, not applications that look good but don't match the program.

---

## Why Now

Grant volume, incentive programs, and scrutiny over impact are all increasing at the same time. The manual process that worked when programs received 20 applications per round is breaking at 100. The ecosystems that build structured, AI-assisted review now will be able to deploy more capital, more accurately, with less overhead — and will have the outcome data to prove it.

---

## Current Status

Working prototype with all core screens built. Forms validated against real grant program data. The AI screening pipeline runs on test data with mocked outputs — the next milestone wires it to a live AI model with structured JSON output.

Grant funding supports building the live AI integration and completing the registry layer.

---

## What FlowOS Does Not Do

FlowOS does not process payments, track milestones post-funding, or replace human reviewers. It handles the coordination layer — structured program design, consistent intake, AI-assisted triage, and outcome record-keeping — so the humans in the process can focus on the decisions that require judgment.
