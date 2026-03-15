
# Mkondo — Build: Current State

## Purpose

This page shows what is already built in Mkondo, what currently works, and what is still mocked or planned next.

---

## What Is Built

- Program Info form
- Eligibility form
- Round Intent form
- Application Builder
- Consumer Apps / Wallets template
- DeFi / Protocols template
- Rubric builder
- Review page
- Application detail view
- AI evaluation view
- Program profile view
- Registry prototype views

---

## What Works Today

- Operators can configure a program and round
- Application templates can be created for two verticals
- Rubric criteria and scoring can be structured in the product
- Completed applications can move through a review flow
- AI evaluation outputs are surfaced in the review experience
- Program and registry views show the intended coordination layer

---

## Technical Work Completed

- Frontend prototype built in Next.js
- Multi-step operator workflow implemented across program setup, round setup, application, rubric, and review
- Structured application templates built for Consumer Apps / Wallets and DeFi / Protocols
- Review flow implemented with rubric criteria, scoring, and AI evaluation surfaces
- Registry prototype views built to show how funded project and program data can be tracked

---

## Agent Design and Logic

- Agent flow designed to evaluate applications against program intent, eligibility, and rubric criteria
- Structured output format defined for triage label, scores, strengths, risks, and summary
- Current build uses mocked outputs to demonstrate review workflow and decision support
- Live model integration is the next implementation step

---

## Validation Completed

- Program setup tested against the Stacks Builder Grant structure
- Consumer template tested against a real approved Stacks application
- DeFi template and rubric built from live grant structures
- Review flow aligned to a real six-criteria scoring model

---

## Mocked vs Functional

### Functional

- Core page flows
- Program setup
- Round setup
- Application templates
- Rubric setup
- Review surfaces
- Program profile
- Registry prototype

### Mocked

- AI scoring outputs
- Live application intake infrastructure
- Full backend persistence
- Registry automation on approval

---

## Current Demo Flow

1. Program Info
2. Eligibility
3. Round Intent
4. Application
5. Rubric
6. Review
7. Application Detail
8. AI Evaluation

---

## Next

- Replace mocked AI outputs with live model integration
- Connect application intake to persistent backend records
- Expand registry linkage across approved applications
- Add additional vertical templates
