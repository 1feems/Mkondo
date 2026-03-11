# FlowOS — Customer Validation (Idea Stage)

Documents early validation work done before operator interviews.

---

## Problem

Ecosystem grant programs have no structured way to define program intent before intake opens, no consistent evaluation process, and no record of what funded projects produced. Each round is rebuilt from scratch. Performance is invisible. Reviewers work from different standards.

This was observed across multiple ecosystems — Gitcoin, Arbitrum, POKT, Polygon — through direct experience as a funder, operator, reviewer, researcher, and grantee.

---

## Method

Document testing and structured walkthrough against a live grant program.

No operator interviews conducted yet — planned as next validation step. This stage was designed to answer: does the problem exist in a real program, and is the FlowOS solution directionally right?

---

## What Was Tested

**Program:** Stacks Endowment Builder Grant and Getting Started Grant

**Assets used:**
- Stacks Endowment eligibility and evaluation guide (published)
- Stacks Builder Grant rubric and evaluation criteria (published)
- Live Stacks grant application form (Getting Started and Builder tracks)
- BNS One — an accepted Stacks application (SIP-31 #31, public GitHub record)

**What was put through the test:**
- Form 1 (Program Info) — mapped against Stacks program-level configuration
- Form 2 (Round Intent) — mapped against Stacks round-level setup
- Pre-Screening — mapped against Stacks eligibility gate
- Rubric — compared directly against Stacks evaluation criteria
- Application Form — BNS One application used to walk through the form as a real submission

---

## Findings

**What held up:**

| Element | Finding |
|---|---|
| Rubric | FlowOS's 6 criteria match Stacks exactly — same names, same 0–5 scale. No modification needed |
| Pre-screening | Three questions map cleanly to Stacks eligibility requirements |
| Form structure | Fields captured what reviewers need to assess strategic alignment, feasibility, ecosystem impact, and budget |
| Registry KPI fields | Aligned with the outcome metrics Stacks tracks post-approval |

**Gaps identified:**

| Gap | What Stacks requires | Not yet in FlowOS |
|---|---|---|
| Milestone disbursement structure | Defined tranches tied to milestone completion | No field for operators to define payment stages |
| KYC/KYB compliance field | Willingness confirmed at intake before application proceeds | Not in pre-screening |
| Reporting cadence | Regular check-ins with program manager post-approval | No field to define expected reporting frequency |
| What We Don't Fund | Explicitly listed exclusions surfaced before applicants apply | No parallel field in program config |
| Outcome Focus | Programs fund across both user and ecosystem outcomes | Form 1 is single-select |
| Ecosystem fit question | Why is this project building on this specific chain? | No dedicated ecosystem alignment field |
| Long-term commitment | Commitment horizon captured at intake | Not captured |
| Sustainability plan | Post-grant maintenance plan | Not captured |

---

## Conclusion

The problem exists in a live, active program. The core FlowOS solution — structured intent before intake, consistent rubric, pre-screening gate, funded project registry — maps directly to what Stacks needs and currently lacks.

The rubric matching without modification is a strong directional signal. The gaps found are structural gaps in how grant programs currently capture and communicate intent — not FlowOS design errors. They represent the next iteration of the form design.

---

## Next Steps

- Operator interviews — 3–5 grant program operators across different ecosystems
- Reviewer interviews — how reviewers currently evaluate and what needs to be surfaced
- Second ecosystem test — repeat document testing against a second live program

---

*Validated against: Stacks Endowment (stacksendowment.co). Reference application: BNS One (github.com/stacksgov/sip31-interim-grants/issues/31).*
