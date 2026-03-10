# FlowOS — Forms Specification

Technical reference for agent screening, application intake, and program configuration. Each field is described with its type, purpose, and how it is used by the agent.

---

## Forms Index

### Operator Forms
| # | Form | Who fills it | When |
|---|---|---|---|
| 1 | Program Info | Operator | Once per program |
| 2 | Program Intent | Operator | Each funding cycle |
| 3 | Rubric — User Outcome | Operator | Once per program or round |
| 4 | Rubric — Ecosystem Outcome | Operator | Once per program or round |

### Applicant Forms (Public — no login required)
| # | Form | Who fills it | When |
|---|---|---|---|
| 5 | Pre-Screening | Applicant | Before application loads |
| 6 | Application Form — DeFi / Protocols | Applicant | Per submission |
| 7 | Application Form — Consumer Apps / Wallets | Applicant | Per submission |

---

## OPERATOR FORMS

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
| Program Focus | Checkbox group | Yes | Agent uses selected outcomes to assess whether submitted project targets the right outcome category. User Outcomes: Acquisition, Retention, Activation. Ecosystem Outcomes: Security, Infrastructure, Interoperability, Developer Tools, Ecosystem Growth |
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

## Form 2 — Program Intent

*(To be completed)*

---

## Form 3 — Rubric — User Outcome

*(To be completed)*

---

## Form 4 — Rubric — Ecosystem Outcome

*(To be completed)*

---

## APPLICANT FORMS (Public)

---

## Form 5 — Pre-Screening

Shown to applicants before the full application loads at /apply/[round-id]. All fields are pulled automatically from operator forms — no manual setup required per round. Applicant must complete all 3 sections to continue to the application.

| Field | Type | Required | Pulls From | Agent Use |
|---|---|---|---|---|
| What type of project are you building? | Dropdown | Yes | Form 1 — Vertical | Agent uses selection for vertical context and to load correct application form template |
| Which outcome does your project primarily target? | Dropdown | Yes | Form 1 — Program Focus | Agent uses as first intent_alignment signal before reading full application. Options: Acquisition, Retention, Activation |
| Do you meet the following requirements? | Checklist (must check all) | Yes | Form 1 — Eligibility Criteria (Criterion 1, 2, 3) | Agent reads confirmed checks to set eligible: true. Any unchecked = eligible: false |

---

## Form 6 — Application Form — DeFi / Protocols

*(To be completed)*

---

## Form 7 — Application Form — Consumer Apps / Wallets

*(To be completed)*
