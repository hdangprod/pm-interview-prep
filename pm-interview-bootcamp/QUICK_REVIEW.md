# Quick review — before the interview

[Home](README.md) · [Roadmap](ROADMAP.md) · [English phrases](english/phrase-bank.md)

Use 10–15 minutes: read the reflexes, then explain one example from each track aloud. No need to read every linked note. With only two minutes, read the lines under each heading.

## Katalon product reflex

**User → Workflow → Friction → Evidence → Hypothesis → Validation → Solution → Metric**

- Which tester, doing which job, in which project?
- What happens today, including workarounds and review?
- Is the request the real need? What would disprove my interpretation?
- What is the smallest useful test of the riskiest assumption?
- What counts as a useful outcome, compared with the current workflow?

A PM interviewer may probe workflow and requirements. A Director may probe why this problem deserves resources. These are preparation inferences, not a published rubric.

If stuck: “I’d first clarify who has this problem and what happened the last time.”

## AI product reflex

**Why AI? Why an agent? What must stay under human control?**

- Does the task need language or judgment, or would rules work?
- Does it need to choose its next action, or is the sequence predictable?
- What context is required? Is it current, relevant and permitted?
- What can go wrong, and what is the cost of being wrong?
- Can we verify the result? Can we reverse the action?
- What can run automatically? What needs a concrete approval?
- What happens on timeout, partial completion or repeated failure?
- Does the feature improve the user's job after review, retries, cost and waiting?

**MCP recall:** AI application (host) → client connection → server exposing tools/context → underlying system. MCP helps systems connect; permission and judgment still need explicit design.

**Evaluation recall:** compare representative tasks against a baseline; inspect correctness and useful outcomes; include failure cases; monitor after release.

More autonomy is a design choice. It must earn its place.

## Testing judgment reflex

**Requirement → design → create → execute → diagnose → fix → regression → release**

- A test that runs is not necessarily a meaningful test.
- A passing test may have a weak or missing assertion.
- A failed test may correctly expose a product defect.
- Editing may be useful customization, not an error.
- A flaky test can damage trust in the whole test suite.
- Fix the right thing: application, test, data or environment.
- Review coverage against important risks; a percentage alone is insufficient.

Measure time to a **useful, verified test**, including correction and review. Check important defects caught and false alarms.

## ShopeeFood marketplace reflex

**What changed? → When? → Where? → Which segment?**

Define the metric and denominator before explaining the movement. Check instrumentation, comparable periods and recent changes.

**Buyer:** traffic, price, selection, conversion, repeat use, reliability.

**Merchant:** open/available, accepts orders, prepares on time, earns enough, has capacity.

**Driver:** available nearby, accepts, waits, travels, earns enough.

**Platform:** completed orders, sustainable economics, service reliability.

Then: **hypothesis → evidence → intervention → trade-off → first-order effect → second-order effect**.

Example possibility: promotion → more demand → pickup congestion → longer driver cycle → less capacity → late/cancelled orders → lower future trust. Check whether it actually occurred.

## Marketplace number reflex

- Completed orders = placed orders × completion rate.
- With compatible definitions: placed orders = ordering sessions × orders per session.
- GMV is order value; it is not platform revenue.
- Revenue minus defined variable costs gives contribution, not full-company profit.
- Ask who pays the promotion and how much demand is incremental.
- City averages can conceal lunch-hour or neighborhood problems.
- Matching and preparation can overlap; don't add overlapping times twice.
- An experiment can change capacity for the comparison group too.

Before recommending growth: “Can merchants and drivers fulfill the extra demand?”

## Decision reflex

Name **one next step**, the segment, why it comes first, and the evidence that would change it.

Choose a useful outcome plus relevant guardrails. Avoid promising certainty or setting thresholds without a baseline/risk rationale.

“Given the information we have, I’d test … because … . I’d watch … and change direction if … .”

## Communication reflex

**Clarify → Structure → Reason → Evidence → Recommendation → Trade-off → Stop**

- Answer the question early.
- Use two or three useful branches, not a long framework recital.
- Say what you know, what you infer and what you need to check.
- If challenged, update the reasoning instead of defending a weak answer.
- End after the recommendation, main trade-off and change criterion.
- Ask for a moment if needed: “Let me take a few seconds to structure this.”

## Personal-evidence reflex

**Situation → my action → observed result → what I learned**

Separate your work from the team's and the AI's. Describe an actual check you made, a failure, or a decision you changed.

No invented users, savings, experiments or customer outcomes. “I didn’t measure that” is better than a number you cannot defend. Detailed TDCX/FPT Software stories and PRJ226 capabilities are not verified in this kit.

## Last spoken check

Without notes, explain:

1. Why a QA feature could run correctly but still fail to create value.
2. Why more food orders could make the marketplace worse.
3. One real decision you made, its evidence and its limitation.

If one is hard, revisit only that section. Your task is to think clearly, not remember every page.
