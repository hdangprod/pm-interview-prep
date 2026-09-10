# Product thinking

[Study home](README.md) · [Discovery](CUSTOMER_DISCOVERY.md) · [Practice](../katalon/CASES.md)

**Start here:** a product decision connects a real problem, evidence, a feasible change and a useful outcome. Features are possible answers, not the starting point.

## 1. Problem, user and outcome

**What is it?** A problem is the gap between what someone is trying to accomplish and what their current workflow allows.

**Why a PM cares:** Shipping a feature creates little value if it solves the wrong gap.

**Mental model:** User → job → obstacle → consequence.

**Example:** A QA engineer needs confidence before release but spends time separating product bugs from unreliable tests. “Add an AI assistant” is a proposed solution; it does not explain the obstacle.

**Common mistake:** Treating a customer request or a low usage number as a complete problem statement.

**Interview application:** Clarify the user, actual workflow, frequency and cost of the problem before selecting a feature.

**Check yourself:**

- What outcome does the user want independently of our product?
- What evidence would show the problem is unimportant?
- Is the buyer of the software the same person as its daily user?

## 2. Break an ambiguous problem into testable questions

**What is it?** Decomposition separates possible mechanisms so you can investigate the right one.

**Why a PM cares:** “Improve AI adoption” is too broad to act on.

**Mental model:** Define the behavior → locate the break → compare segments → rank explanations.

**Example:** Separate people who never discover the feature, abandon setup, reject output, or finish successfully but have no reason to return. Compare similar tasks and users who do return.

**Common mistake:** Listing ten hypotheses without choosing which evidence matters first.

**Interview application:** State one first comparison and why it could change your decision. Start with a low-cost check; then timebox deeper discovery.

**Check yourself:**

- What precisely counts as adoption?
- Do non-returning users have another opportunity to do the job?
- Which observation would eliminate your leading explanation?

## 3. Prioritize with judgment

**What is it?** Choosing what deserves scarce attention now.

**Why a PM cares:** Every engineering week has an alternative use.

**Mental model:** Impact on the goal × strength of evidence, balanced against effort, risk and dependencies. This is a reasoning aid, not a magic calculation.

**Example:** A small project-template improvement might solve repeated setup friction sooner than redesigning an entire agent. First establish how many relevant users have the friction.

**Common mistake:** Confusing the loudest enterprise request with the most important problem, or using a scoring formula to hide guesses.

**Interview application:** Recommend one choice, name the opportunity cost, and explain what new evidence would change the ranking.

**Check yourself:**

- Why this segment first?
- What could you validate without building the whole feature?
- With half the capacity, what remains essential?

## 4. Turn a problem into a small specification

**What is it?** A shared description of intended behavior and its boundaries.

**Why a PM cares:** Engineering, Design and the customer need to agree on what success looks like.

**Mental model:** Problem → user flow → scope → acceptance criteria → measurement.

**Example — hypothetical review screen:**

- **Problem:** A tester cannot easily identify what a proposed test edit changes.
- **User flow:** Open suggestion → inspect before/after → accept or reject.
- **Scope:** One test case at a time; batch editing is outside this first version.
- **Acceptance:** Reject leaves the file unchanged. Accept applies only the displayed change. A changed underlying file triggers a conflict warning instead of silent overwrite.
- **Failure behavior:** Show save failure and allow safe retry without duplicate changes.
- **Measure:** Time to an informed decision and incorrect changes applied.

**Common mistake:** Writing “fast, accurate and user-friendly” without observable criteria.

**Interview application:** Describe the happy path, one important failure path, permissions, and a measurable success condition. Ask engineers about feasibility rather than invent implementation certainty.

**Check yourself:**

- Could a tester decide whether your requirement is met?
- What happens when the operation only partly succeeds?
- What have you deliberately left out?

## 5. Metrics that match the job

**What is it?** A way to observe whether the intended outcome improved.

**Why a PM cares:** Easy-to-count activity can hide poor outcomes.

**Mental model:** Outcome metric + diagnostic signals + guardrails.

**Example:** For AI-generated tests, useful task completion and total time including review are closer to value than number of generations. Edits help diagnosis, but some edits are desirable.

Define the population, event, denominator and window. “Repeat use within two weeks among users with another relevant task” means something different from repeat use among all sign-ups. How will you identify that opportunity?

**Common mistake:** Treating test failure rate as universally bad. Useful tests can fail because they found real product defects.

**Interview application:** Name a baseline and one metric you refuse to optimize in isolation.

**Check yourself:**

- Can this metric rise while the user's outcome worsens?
- Is the metric average hiding a harmed segment?
- How would you verify the underlying events are measured correctly?

## 6. Validate before scaling

**What is it?** Gathering evidence that a proposed change addresses the problem.

**Why a PM cares:** A polished prototype or enthusiastic interview does not prove impact.

**Mental model:** Risky assumption → smallest credible test → observation → decision.

**Example:** Test a review-screen prototype on realistic tasks before building full workflow automation. Later compare task outcomes against the existing process.

Use interviews for explanations, task observation for usability, and a suitable comparison for impact. A randomized test can strengthen a causal claim; a before/after change may also reflect seasonality or other releases.

**Common mistake:** Saying “A/B test it” without explaining the outcome, comparison, exposure or decision rule.

**Interview application:** Say what you will test, for whom, what you will observe, and what would make you stop. Choose practical thresholds based on baseline and error cost; label provisional targets.

**Check yourself:**

- Which uncertainty does your test actually resolve?
- Could other changes explain the result?
- What is your next action if the evidence is mixed?

## Practice aloud

Take [K-F01](../katalon/CASES.md#foundation) and give a 90-second first response. Ask Gemini to challenge one assumption. Reuse the same reasoning in [S-D01](../shopeefood/CASES.md#intermediate); do not force an identical answer structure.

[Next: customer discovery](CUSTOMER_DISCOVERY.md) · [Quick review](../QUICK_REVIEW.md)
