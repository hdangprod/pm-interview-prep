# Katalon research

Accessed 2026-09-10. Public documented facts below; capability claims are not independent performance validation. Candidate supplied the exact job URL during setup; it was opened and matched to the initially located official listing.

## Sources and findings

- K1 — [Candidate-supplied official PM Intern role](https://katalon.com/careers/job/8186179), retrieved Sep 10; relative posting date only. Also matched [official careers listing](https://careers.katalon.com/jobs/8186179-product-management-intern). Lists testing research, customer problem statements/JTBD, workflows/prototypes, specs, interviews and success metrics. Explicitly asks for English, effective AI use, MCP explanation, and decomposition of broad agent problems. Confirms a panel assessment. Exact panel composition remains candidate expectation.
- K2 — [Studio Agent mode](https://docs.katalon.com/katalon-studio/studioassist/studioassist-agent-mode), updated August 2026. Uses project context, documentation and MCP tools to create/update assets and investigate failures. Users can review generated file changes. Distinguishes task execution from Ask-mode answers.
- K3 — [True Platform AI Assistant](https://docs.katalon.com/katalon-platform/katalon-ai-assistant), updated August 2026. Covers requirements, generation, execution, failure analysis, bugs and project insights. Documents approval before mutating/running actions. Keep this platform-specific behavior separate from Studio configuration.
- K4 — [Studio AI overview](https://docs.katalon.com/katalon-studio/studioassist/studioassist-overview), updated August 2026. Describes Ask and Agent modes and provider/license requirements. Product understanding should distinguish Studio test-authoring context from platform coordination.
- K5 — [True Platform MCP](https://docs.katalon.com/katalon-platform/testops-mcp-server), updated September 2026. External AI clients can work with platform testing artifacts through exposed tools. Availability is specifically True Platform; do not assume identical permissions or capabilities across all deployments.
- K6 — [Katalon MCP product page](https://www.katalon.com/katalon-mcp), date not shown. Describes remote platform and local Studio connectivity and workflow skills. Relevant product question: meet users in existing development workflows.
- K7 — [MCP architecture](https://modelcontextprotocol.io/docs/2026-07-28/learn/architecture), official protocol documentation. MCP standardizes context/tool exchange using host/client/server roles; it does not itself determine the application's reasoning or context-management policy.
- K8 — [Playwright Test Agents](https://playwright.dev/docs/test-agents), official competitor/alternative documentation. Planner, generator and healer support test creation and repair. This is evidence that agent-based testing alternatives exist, not evidence of superiority.

## Product/workflow map — coach synthesis

QA/tester prepares requirements and test assets → executes against application/environment → inspects failures and evidence → distinguishes product defect, test issue, or environment issue → updates tests/bugs → informs release decision.
Studio supports automated-test authoring; True Platform coordinates testing artifacts and visibility; documentation also lists cloud execution and TrueTest surfaces. Do not conflate “AI testing a conventional app” with “evaluating an AI product.”

Likely users: QA engineers, hybrid manual/automation testers, developers; leads/managers need trustworthy release information. Buying/admin stakeholders may have different needs from daily users. These persona implications are inference.

## Interview implications — inference

Practice investigation of a specific failing workflow, adoption beyond first use, evaluating useful/correct tests, requirements and acceptance criteria, risk-based autonomy, observable actions, recovery, and evidence that a candidate challenged AI.
A useful evaluation may distinguish executable tests from tests with correct assertions and meaningful coverage. Passing tests alone are not proof of product correctness.
MCP drill: explain the host/client/server flow for reading a test result or creating a test case, then reason about permissions, incorrect arguments, and review. Avoid presenting MCP as an LLM, agent, or security guarantee.
Competitive case: why choose an integrated QA workflow when a coding agent can generate Playwright tests? Validate workflow and governance needs rather than assert Katalon wins.

## Limits / next refresh

No independent testing of products performed; no pricing or performance comparisons established. Do not claim hands-on Katalon experience for the candidate.
Research supports likely evaluation dimensions, not exhaustive interview questions. Refresh only relevant changing facts before final mock.

