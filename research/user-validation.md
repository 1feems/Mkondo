# FlowOS — Product Testing

**Purpose:** Product testing — not customer validation. FlowOS forms were mapped against live grant programs and real approved applications to confirm the product works as intended for the people running it. This documents what was tested and what it confirmed.

---

## Programs Tested Against

### Stacks Endowment — Builder Grant Program
- **Program Info Form** — mapped against the Stacks Builder Grant program track: ecosystem identity, eligibility criteria, outcome focus, vertical, and expected deliverables
- **Round Intent Form** — mapped against Stacks round-level setup: grant type, budget, target applicants, project types in scope, and success metrics
- **Pre-Screening** — three questions map cleanly to Stacks eligibility requirements and outcome focus
- **Rubric** — six criteria match Stacks exactly — same names, same 0–5 scale
- **Reference:** [Stacks Builder Grant Program Track](https://stacksendowment.co/grants-docs/builder-grant-program-track)

### Optimism — Growth Grants Season 9
- **Program Info Form** — mapped against OP Growth Grant program-level setup: ecosystem identity, eligibility, vertical focus, and outcome metrics
- **Round Intent Form** — mapped against OP round-level setup: grant type, budget, target applicants, success metrics
- **Reference:** [OP Grants Season 9](https://www.opgrants.io/seasons/current/season-9/)

---

## Application Templates Tested

### Consumer Apps / Wallets template
**Tested against:** BNS One — approved Stacks SIP-31 interim grant ($30,000)
- Base fields map cleanly to what was submitted
- Grant use breakdown maps to their milestone budget structure
- Milestones table maps to their 3-milestone roadmap (description + date + deliverable)
- Consumer-specific numeric fields (MAU, total unique users, retention rate) match the traction metrics BNS One reported: 750-800 MAU, 6,500+ unique users, 68% engagement rate
- **Reference:** [SIP-31 #31 — BNS One](https://github.com/stacksgov/sip31-interim-grants/issues/31)

**Also tested against:** Optimism Audit Grant — approved OP application (APP-4OH1CJ5K-B8DQF7)
- Form structure and consumer-specific fields confirmed against a second approved application in the vertical across a different program
- **Reference:** [APP-4OH1CJ5K-B8DQF7 — OP Audit Grant](https://app.opgrants.io/applications/APP-4OH1CJ5K-B8DQF7)

### DeFi / Protocols template
**Tested against:** Lido — approved Optimism Growth Grant Season 8 (200,000 OP)
- Base fields, grant use breakdown, and milestones all map to what was submitted and approved
- DeFi-specific numeric fields (TVL, DAU/MAW, 30-day transaction volume) map to the on-chain metrics Lido reported: ~$408M TVL across 7 Superchain deployments
- Milestone table maps to their 2-milestone structure with TVL targets and target dates
- **Reference:** [APP-ADR4SDTF-LR8N60 — Lido](https://app.opgrants.io/applications/APP-ADR4SDTF-LR8N60)

---

## What Validated

- Program Info and Round Intent forms cover what both Stacks and Optimism require to define a program and open a round
- Rubric criteria and scoring scale matched Stacks without modification
- Pre-screening maps cleanly to Stacks eligibility requirements
- Consumer template fields align with the traction metrics consumer/wallet grant applicants actually report
- DeFi template fields align with the on-chain metrics DeFi protocol applicants report and that agents can verify via DefiLlama and on-chain data
- Milestone table structure (milestone + target date + deliverable) matches how both Stacks and OP structure grant disbursement

---

## Where FlowOS Fits

**Grant Operators** — the team running the program day to day

| Step | FlowOS |
|---|---|
| Define what the program funds | Program setup forms — eligibility, rubric, outcome focus, and grant scope defined once and applied every round |
| Open a new round | Round setup — budget, who the round is for, and how success is measured |
| Receive applications | AI screening labels every submission before a reviewer sees it — Pass / Needs Revision / Not a Fit |
| Run review | Every application arrives with rubric scores already surfaced — reviewers work from the same criteria every round |

**Treasury Committee** — meets quarterly to review what the grant program produced and approve strategy and budgets

| Step | FlowOS |
|---|---|
| Quarterly review calls | The registry gives the committee a structured record per round — funded projects, outcome metrics, and what each round produced — ready to pull from before every call |
| Budget approvals | Program setup creates a record of what each program is designed to fund, at what cost, and against what metrics — decisions are grounded in structured data, not recall |

---

## Next Steps

- Operator interviews — 3–5 grant program operators across different ecosystems
- Reviewer interviews — how do reviewers currently evaluate, what do they need surfaced
- Applicant perspective — friction points in the current application experience
- Consumer Apps / Wallets template — test against a second approved application in this vertical
- Expand vertical templates — Infrastructure / Tooling as the next template to build and test

---

*Product testing conducted against: Stacks Endowment Builder Grant program track and approved BNS One application (SIP-31 #31). Optimism Growth Grant program (Season 9) and approved Lido application (APP-ADR4SDTF-LR8N60, Season 8).*
