# Katalon practice cases

[Home](../README.md) · [Testing notes](../study/TESTING_FOR_PM.md) · [AI notes](../study/AI_AGENTS_MCP.md) · [Gemini prompt](../gemini/COACH_PROMPT.md)

Choose one case, answer aloud, then ask for a challenge. Start with 60–90 seconds; extend when needed. Cases are hypothetical, not actual Katalon incidents or interview questions. No answer key or logging required.

Existing case IDs are retained so prior practice stays recognizable. Optional follow-ups are hidden until you open them.

## Foundation

### K-F01 — A customer asks for a feature

A QA lead asks for a button that automatically fixes every failed test. How would you investigate the underlying need?

### K-F02 — Different testers, different needs

A manual tester and an automation engineer both request “easier test creation.” How would you discover whether they need the same solution?

### K-F03 — Write a small specification

A tester needs to inspect and accept or reject an AI-proposed change. Describe a small first version, including acceptance criteria and one failure path.

### K-F04 — Trust

Users say they do not trust generated output. What would you need to understand before choosing a product change?

## Intermediate

### K-D01 — Low adoption

QA engineers try an AI test-generation feature, but many do not use it again. Engineering proposes more agent autonomy. How would you approach the decision?

<details>
<summary>Optional follow-up: K-D01-F1, previously used in coaching</summary>

95% of generated tests run successfully; 70% are edited. In six interviews, most edits appear to adapt tests to project conventions. Comparable tasks take about 20 minutes including generation/review versus 25 minutes manually. Engineering proposes removing review. You have one engineer for one week. What would you test next, and what result would make you change direction?

These are synthetic observations, not facts about Katalon.

</details>

### K-C03 — Green tests, missed defects

Generated tests execute successfully, yet important defects reach users. How would you investigate and define improvement?

<details>
<summary>Optional interviewer follow-up</summary>

Engineering raises the pass rate further. Why might the user's job still be unimproved?

</details>

### K-C04 — Conflicting customer evidence

One customer wants fewer review steps; another says existing reviews miss important changes. How would you decide what to build?

<details>
<summary>Optional interviewer follow-up</summary>

Sales says the larger account must win. How would you handle the disagreement?

</details>

### K-I01 — Heavy editing

Testers frequently rewrite generated tests. What evidence would tell you whether this is a quality failure, useful customization, or a workflow problem?

### K-I02 — Better AI, unchanged retention

A measured output-quality score improves but repeat use stays flat. How would you investigate?

<details>
<summary>Optional interviewer follow-up</summary>

Your team can run only one small validation this week. Choose it and explain the decision it informs.

</details>

## Pressure test

### K-C02 — Enterprise autonomy request

A large customer requests unattended test edits and execution across shared projects. What would you offer initially, and what evidence would justify expanding autonomy?

<details>
<summary>Optional interviewer follow-up</summary>

The customer refuses extra review steps and threatens to leave. What is your recommendation?

</details>

### K-P01 — Engineering wants full automation

Engineering says manual approvals are the biggest cause of delay. You have no direct evidence that users benefit from removing them. How do you move the decision forward?

### K-P02 — MCP permission failure

An assistant can read test results through an MCP server. A new workflow also needs to edit tests, but some users lack write access. Design the user experience and action boundaries.

<details>
<summary>Optional interviewer follow-up</summary>

An update times out. The assistant does not know whether it succeeded. What should happen next?

</details>

### K-C05 — A competitor launches similar AI

A customer can generate tests with a coding assistant and Playwright agents. How would you evaluate whether an integrated QA product still solves a valuable problem for that customer?

<details>
<summary>Optional interviewer follow-up</summary>

You have half the planned engineering capacity. What would you prioritize, and what evidence could reverse that choice?

</details>

### K-P03 — Cost versus useful outcomes

An improved model produces better individual outputs but doubles latency and increases cost per completed task. Would you ship it?

<details>
<summary>Optional interviewer follow-up</summary>

Power users prefer it; occasional users abandon more often. Make a recommendation with incomplete data.

</details>

## Mock interview

Paste into Gemini after the [coach prompt](../gemini/COACH_PROMPT.md):

> Run a Katalon PM Intern mock. Ask one question at a time: first a customer problem, then a technical/QA case with AI evaluation, an applied agent/MCP question, a small specification, and a real behavioral story. Probe like a PM, then a Product Director. Challenge evidence, autonomy and priorities. Let me answer before feedback; save overall feedback until I say “end mock.” Use new hypothetical details, not claimed company facts.

For a true behavioral answer, choose a real integration or PRJ226 incident. Do not turn a practice scenario into experience.

[Optional previous attempts](case-bank.md) · [Company research](research.md) · [Quick review](../QUICK_REVIEW.md)
