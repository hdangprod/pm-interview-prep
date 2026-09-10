# Katalon case bank

All cases are coach-created simulations, not actual Katalon metrics, incidents, or leaked questions.
No cases completed or failed. Ask one prompt at a time; do not reveal a model answer before an attempt.

## K-D01 — Highest-information opening diagnostic

Status: ATTEMPTED; first answer evaluated, follow-up K-D01-F1 pending. Target: about 2 minutes in English; no prepared framework needed.

Prompt:
“You are a PM intern at Katalon. In a hypothetical pilot, QA engineers try an AI feature that generates test cases, but many do not use it again. Engineering proposes making the agent more autonomous. Your PM asks you to recommend what the team should do next. How would you approach this?”

Observe only demonstrated dimensions: problem decomposition, customer discovery, metrics, prioritization, AI judgment, communication and English. Technical depth remains UNKNOWN unless shown.
After answer, challenge the most consequential unsupported assumption. Save all follow-ups and revisions with distinct IDs. Do not pre-assign an answer-dependent challenge.
Exit: candidate gives an evidence-led next step and handles a contrary signal without inventing facts. Final baseline can still be low; exit is not a pass.

## Remaining prioritized queue

| ID | Scenario | Purpose | Status |
| --- | --- | --- | --- |
| K-C02 | Enterprise customer requests unattended changes to test assets and execution | Autonomy, permissions, risk, reversibility, evaluation | PLANNED |
| K-C03 | Generated tests execute successfully but miss important defects | Quality definition, assertions, evaluation set, QA reasoning | PLANNED |
| K-C04 | Two customers describe conflicting needs in failure diagnosis | Discovery, segmentation, scope, testable specification | PLANNED |
| K-C05 | Team can use Playwright agents; assess the value of an integrated testing product | Alternatives, workflow value, prioritization | OPTIONAL |
| K-M01 | Final onsite simulation, sequential PM and Director probing | All critical gates, behavioral evidence, pressure | PLANNED Sep 15 |

Each attempt record: date, raw answer ID, clarification facts supplied, probes, scores/rationale, assistance level, KEEP/FIX, retry, transfer result, status (attempted/completed/failed/retest).


## K-D01 attempt history

2026-09-10: A1 preserved in ../sessions/2026-09-10-K-D01-A1.raw.txt; evaluation in ../sessions/2026-09-10-K-D01-feedback.md. Required-dimension scores: discovery 8, decomposition 8, agent judgment 7, evaluation 6, communication 8, typed English 8. Supplemental metrics 6, prioritization 6. No in-session assistance before A1. Case remains in progress, neither passed nor failed.

### K-D01-F1 — pending

New hypothetical evidence: 95% of generated tests run successfully, but 70% are edited before use. In six user interviews, most edits appear to adapt tests to project conventions. For comparable tasks, observed total generation-and-review time is about 20 minutes, versus 25 minutes manually. Engineering argues that removing review will unlock the benefit. You have one engineer for one week. What would you test next, and what result would make you change direction?

Target: approximately 90 seconds. New synthetic evidence; no preferred answer supplied. Assess choice, interpretation and an actionable success/change criterion.
