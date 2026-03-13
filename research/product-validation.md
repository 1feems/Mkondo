# FlowOS — Product Validation

**Purpose:** To test if the pages and forms built align with current process and assets used by live grant programs. This stage was designed to answer: do the forms work as intended for the people running real programs, and does the output map to what real applicants submit?

---

## Method

Document testing and structured walkthrough against live grant programs and approved applications.

No operator interviews conducted yet — planned as next validation step. This stage was designed to answer: do the forms and pages built reflect how real grant programs operate, and is the FlowOS solution directionally right?

---

## Programs Tested Against

- **Stacks Endowment — Builder Grant Program** ([stacksendowment.co/grants-docs/builder-grant-program-track](https://stacksendowment.co/grants-docs/builder-grant-program-track))
- **Optimism — Growth Grants Season 9** ([opgrants.io/seasons/current/season-9](https://www.opgrants.io/seasons/current/season-9/))

---

## What Was Tested

**Program Info Form** — mapped against Stacks and Optimism program-level setup: ecosystem identity, eligibility criteria, outcome focus, vertical, and expected deliverables

**Round Intent Form** — mapped against Stacks and Optimism round-level setup: grant type, budget, target applicants, project types in scope, and success metrics

**Pre-Screening** — mapped against Stacks eligibility requirements: three questions tested against the gate criteria a real program uses before intake

**Rubric** — compared directly against Stacks evaluation criteria and scoring scale

**Application Form — Consumer Apps / Wallets template**
- Tested against BNS One — approved Stacks SIP-31 interim grant ($30,000) ([SIP-31 #31](https://github.com/stacksgov/sip31-interim-grants/issues/31))
- Also tested against Optimism Audit Grant — approved OP application ([APP-4OH1CJ5K-B8DQF7](https://app.opgrants.io/applications/APP-4OH1CJ5K-B8DQF7))

**Application Form — DeFi / Protocols template**
- Tested against Lido — approved Optimism Growth Grant Season 8, 200,000 OP ([APP-ADR4SDTF-LR8N60](https://app.opgrants.io/applications/APP-ADR4SDTF-LR8N60))

---

## Findings

**What held up:**

| Element | Finding |
|---|---|
| Program Info Form | Fields map to how both Stacks and Optimism define a program — ecosystem identity, vertical, eligibility, and outcome focus captured without gaps |
| Round Intent Form | Round-level setup aligns with how both programs structure a funding round — budget, target applicants, success metrics |
| Rubric | FlowOS's 6 criteria match Stacks exactly — same names, same 0–5 scale. No modification needed |
| Pre-screening | Three questions map cleanly to Stacks eligibility requirements and outcome focus |
| Consumer template fields | MAU, total unique users, and retention rate match the traction metrics BNS One reported (750-800 MAU, 6,500+ unique users, 68% engagement) — confirmed across two programs |
| DeFi template fields | TVL, DAU/MAW, and 30-day transaction volume map to on-chain metrics Lido reported (~$408M TVL) — agent-verifiable via DefiLlama |
| Milestone table | Milestone + target date + deliverable structure matches how both Stacks and OP structure grant disbursement |
| Grant use breakdown | Category + amount table maps to how applicants break down budget across both programs |

---

## Next Steps

- Operator interviews — 3–5 grant program operators across different ecosystems
- Reviewer interviews — how do reviewers currently evaluate, what do they need surfaced
- Applicant perspective — friction points in the current application experience
- Expand vertical templates — Infrastructure / Tooling as the next template to build and test
- Agent outcome testing — pre-screening scores, on-chain verification, and impact tracking against submitted applications

---

*Product validation conducted against: Stacks Endowment Builder Grant program track and approved BNS One application (SIP-31 #31). Optimism Growth Grant program (Season 9), approved Lido application (APP-ADR4SDTF-LR8N60, Season 8), and approved OP Audit Grant application (APP-4OH1CJ5K-B8DQF7).*
