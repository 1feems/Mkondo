# FlowOS — Forms Specification

Field reference for all operator and applicant forms.

---

## Forms Index

### Operator Forms

| # | Form | Who fills it | When |
|---|---|---|---|
| 1 | Program Info | Operator | Once per program |
| 2 | Program Round Intent | Operator | Each funding cycle |
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

Sets the permanent identity of a grant program. Created once by the operator. Applies to all rounds under this program.

| Field | Type | Required |
|---|---|---|
| Program Name | Text | Yes |
| Ecosystem / Chain | Text | Yes |
| Program Description | Long Text | Yes |
| Funding Type | Static | Yes |
| Mechanism | Dropdown | Yes |
| Outcome Focus | Dropdown | Yes |
| Area of Focus | Checkbox group | Yes |
| Vertical | Dropdown | Yes |
| Eligibility Criterion 1 | Text | Yes |
| Eligibility Criterion 2 | Text | Yes |
| Eligibility Criterion 3 | Text | Yes |
| Eligibility Criterion 4 | Text | Optional |
| Eligibility Criterion 5 | Text | Optional |
| Expected Deliverables | Long Text | Yes |
| Rubric | Dropdown | Yes |
| Program Lead / Contact | Text | Yes |
| Primary Impact Goal | Text | Optional |

---

## Form 2 — Program Round Intent

Filled each funding cycle. Pre-filled fields carry over from Program Info automatically.

| Field | Type | Required |
|---|---|---|
| Program Name | Pre-filled | — |
| Program Description | Pre-filled | — |
| Vertical | Pre-filled | — |
| Outcome Focus | Pre-filled | — |
| Area of Focus | Pre-filled | — |
| Eligibility | Pre-filled | — |
| Funding Round ID | Text | Yes |
| Grant Type | Dropdown | Yes |
| Round Start Date | Date picker | Yes |
| Round End Date | Date picker | Yes |
| Total Budget (Token) | Number | Yes |
| Total Budget (USD) | Number | Optional |
| Area of Focus (this round) | Checkbox group | Yes |
| Target Applicants | Short Text | Yes |
| Project Type 1 | Editable text | Optional |
| Project Type 2 | Editable text | Optional |
| Project Type 3 | Editable text | Optional |
| Impact Metric 1 | Text | Yes |
| Impact Metric 2 | Text | Optional |
| Impact Metric 3 | Text | Optional |

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

Shown before the full application loads. All options auto-populated from the operator's program setup. Applicant must complete all sections to continue.

| Field | Type | Required | Pulls From |
|---|---|---|---|
| What type of project are you building? | Dropdown | Yes | Form 1 — Vertical |
| Which outcome does your project primarily target? | Dropdown | Yes | Form 1 — Area of Focus |
| Do you meet the following requirements? | Checklist — must check all | Yes | Form 1 — Eligibility Criteria |

---

## Form 6 — Application Form — DeFi / Protocols

*(To be completed)*

---

## Form 7 — Application Form — Consumer Apps / Wallets

*(To be completed)*
