# Testing for a PM

[Study home](README.md) · [AI evaluation](AI_AGENTS_MCP.md#6-evaluate-the-users-job) · [Katalon cases](../katalon/CASES.md)

**Start here:** testing produces evidence about quality and release risk. A green report is useful only if tests check meaningful behavior.

## Essential building blocks

### Tests and defects

**What is it?** A test case describes conditions, inputs/actions and expected results. A test suite groups cases for a purpose. A bug/defect is a product flaw; a failed test is an observation needing diagnosis.

**Why a PM cares:** Without a clear expected result, a generated test can check the wrong thing.

**Mental model:** Requirement → action → expected result → observed result.

**Example:** Given an expired coupon, submitting an order must show the agreed message and must not apply the discount. Checking only that the page loads misses the requirement.

**Common mistake:** Counting tests as quality, regardless of assertions or risk.

**Interview application:** Ask whether tests catch relevant failures, not just whether they execute.

**Check yourself:**

- What makes an expected result trustworthy?
- Can a failed test occur without a product defect?

### Manual, automated and regression testing

**What is it?** Manual testing uses a person to explore or execute checks. Automated testing uses software. Regression testing checks that changes have not broken previously working behavior; it can be manual or automated.

**Why a PM cares:** Automation brings repeatability but setup and maintenance costs. Human exploration helps when behavior is unclear.

**Mental model:** Repeat stable checks; explore uncertainty; recheck existing behavior after change.

**Example:** Automate a frequent API permission check; use human judgment to explore confusing first-use behavior.

**Common mistake:** “Automate everything.” Automating a poor test repeats a poor check faster.

**Interview application:** Prioritize by risk, frequency, stability and maintenance cost.

**Check yourself:**

- Which test is worth automating first?
- When is manual testing a better starting point?

### Levels and surfaces

**What is it?** Levels describe scope; surfaces describe how you interact with the system.

- **Unit:** A small part in isolation, such as a discount calculation.
- **Integration:** Parts working together, such as order service and payment adapter.
- **API:** Requests/responses and behavior through a programmatic interface.
- **UI:** User-visible behavior through the interface.
- **End-to-end:** A complete journey spanning components, such as checkout through confirmation.

API tests can be integration tests; UI tests are not always full end-to-end tests.

**Why a PM cares:** Different checks reveal different problems at different costs.

**Mental model:** Narrow checks localize failures; broader checks show whether the journey works.

**Example:** Correct pricing in a unit test does not prove checkout sends the right price to payments.

**Common mistake:** Treating categories as mutually exclusive or relying only on a large UI suite.

**Interview application:** Explain the missing evidence if only one layer is tested.

**Check yourself:**

- What could an API test catch that a calculation unit test misses?
- Why does a complete journey still need narrower checks?

## The QA workflow

**Requirement → Test Design → Test Creation → Execution → Failure → Diagnosis → Fix → Regression → Release**

This shows a path through failure; not every run must fail. Learning can send the team backward.

Each stage follows **job / friction / possible AI help / AI risk**. Opportunities are hypothetical, not a claim every product provides them.

### 1. Requirement

- **Job:** Agree on behavior and acceptance criteria.
- **Friction:** Missing rules and conflicting documents.
- **Possible AI help:** Flag ambiguity; suggest clarification questions.
- **AI risk:** Invent business rules that appear agreed.

### 2. Test design

- **Job:** Choose scenarios and risks worth checking.
- **Friction:** Overlooked paths and redundant cases.
- **Possible AI help:** Suggest boundary, negative and regression scenarios.
- **AI risk:** Generate shallow cases while missing costly failures.

### 3. Test creation

- **Job:** Create usable manual steps or automated checks.
- **Friction:** Setup, data, locators, assertions and conventions.
- **Possible AI help:** Draft steps/scripts from verified requirements.
- **AI risk:** Invent APIs, expose secrets, use wrong data or weak assertions.

### 4. Execution

- **Job:** Run checks in the right environment and collect evidence.
- **Friction:** Slow runs, unavailable environments and authentication.
- **Possible AI help:** Assist setup or execute bounded tasks.
- **AI risk:** Use the wrong environment or misreport completion.

### 5. Failure

- **Job:** Capture what failed and its context.
- **Friction:** Noisy alerts and missing reproduction details.
- **Possible AI help:** Summarize logs and group symptoms.
- **AI risk:** Hide an outlier or summarize incomplete evidence confidently.

### 6. Diagnosis

- **Job:** Distinguish product, test, data and environment faults.
- **Friction:** Multiple systems and intermittent behavior.
- **Possible AI help:** Rank explanations; retrieve relevant changes.
- **AI risk:** Present correlation as root cause.

### 7. Fix

- **Job:** Correct the actual fault and review the change.
- **Friction:** Uncertain scope and unintended consequences.
- **Possible AI help:** Propose a bounded patch with evidence.
- **AI risk:** Weaken assertions or skip tests just to turn the report green.

### 8. Regression

- **Job:** Check the repair and protect existing behavior.
- **Friction:** Slow suites, duplicates and unstable checks.
- **Possible AI help:** Suggest relevant cases and gaps.
- **AI risk:** Exclude an important case or repeat a wrong assumption.

### 9. Release

- **Job:** Decide whether remaining risk is acceptable.
- **Friction:** Scattered evidence and unclear coverage.
- **Possible AI help:** Summarize results with sources and uncertainties.
- **AI risk:** Overstate confidence or omit unresolved failures.

**Check yourself:**

- Where would faster generation leave the bottleneck untouched?
- Which stage needs the clearest human decision boundary?
- What evidence should accompany a proposed fix?

## Reliability, maintenance and delivery

### Flaky tests and maintenance

**What is it?** A flaky test passes or fails inconsistently under apparently unchanged conditions. Maintenance keeps tests aligned with intended behavior and changing environments.

**Why a PM cares:** Noise wastes time and teaches teams to ignore genuine alerts.

**Mental model:** Reproduce → isolate cause → repair → verify repeated behavior.

**Example:** A UI check intermittently fails because a fixed wait is shorter than a variable response time. Shared data or environments may cause other intermittent failures.

**Common mistake:** Treating a passing retry as proof nothing is wrong, or “healing” by removing checks.

**Interview application:** Measure false alarms, investigation effort and trust. Compare realistic runs.

**Check yourself:**

- Could the intermittent behavior be in the product?
- Does the repaired test still check the requirement?

Testing visible behavior and isolating tests are emphasized in [Playwright's guidance](https://playwright.dev/docs/best-practices).

### CI/CD and coverage

**What is it?** Continuous integration regularly combines and checks changes. Continuous delivery keeps changes releasable; continuous deployment automatically releases eligible changes. Coverage describes what tests exercise: code, requirements or risks.

**Why a PM cares:** Tests affect feedback speed and release confidence. “High coverage” needs a definition.

**Mental model:** Change → timely evidence → informed release.

**Example:** A suite can cover many code lines but never verify a refund amount. Slow checks can delay useful feedback.

**Common mistake:** “100% coverage means no bugs,” or confusing delivery with automatic production release.

**Interview application:** Connect coverage to important risks; balance speed with missed-failure cost.

**Check yourself:**

- Which business risk is absent from the coverage number?
- What would you check before removing a slow test?

## Relate this to Katalon

The [research](../katalon/research.md) distinguishes Studio authoring from True Platform coordination and AI-assisted testing. Learn where the user works before proposing a feature. Documentation is not independent accuracy evidence.

Practice [K-C03](../katalon/CASES.md#intermediate): tests run but miss defects. Explain the harm and evidence needed before suggesting a solution.

[Quick review](../QUICK_REVIEW.md) · [Gemini prompt](../gemini/COACH_PROMPT.md)
