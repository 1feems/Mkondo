# FlowOS — Forms Specification

Technical reference for agent screening, application intake, and program configuration. Each field is described with its type, purpose, and how it is used by the agent.

---

## Forms Index

| # | Form | Who fills it | When |
|---|---|---|---|
| 1 | Program Info | Operator | Once per program |
| 2 | Program Intent | Operator | Each funding cycle |
| 3 | Application Form — DeFi / Protocols | Builder (public) | Per submission |
| 4 | Application Form — Consumer Apps / Wallets | Builder (public) | Per submission |
| 5 | Rubric — User Outcome | Operator | Once per program or round |
| 6 | Rubric — Ecosystem Outcome | Operator | Once per program or round |

---

## Form 1 — Program Info

Sets the permanent identity of a grant program. Created once by the operator. All fields are passed to the agent as program-level context when screening applications.

| Field | Type | Required | Agent Use |
|---|---|---|---|
| Program Name | Text | Yes | Program identity label in all agent outputs |
| Ecosystem / Chain | Text | Yes | Agent uses to assess ecosystem alignment of submitted projects |
| Program Description | Long Text | Yes | Agent reads to understand program purpose and gap being addressed |
| Funding Type | Static | Yes | Context — always Grant in v1 |
| Mechanism | Dropdown | Yes | Context — always Grant in v1. Options: Grant |
| Program Focus | Checkbox group | Yes | Agent uses selected outcomes to assess whether submitted project targets the right outcome category. User Outcomes: Acquisition, Retention, Activation, Reactivation. Ecosystem Outcomes: Security, Infrastructure, Interoperability, Developer Tools, Ecosystem Growth |
| Vertical | Dropdown | Yes | Determines which application form template is used. Signals to agent which vertical the program targets. Options: DeFi / Protocols, Consumer Apps / Wallets |
| Eligibility Criterion 1 | Text | Yes | Agent checks submitted application against each criterion independently to determine eligible: true / false |
| Eligibility Criterion 2 | Text | Yes | Agent checks submitted application against each criterion independently to determine eligible: true / false |
| Eligibility Criterion 3 | Text | Yes | Agent checks submitted application against each criterion independently to determine eligible: true / false |
| Eligibility Criterion 4 | Text | Optional | Additional eligibility check if needed |
| Eligibility Criterion 5 | Text | Optional | Additional eligibility check if needed |
| Expected Deliverables | Long Text | Yes | Agent uses to assess whether proposed project deliverables match program expectations |
| Rubric | Dropdown | Yes | Selects which rubric the agent scores against. Options: User Outcome Rubric, Ecosystem Outcome Rubric |
| Program Lead / Contact | Text | Yes | Internal metadata — not passed to agent |
| Primary Impact Goal | Text | Optional | Agent uses as top-level intent signal when assessing intent_alignment |

---

*Forms 2–6 will be added as each is completed.*
