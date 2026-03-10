# FlowOS — Forms Specification

Field reference for Figma design and development. Updated as each form is completed.

---

## Forms Index

| # | Form | Who fills it | When |
|---|---|---|---|
| 1 | Program Info | Operator | Once per program |
| 2 | Program Round | Operator | Each funding cycle |
| 3 | Program Intent | Operator | Each funding cycle |
| 4 | Application Form — DeFi / Protocols | Builder (public) | Per submission |
| 5 | Application Form — Consumer Apps / Wallets | Builder (public) | Per submission |
| 6 | Rubric — User Outcome | Operator | Once per program or round |
| 7 | Rubric — Ecosystem Outcome | Operator | Once per program or round |

---

## Form 1 — Program Info (General)

**Purpose:** This form sets the identity of your grant program. Filled once and applies to all rounds. Appears in the registry and on your public application page.

| Field Label | Field Type | Required | Description / Guide |
|---|---|---|---|
| Program Name | Text | Yes | Give your program a unique name. e.g. Stacks Builder Grant |
| Ecosystem / Chain | Text | Yes | Which blockchain ecosystem does this program support? e.g. Stacks, Optimism, Near |
| Program Description | Long Text | Yes | What is this program trying to achieve? Describe the gap or opportunity it addresses |
| Funding Type | Static | Yes | Grant Program |
| Mechanism | Dropdown | Yes | How funding is distributed. Options: Grant |
| Program Focus | Checkbox group | Yes | Select all that apply — User Outcomes: Acquisition, Retention, Activation, Reactivation / Ecosystem Outcomes: Security, Infrastructure, Interoperability, Developer Tools, Ecosystem Growth |
| Vertical | Dropdown | Yes | Select the vertical this program supports. Determines the application form template used for all rounds. Options: DeFi / Protocols, Consumer Apps / Wallets |
| Eligibility Criteria | Grouped section | Yes | Define the conditions a project must meet to qualify |
| ↳ Criterion 1 | Text input | Yes | e.g. Project must be live and deployed on supported chain |
| ↳ Criterion 2 | Text input | Yes | e.g. Minimum 3 months of demonstrable user activity or traction |
| ↳ Criterion 3 | Text input | Yes | e.g. No major security incidents in the last 6 months |
| ↳ + Add criterion | Repeater | Optional | Up to 2 additional criteria |
| Expected Deliverables | Long Text | Yes | What outputs do you expect from funded projects? e.g. integrations, tooling, user campaigns |
| Rubric | Dropdown | Yes | Select the rubric for this program. Options: User Outcome Rubric |
| Program Lead / Contact | Text | Yes | Who is the internal owner or point of contact for this program? |
| Primary Impact Goal | Text | Optional | What is the single most important outcome this program is working toward? e.g. Grow active users via high-usage integrations |

---

*Forms 2–7 will be added as each is completed.*
