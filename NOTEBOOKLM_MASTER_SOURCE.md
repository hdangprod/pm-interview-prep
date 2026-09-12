# Product Management Interview Foundations: NotebookLM Master Source

For a beginner preparing for **Katalon Product Management Intern** and **ShopeeFood Associate Product Management** interviews. Written in clear English for a learner with a software and technical integrations background.

This is the learning material. It explains ideas, connects them, and demonstrates decisions. It can be understood without opening other repository files.

**Priority key**

- **P0 — MUST KNOW:** Core reasoning that is likely to affect interview performance. This is a study priority, not a confirmed company interview rubric.
- **P1 — SHOULD KNOW:** Knowledge that supports stronger explanations and decisions.
- **P2 — OPTIONAL DEPTH:** Useful extensions after the foundations are clear.

**Evidence key**

- **FACT:** A supported observation or a stated definition. A fact has a scope; it does not automatically explain a cause.
- **HYPOTHESIS:** A possible explanation or predicted effect that needs evidence.
- **ILLUSTRATIVE EXAMPLE:** Invented teaching material. All company-named cases, numerical exercises, customer conversations, and proposed product behavior in this source are hypothetical unless explicitly identified otherwise.
- **PERSONAL EVIDENCE REQUIRED:** The repository does not contain enough candidate evidence to make the claim or tell the story.

Company names identify preparation tracks. The examples do not claim to describe actual company incidents, internal policies, existing features, interview questions, or the candidate's work. Numerical targets are teaching assumptions, not industry benchmarks.

## Table of contents

- [Part 0: How to use this source](#part-0-how-to-use-this-source)
- [Part 1: PM thinking from zero](#part-1-pm-thinking-from-zero)
- [Part 2: Case solving from zero](#part-2-case-solving-from-zero)
- [Part 3: Systems thinking](#part-3-systems-thinking)
- [Part 4: Customer discovery](#part-4-customer-discovery)
- [Part 5: Hypotheses and evidence](#part-5-hypotheses-and-evidence)
- [Part 6: Metrics from zero](#part-6-metrics-from-zero)
- [Part 7: Trade-offs and decision making](#part-7-trade-offs-and-decision-making)
- [Part 8: Software testing for a PM](#part-8-software-testing-for-a-pm)
- [Part 9: AI fundamentals for a PM](#part-9-ai-fundamentals-for-a-pm)
- [Part 10: RAG, tools, agents and MCP](#part-10-rag-tools-agents-and-mcp)
- [Part 11: AI product judgment](#part-11-ai-product-judgment)
- [Part 12: Katalon product case mental models](#part-12-katalon-product-case-mental-models)
- [Part 13: Marketplace thinking from zero](#part-13-marketplace-thinking-from-zero)
- [Part 14: Marketplace systems thinking](#part-14-marketplace-systems-thinking)
- [Part 15: Marketplace diagnosis](#part-15-marketplace-diagnosis)
- [Part 16: Unit economics from zero](#part-16-unit-economics-from-zero)
- [Part 17: ShopeeFood case mental models](#part-17-shopeefood-case-mental-models)
- [Part 18: Product communication](#part-18-product-communication)
- [Part 19: Behavioral interview thinking](#part-19-behavioral-interview-thinking)
- [Part 20: Common beginner failure modes](#part-20-common-beginner-failure-modes)
- [Part 21: Mini case walkthroughs](#part-21-mini-case-walkthroughs)
- [Part 22: Concept comparisons](#part-22-concept-comparisons)
- [Part 23: Glossary](#part-23-glossary)
- [Part 24: Active recall question bank](#part-24-active-recall-question-bank)
- [Part 25: Flashcard-ready facts](#part-25-flashcard-ready-facts)
- [Part 26: Audio-ready recaps](#part-26-audio-ready-recaps)
- [Sources and evidence boundaries](#sources-and-evidence-boundaries)
- [Part 27: Final 15-minute review](#part-27-final-15-minute-review)

## Part 0: How to use this source

**P0 — MUST KNOW**

Use Audio Overviews to reinforce concepts, Mind Maps to see relationships, Quizzes to retrieve ideas from memory, and Flashcards to learn terms. Study Guides can organize P0 before P1 and P2. You control the order and pace.

For active practice, choose one case and attempt it aloud before reading its walkthrough or answer cues. Ask a coach to reveal one question at a time. Listening builds familiarity; speaking through a new case tests whether you can use the ideas. NotebookLM supports that practice but cannot replace it.

When generating learning material, keep the evidence labels. Ask for hypothetical scenarios to stay hypothetical and for missing personal evidence to stay missing.

## Part 1: PM thinking from zero

**P0 — MUST KNOW**

### 1.1 What a Product Manager actually does

A Product Manager helps a team decide **which problem to solve, for whom, why it matters, and how to judge the result**. The PM brings together user needs, business goals, and what the team can realistically deliver.

Think of a restaurant with a long queue. Someone proposes a second payment terminal. Before buying it, you need to know where customers wait. If food preparation is slow, faster payment may only move the queue into the kitchen. The product decision is choosing the useful change, based on the real constraint.

A PM's work can include observing customers, interpreting data, writing requirements, comparing options, working with engineers and designers, and checking outcomes after launch. A PM does not need to know every answer or perform every role. The responsibility is to help the team make coherent decisions and learn when those decisions are wrong.

Four things often appear together but mean different things:

- **User problem:** An obstacle to the person's intended outcome. A QA engineer cannot tell whether a failed test means checkout is broken.
- **Business problem:** An obstacle to a sustainable business outcome. Customers may stop renewing if the testing product does not help them make release decisions.
- **Technical problem:** A limitation or fault in the system. Test logs may lack the request identifier needed to connect events.
- **Solution:** A possible response. Add linked request logs, a diagnosis view, or an AI summary.

These can be connected: missing log context → slower diagnosis → delayed release decisions → weaker perceived product value. That chain is a **hypothesis** until supported. A technical improvement matters to the PM because of the outcome it enables, not just because it is technically elegant.

**Decision-making under uncertainty** means choosing when the information is incomplete. You may know the workflow is slow without knowing whether the main cause is setup, review, or execution. The next useful decision may be to observe three realistic tasks before building a large feature. Uncertainty calls for a deliberate learning step, not confident guessing.

### 1.2 Symptom, problem, root cause and solution

A **symptom** is an observable signal. A **problem** is the important gap behind that signal. A **root cause** is an underlying mechanism that explains it at a useful level. A **solution** changes a mechanism or reduces its consequences.

**ILLUSTRATIVE EXAMPLE — Orders dropped 20%.**

“Orders dropped 20%” is a symptom. It leaves many questions open: placed or completed orders, over which period, and in which city? The business problem may be fewer successfully served meals and lower contribution. The buyer's problem might be inability to find an available driver at lunch.

Possible explanations include fewer visitors, lower checkout conversion, unavailable restaurants, fewer available drivers, payment errors, higher total price, or an incorrect report. A launch promotion addresses some demand problems. It may worsen a fulfillment shortage.

Do not jump from the symptom to “the root cause is low demand.” First ask what evidence separates demand from fulfillment. If placed orders stayed stable but completion fell, a demand-only explanation becomes less convincing.

**ILLUSTRATIVE EXAMPLE — AI output is edited frequently.**

The symptom is a high edit rate. The problem might be incorrect output, but users may also be making useful project-specific changes. A possible cause is missing project conventions. A possible solution is supplying an approved template. Removing editing would lower the measured edit rate while possibly making the product worse.

**ILLUSTRATIVE EXAMPLE — Tests fail after a release.**

The symptom is test failure. The product may contain a real bug, or the test may expect an old button label. Updating the test is correct only if the intended behavior changed. If checkout is charging twice, “repairing” the assertion to accept two charges hides a defect.

There may be several interacting causes. A slow restaurant and inaccurate preparation estimates can both contribute to driver waiting. “Root cause” should not force a complex system into one explanation. Choose a causal depth that changes the decision: “people are careless” is less useful than “stock updates do not reach the menu before orders are placed.”

**Better reflex:** Define the symptom → identify whose outcome suffers → propose mechanisms → ask for distinguishing evidence → choose a response.

### 1.3 Goal versus proposed solution

A **goal** describes the outcome you want. A **proposed solution** describes one way to achieve it.

Engineering says, “We need more AI autonomy.” Autonomy means the system can take more actions without asking a person. That is a design choice. The goal could be reducing QA effort while maintaining reliable defect detection.

Use this sentence to expose the real decision:

> Improve X without materially harming Y.

For Katalon preparation: improve time to a useful test without materially harming test correctness or user control.

For ShopeeFood preparation: improve completed lunch orders without materially harming delivery reliability, driver earnings, or contribution per order.

“Materially” needs a practical meaning. A team should agree which harms are unacceptable and what change would trigger review. Do not invent a universal acceptable cancellation rate. Ask for the baseline, affected population, error cost, and business constraints.

There can be more than one goal. If growth and near-term economics conflict, clarify which takes priority and within what budget. Naming the conflict is more useful than claiming to maximize everything.

### 1.4 Problem framing

A useful problem statement connects **user, context, obstacle, impact, and evidence**.

> [User] experiences [problem] when [context], resulting in [impact].

**ILLUSTRATIVE EXAMPLE:** “QA engineers struggle to check whether generated assertions match the requirement when reviewing tests before release, which increases review effort and uncertainty about coverage.”

That is a proposed framing, not a research finding. Add evidence when you have it: “In an observed task, the tester repeatedly switched between the requirement and test file.” Then separate what remains unknown: “We have not established how common this is.”

For food delivery: “Office workers cannot reliably receive lunch within their break when nearby fulfillment capacity is overloaded, leading to abandoned or cancelled orders.” This also needs evidence. Office workers, overload, and the consequence are hypotheses unless supplied by the case.

The sentence helps prevent solution-first thinking. It is less useful when used mechanically during an urgent incident. If payment is currently failing, mitigate the incident while confirming scope. You can refine the problem statement as you learn.

### 1.5 From a problem to requirements and a small product spec

**P1 — SHOULD KNOW**

A **requirement** states behavior or a constraint the product must satisfy. A **product specification**, or spec, organizes the problem, intended experience, scope, important rules, and success measures so a team can build and evaluate the same thing.

**ILLUSTRATIVE EXAMPLE — A review screen for AI test changes.**

- **Problem:** Reviewers cannot easily see whether the suggestion changes the test's meaning.
- **User and context:** A QA engineer reviewing one proposed test change in an authorized project.
- **Goal:** Reduce effort to make a correct review decision.
- **Flow:** Open suggestion → inspect original and proposed test → inspect supporting requirement → accept or reject.
- **First scope:** One test at a time. Batch editing can wait until single-change review works.
- **Acceptance criteria:** Reject leaves the file unchanged. Accept applies only the displayed change. The user can see whether expected behavior changes. If the source file changed after the suggestion was created, ask for renewed review instead of silently overwriting it.
- **Failure behavior:** A save failure is visible. If completion is uncertain after a timeout, check the resulting state before retrying.
- **Permissions:** Users without write access can inspect an allowed suggestion but cannot apply it.
- **Measures:** Correct review decisions and total review time; incorrect changes applied are a guardrail.

An **acceptance criterion** is an observable condition for deciding whether the requirement is met. “Easy and accurate” is hard to test. “Reject leaves the file unchanged” is testable.

The spec should leave room for engineering and design input. It need not prescribe every technical detail. State the desired behavior clearly enough to expose disagreements before implementation.

### Check yourself: PM foundations

Choose one question at a time. Explain with an example before moving on.

1. Why is “add automatic repair” not a problem statement?
2. How could a technical improvement create no user value?
3. What observation would make you revise the office-worker problem statement above?

**Audio recap — PM thinking:** A PM helps the team choose a useful change. Imagine buying a second payment terminal when the kitchen is the real queue. Start with the user's job, find the obstacle, and ask what evidence supports it. The common mistake is treating a proposed feature as the goal. Ask yourself: what are we trying to improve, and what must not become worse?

## Part 2: Case solving from zero

**P0 — MUST KNOW**

A product case gives you an incomplete situation and asks you to make a decision. It tests how you reduce uncertainty. You are not expected to magically know private company data.

Use this operating system:

**GOAL → ACTORS → PROBLEM → BREAKDOWN → HYPOTHESES → EVIDENCE → ACTION → TRADE-OFF → METRICS.**

This is a set of questions, not nine paragraphs to recite. You can move back when new evidence changes the problem. Sometimes an urgent action happens before diagnosis is complete.

### 2.1 GOAL: What are we trying to improve?

**Why it matters:** The same feature can be good for one objective and poor for another. Faster releases, fewer missed defects, and more AI usage are different outcomes.

**Beginner mistake:** Accepting the requested feature as the goal or saying “improve user experience” without a concrete outcome.

**Katalon example:** “Is the priority to reduce total test-creation effort while preserving meaningful checks?”

**ShopeeFood example:** “Are we trying to recover completed orders, and what economic or service limits must we respect?”

If the interviewer supplies no answer, state a reasonable working goal and keep it revisable.

### 2.2 ACTORS: Who participates and who is affected?

**Why it matters:** The person requesting a feature may not be the person using it or carrying its risks.

**Beginner mistake:** Saying “the user” as though all users have identical needs.

**Katalon example:** A QA engineer reviews output, an administrator controls access, and a release lead uses test results to judge risk.

**ShopeeFood example:** Buyers order, merchants prepare, drivers deliver, and the platform coordinates and funds parts of the service.

Choose the actors relevant to the problem. Listing every department adds little unless it changes your decision.

### 2.3 PROBLEM: What gap is actually causing harm?

**Why it matters:** A symptom shows movement; a problem explains why the movement matters to someone.

**Beginner mistake:** “AI usage is low, so we need more AI features.”

**Katalon example:** The possible problem is that test review takes almost as long as writing tests manually. Verify the total task time.

**ShopeeFood example:** Buyers may be placing orders but failing to receive them because delivery cannot be arranged. Confirm the order status breakdown.

Separate what the prompt tells you from your interpretation. Say “possible problem” when the mechanism is not established.

### 2.4 BREAKDOWN: Where in the journey could the problem occur?

**Why it matters:** Breaking the system into stages makes investigation manageable.

**Beginner mistake:** Listing generic categories with no connection to the observed outcome.

**Katalon example:** Discover feature → set up → generate → review → use a useful test → return for another relevant task.

**ShopeeFood example:** Visit → select meal → place order → merchant accepts → fulfillment arranged → pickup → delivery. Some steps overlap operationally.

The breakdown should help you locate a failure. If users never complete setup, start there before optimizing generated explanations.

### 2.5 HYPOTHESES: What mechanisms could explain the gap?

**Why it matters:** Competing explanations prevent attachment to the first plausible story.

**Beginner mistake:** Treating a hypothesis as an established cause or producing an endless list without ranking it.

**Katalon example:** Missing project context could cause corrections; infrequent testing tasks could explain low return; slow generation could cause abandonment.

**ShopeeFood example:** A lunch decline could reflect fewer buyer visits, overloaded kitchens, or drivers spending more time at pickup.

Select a few distinct explanations. Rank them by fit with timing, segment, likely impact, and ease of checking.

### 2.6 EVIDENCE: What observation would distinguish the explanations?

**Why it matters:** “Look at data” is too vague. Useful evidence changes what you would do.

**Beginner mistake:** Requesting a dashboard of every metric without a decision in mind.

**Katalon example:** Observe returners and non-returners completing comparable tasks. Classify review edits and measure where time goes.

**ShopeeFood example:** Compare placed and completed orders at lunch. Then inspect merchant acceptance, assignment time, and pickup wait in affected zones.

Name the expected pattern. “If assignment time rose but kitchen preparation stayed stable, a delivery-capacity explanation becomes stronger.” This is a prediction, not a conclusion.

### 2.7 ACTION: What should happen next, given current evidence?

**Why it matters:** A diagnosis has value when it guides a feasible decision.

**Beginner mistake:** Staying in analysis forever or proposing a large feature before testing its main assumption.

**Katalon example:** If convention mismatch dominates, test an approved project template on a limited set of tasks. An engineer and QA reviewer can compare it with the current workflow.

**ShopeeFood example:** If a few overloaded restaurants drive pickup delays, operations could trial capacity-aware order limits with those merchants.

Be specific about scope, responsible team, and what you expect to learn. A learning action, temporary mitigation, or small product change can all be valid next steps.

### 2.8 TRADE-OFF: What could this action make worse?

**Why it matters:** Effects cross users, time periods, and parts of the system.

**Beginner mistake:** Naming only the benefit or giving a generic “cost versus quality” without a mechanism.

**Katalon example:** Applying templates may reduce edits but could copy outdated conventions across projects. Keep templates owned and versioned.

**ShopeeFood example:** Limiting restaurant orders may reduce cancellations but also reduce merchant revenue and buyer selection. Consider alternative restaurants and the merchant's capacity.

Use “and then what happens?” to follow the intervention one step further.

### 2.9 METRICS: How will we know whether it worked?

**Why it matters:** The measure should reflect the original goal and detect important harms.

**Beginner mistake:** Counting feature clicks or raw orders while ignoring successful outcomes.

**Katalon example:** Total time to a verified, useful test; guardrails include incorrect assertions and unauthorized changes.

**ShopeeFood example:** Completed orders in affected lunch zones; guardrails include cancellations, severe lateness, driver earnings per online hour, and contribution.

Define the population, event, denominator, time window, and comparison. Use only the most relevant metrics in the spoken answer; expand when asked.

### 2.10 How a beginner can use this during an interview

Start by clarifying the one ambiguity that changes the investigation most. If the prompt is “orders dropped,” ask whether it means placed or completed orders. Then offer two or three branches and explain which you would check first.

You can say: “I do not know the cause yet. I would first separate demand from fulfillment by comparing placed and completed orders.” That is a useful response because it names an uncertainty, a comparison, and its purpose.

If the interviewer asks for a decision before providing more data, make a conditional recommendation. State your working assumption, choose a limited action, and name what would change it. Do not spend the whole answer requesting unavailable information.

**Check yourself:** If you can ask only one question about low AI repeat use, which question best separates lack of value from lack of another task?

## Part 3: Systems thinking

**P0 — MUST KNOW**

Systems thinking means recognizing that changing one part can affect other parts, sometimes indirectly or after a delay. A product is used inside a system of people, incentives, technology, and operating limits.

### 3.1 Causal chains and the question “And then what happens?”

A **causal chain** describes a proposed sequence where one change helps cause another. An arrow means “may lead to through this mechanism,” not “is guaranteed to cause.”

**ILLUSTRATIVE HYPOTHESIS — Promotion:**

Promotion → lower effective price → more order attempts → more demand for kitchen and driver capacity → longer waits if capacity is tight → higher cancellation → weaker future trust.

The first links may fail if customers do not notice the offer. The capacity links may fail if merchants and drivers have spare capacity. The trust link may vary by customer and service recovery. For each arrow, ask what condition must hold and what evidence would show the change happened.

**ILLUSTRATIVE HYPOTHESIS — AI autonomy:**

More automatic test edits → fewer human review steps → faster workflow → incorrect edits sometimes applied → real defects hidden → lower trust → users disable automation.

This chain is not an argument against all autonomy. It shows why faster action should be evaluated together with error cost and downstream behavior. A carefully bounded action with strong checks may avoid much of the harm.

### 3.2 First-order, second-order and unintended effects

A **first-order effect** is close to the intervention. A **second-order effect** follows as people or other parts respond. A **third-order effect** is a further consequence. These labels help you keep looking; exact numbering is less important than the mechanism.

For a driver incentive, more drivers may enter a target district. That is a direct response. A nearby district may lose drivers. Its ETAs may then rise and buyers may leave. A local success can therefore hide a wider loss.

An **unintended consequence** is an effect the team did not aim for. It can be positive or negative. A clearer test review view might also help new employees learn conventions. Conversely, removing review might make release leads less willing to rely on the report.

Do not confuse a possible downside with a reason to reject the idea automatically. Estimate who bears it, how large it could be, how reversible it is, and whether a guardrail can detect it.

### 3.3 Constraints and bottlenecks

A **constraint** is a limit: budget, permissions, time, staff, kitchen capacity, or model latency. A **bottleneck** is the limiting step that most restricts the current workflow's output.

**ILLUSTRATIVE EXAMPLE:** A QA workflow spends 5 minutes drafting tests and 25 minutes gathering unclear requirements. Cutting drafting time to 1 minute saves 4 minutes, not 24. Improving requirement clarity may offer more value. Measure rather than assume where the bottleneck sits.

For delivery, registered driver count is not the same as available capacity. A driver waiting at a restaurant cannot immediately serve another order. A kitchen delay can create an apparent driver shortage even when the number of online drivers stays stable.

Improving a bottleneck can move the constraint elsewhere. Faster preparation may reveal that delivery capacity is now limiting completion. Recheck the system after a change.

### 3.4 Feedback loops

**P1 — SHOULD KNOW**

A **feedback loop** occurs when a change travels through a chain and affects the original condition again.

A **reinforcing loop** amplifies a direction. Hypothetically, reliable deliveries encourage repeat buying; denser demand can make driver time more productive; more reliable available capacity may improve deliveries again. This requires suitable economics and balanced capacity. Growth alone does not guarantee the loop.

A **balancing loop** pushes against a change. Rising demand may overload kitchens, causing longer waits that reduce buyer conversion. Demand then stops rising. “Balancing” describes the opposing force; it does not mean the result is desirable.

Delays make loops harder to see. A bad meal delivery today may affect next week's orders. A rushed AI change may cause a defect discovered after release. Measure across a time window that can reveal the effect.

### 3.5 A practical systems check

Before recommending an intervention, explain:

1. Who changes behavior first?
2. Which resource or workflow receives more work?
3. Where might capacity or control fail?
4. Who bears that failure?
5. What later behavior could change?

**Check yourself:** A team doubles test generation speed. Review time rises because there are twice as many suggestions. What metric would reveal whether the user actually saves effort?

**Audio recap — Systems thinking:** Imagine sending more water into a narrow pipe. More input does not guarantee more useful output. A promotion can bring orders into a kitchen that is already full. Faster AI can send more work into a human review queue. Follow the proposed change through the next person and the next constraint. Ask: and then what happens, and how would I know?

## Part 4: Customer discovery

**P0 — MUST KNOW**

Customer discovery is learning how people try to achieve an outcome, where they struggle, and whether the problem is worth solving. It helps a team replace assumptions with evidence before committing to a solution.

### 4.1 The vocabulary, connected to one example

Imagine a company buying testing software for its QA team. The **customer** is the purchasing organization or paying party. The **user** is the person interacting with the product. The buyer, administrator, and daily tester may have different goals.

A **segment** groups people by a difference that matters to the decision. Manual testers moving into automation may need different help from experienced automation engineers. Segment by behavior, job, constraints, or context before inventing demographic details.

A **customer problem** is an obstacle to a desired outcome. A **pain point** is a specific difficulty within that problem. The broad problem may be slow release decisions; repeatedly searching for failure logs is a pain point.

A **need** is something required to make progress. The tester needs enough evidence to classify a failure. A **feature request** is a suggested implementation, such as “add automatic test repair.” The **underlying need** may be reducing repetitive investigation without losing confidence in the release.

A **workflow** is the sequence of actions and handoffs used to complete a job. A **workaround** is what people do when the current product does not support them well. A tester may copy logs into a document and ask a colleague to interpret them. That workaround can reveal urgency, effort, and missing support.

An **assumption** is something treated as true without enough evidence. A **hypothesis** is a testable explanation or prediction. **Evidence** is information that supports or challenges a claim. **Validation** is gathering enough relevant evidence to support a particular decision. It does not mean proving an idea can never fail.

### 4.2 Feature request does not equal underlying problem

**ILLUSTRATIVE EXAMPLE — “Add automatic test repair.”**

Start with the recent event behind the request. Ask: “Tell me about the last failed test you wanted repaired.” Suppose the person describes spending an hour comparing a new page with an old locator. That example points toward maintenance after interface changes. It does not prove all failures should be repaired automatically.

Ask what they were trying to accomplish. Their answer may be “finish the release checks by Friday.” Ask what happened today, what they did instead, and the consequence. Perhaps the real delay was waiting for someone to confirm whether the interface change was intentional.

Several possible needs can sit behind the same request:

- Find the correct element after an intended UI change.
- Decide whether the application or the test is wrong.
- Reduce repetitive updates across many similar tests.
- Avoid waiting for another team to explain a requirement.

These needs suggest different options: stable locators, clearer change notices, better diagnosis, bulk editing with review, or bounded AI assistance. Discovery keeps those options open until the evidence narrows them.

### 4.3 Ask about behavior, then explore explanations

Useful questions have a purpose:

- **“What are you trying to accomplish?”** Establish the desired outcome.
- **“What happens today?”** Learn the existing process before proposing a replacement.
- **“Tell me about the last time this happened.”** Move from general opinion to a concrete event.
- **“What did you do instead?”** Reveal workarounds and alternatives.
- **“What was the consequence?”** Understand impact rather than irritation alone.
- **“How often does this happen?”** Estimate recurrence, then check records if available.

Ask one question at a time and follow the answer. A list is a question bank, not a speech to read at a customer.

Past behavior is often stronger than hypothetical preference because it includes real constraints. “I would use full automation” costs the person nothing to say. Seeing them reject an automatic change on a live project reveals concerns they may not mention in a general discussion.

Past reports still have limits. Memory is imperfect, and one dramatic event may not be common. When permitted, inspect a safe example, observe a task, or compare activity records. Do not assume the artifact proves every part of the person's explanation.

### 4.4 Avoid leading the witness

“Would a more accurate AI make you happier?” encourages agreement and supplies the explanation. A stronger question is “What made the last suggestion useful or difficult to use?”

“Why did you stop using the feature?” assumes they stopped. First establish whether they used it again and whether they had another relevant task. A weekly testing job should not be judged by daily return behavior.

Do not sell while trying to learn. If the person asks for a feature, explore the need respectfully: “I can see why that might help. Could we walk through the last time you needed it?” The aim is understanding, not winning an argument about their request.

### 4.5 JTBD and personas

**JTBD**, or jobs-to-be-done, describes the progress someone wants in a situation. A simple pattern is:

> When [situation], I want [progress], so I can [outcome].

For QA: “Before a release, I want to separate real product defects from unreliable checks, so I can give a defensible release recommendation.”

For food delivery: “During a short lunch break, I want a meal that arrives within my available time, so I can eat without missing work.”

The job should survive a change in solution. “I want an AI button” does not describe the deeper progress. The person could use manual investigation, deterministic tools, or AI to achieve the job.

A **persona** is an evidence-based description of a meaningful user group. An illustrative persona might be a QA engineer maintaining a shared regression suite, with limited write permission and a release deadline. The useful details are workload, skills, responsibilities, and constraints. Age or hobbies usually add little to this case.

An invented persona can help explore a scenario, but label it illustrative. It is not customer research.

### 4.6 Map handoffs and select a useful sample

**P1 — SHOULD KNOW**

Map trigger → actions → tools → handoffs → decision → outcome. Ask where work waits and where context is lost. Faster test generation will not solve a requirement approval queue.

Compare groups that can distinguish explanations: successful repeat users, first users who did not return despite another task, and people using an alternative workflow. Include different project types if you think context matters.

Several interviews can uncover a mechanism. They cannot establish that a specific percentage of the entire market has it. Use quantitative evidence to estimate prevalence when the decision requires it.

Contradictory requests can reveal different segments. A small isolated project may tolerate unattended edits; a shared release-critical project may need review. Ask what differs before averaging the requests into one confusing feature.

**Check yourself:** A QA lead requests “more trust.” What recent behavior would you investigate before adding explanations or confidence scores?

## Part 5: Hypotheses and evidence

**P0 — MUST KNOW**

### 5.1 What a hypothesis is

A hypothesis is a claim you can investigate through predicted observations. It can explain a symptom or predict an intervention's effect.

**Explanatory hypothesis:** Missing project conventions cause users to spend too long editing generated tests.

**Intervention hypothesis:** Supplying an approved project template will reduce convention-related edits and total task time without increasing incorrect assertions.

Both need evidence. The second depends partly on the first, but proving the problem exists does not prove that your particular solution works.

Compare five statements:

- **Assumption:** “All testers have another test-generation task each week.” We are using this as a premise, but have not checked it.
- **Opinion:** “The feature feels too complicated.” This is a judgment that needs explanation and context.
- **Hypothesis:** “Users abandon setup because the required project connection is unclear.” We can observe setup and compare failures.
- **Fact within an illustrative dataset:** “Eight of twenty observed setup attempts stopped at project connection.” This describes that sample, not the entire user base.
- **Solution:** “Add connection guidance.” This is a proposed action, not evidence of its own value.

### 5.2 Generate competing explanations

For low AI repeat use, consider mechanisms across the workflow:

1. **Poor output quality:** The output is wrong or misses important checks.
2. **Irrelevant use case:** The feature solves a rare or low-value task.
3. **Missing context:** The model lacks project rules, current requirements, or data conventions.
4. **High review effort:** Checking and correcting takes too much work.
5. **Low trust:** Users cannot judge whether output is safe or remember costly errors.
6. **Slow latency:** Users wait too long and return to their previous method.
7. **Workflow mismatch:** Copying, exporting, or obtaining permissions interrupts the real task.

These can interact. Missing context can cause errors, which increase review time and reduce trust. Avoid treating a list as seven independent causes when some form a chain.

### 5.3 Ask for evidence that separates explanations

If **quality** is the issue, you may see wrong expected results in expert review. If **conventions** are the issue, the underlying assertions may be correct but require predictable formatting or setup changes. Classify edits instead of counting them alone.

If **latency** is the issue, abandonment may cluster during long waits. That association is not enough: harder tasks may be both slower and less successful. Compare similar tasks or test a latency improvement while checking quality.

If **task frequency** is the issue, successful users may have no reason to return during the measured window. Ask when their next eligible task occurred. Do not silently exclude inconvenient users to make retention look better; define eligibility consistently and report the broader population too.

If **trust** is the issue, observe the verification behavior. Do people inspect every detail because prior output was wrong, because sources are missing, or because their role requires review regardless of model quality? Each explanation implies a different product response.

### 5.4 Qualitative and quantitative evidence

**Qualitative evidence** explains experiences and mechanisms. Examples include task observation, interview accounts, support conversations, and annotated failed tests.

**Quantitative evidence** measures counts, rates, distributions, and changes. Examples include setup completion, total task duration, cancellation by stage, and repeat usage by cohort.

Use them together. Interviews may suggest that restaurant tablets miss order notifications. Logs can test whether acknowledgement delays increased on the affected devices. The logs locate the pattern; observation can show why it occurs.

Evidence quality depends on relevance, reliability, and comparison. A large sample of the wrong users may be less useful than a small sample closely matching the decision. A small relevant sample still has uncertainty about prevalence.

### 5.5 Correlation, causation and “What would change my mind?”

**Correlation** means two things move together. **Causation** means changing one contributes to changing the other.

Drivers who receive incentives may complete more orders. Perhaps incentives helped. Perhaps the platform targeted already busy districts. Demand could cause both higher incentives and more orders. This alternative influence is a **confounder**.

A **counterfactual** is what would have happened without the intervention. You cannot observe both versions for the same person at the same moment, so you need a credible comparison. Random assignment can help, but the experiment must still handle measurement errors, shared capacity, and sufficient observation time.

Ask before investigation: “What result would make my leading explanation less likely?” If you blame missing context, correct output with low review effort would push you toward task relevance or workflow access. If no imaginable evidence changes your view, you are defending an opinion rather than testing a hypothesis.

### 5.6 Choose a validation method for the uncertainty

**P1 — SHOULD KNOW**

- **Problem uncertainty:** Observe recent tasks and consequences. Do people actually struggle?
- **Usability uncertainty:** Give a prototype and a realistic task. Can people use it without coaching?
- **Technical feasibility uncertainty:** Ask engineers to investigate the hardest technical dependency or test a limited approach.
- **Impact uncertainty:** Compare outcomes with a credible baseline or controlled rollout.
- **Safety and reliability uncertainty:** Evaluate realistic failure cases and rare severe errors before increasing exposure.

A prototype showing that users understand a button does not prove it improves retention. A model benchmark does not prove an enterprise will approve the workflow. Match the evidence to the claim.

**Check yourself:** What evidence would distinguish “users distrust accurate output” from “users correctly notice poor output”?

## Part 6: Metrics from zero

**P0 — MUST KNOW**

A metric is a defined measurement. A goal says where you want to go; metrics help you observe progress and understand mechanisms. “Make lunch more reliable” is a goal. “Share of completed orders arriving within the promised window” is a possible metric, with definitions still needed.

### 6.1 Metric roles

An **output metric** measures a result. Completed orders and successful testing tasks are outputs. An **input metric** measures an activity or condition that can influence the result, such as accurate merchant availability or successful project setup. An input's causal influence is a hypothesis to validate.

A **leading indicator** gives an earlier signal of a later outcome. Successful first-task completion may help predict later use. A **lagging indicator** reports an outcome after the process, such as renewal or monthly retention. Leading does not mean guaranteed, and lagging does not mean unimportant.

A **primary metric** is the main outcome used to judge a specific decision. A **supporting metric** helps explain the result. A **guardrail metric** detects important harm while pursuing the primary outcome.

**ILLUSTRATIVE EXAMPLE — A food promotion:** Completed orders are primary. Checkout conversion and order attempts support diagnosis. Cancellation rate and contribution may be guardrails because growth is less useful if deliveries fail or the subsidy exceeds the intended budget.

**ILLUSTRATIVE EXAMPLE — AI test creation:** Successful useful tests per eligible task can be primary. Generation completion, edit categories, and review time support diagnosis. Incorrect assertions and missed critical defects can be guardrails.

A **vanity metric** looks impressive but gives weak evidence of value in context. Total generations can rise because people retry failed output. The same count can still be useful for capacity planning. A metric's role depends on the question.

These categories overlap. Merchant acceptance may be a supporting input metric in an order-growth experiment and the primary metric in a notification-reliability test. Do not memorize one fixed category for every term.

### 6.2 Define the metric before discussing the number

Specify **population, event, denominator, time window, and comparison**.

“AI repeat use is 30%” is incomplete. Does that mean any second click among all sign-ups, or a useful second task among first-time successful users who had another task within fourteen days? These measures answer different questions.

For cancellations, ask whether the denominator is placed orders, accepted orders, assigned orders, or driver assignment offers. A driver cancelling one assignment does not always cancel the buyer's order; another driver might complete it.

**ILLUSTRATIVE EXAMPLE:** 100 cancelled orders out of 1,000 placed orders is 10%. If a report uses 800 merchant-accepted orders as the denominator, the same count becomes 12.5%. Before debating why the rate changed, align what it measures.

Compare like with like: same status definition, time zone, attribution rule, and reporting maturity. Orders placed near midnight may complete on the next day. A recent cohort may not have had a full return window yet.

### 6.3 Funnels locate the stage where opportunities are lost

A **funnel** tracks progress through defined stages. Food delivery might use eligible session → menu view → checkout start → order placed → order completed.

Counts tell you where volume changes. Rates tell you how efficiently one stage becomes the next. Both matter. Conversion can improve while orders fall if traffic falls more sharply.

**ILLUSTRATIVE EXAMPLE:** Last week, 10,000 eligible sessions produced 2,000 placed orders: 20% session conversion. This week, 8,000 sessions produced 1,760 placed orders: 22% conversion. Conversion rose, but placed orders fell 12% because the traffic loss was larger.

Do not treat this as proof of why traffic fell. The funnel locates the change. You still need hypotheses about acquisition, seasonality, availability, or measurement.

### 6.4 Metric trees: a way to decompose an outcome

A **metric tree** connects an outcome to smaller components. Some links are arithmetic identities. Other links are hypothesized causal influences. Keep the distinction clear.

**A compatible session-based identity:**

Placed orders = eligible sessions × orders per eligible session.

Completed orders = placed orders × completion rate.

If at most one order is attributed to each eligible session, orders per session equals session-to-order conversion. If multiple orders can occur in a session, a simple converted-session percentage does not capture order count on its own.

**A compatible buyer-based identity:**

Placed orders = ordering buyers × average placed orders per ordering buyer in the period.

You can expand ordering buyers into eligible people × share who order, provided the population and period match. Then order frequency is orders per ordering buyer.

You may hear “orders = traffic × conversion × frequency.” That works only with definitions that avoid overlap, such as distinct eligible people × share becoming ordering buyers × orders per ordering buyer. If traffic means sessions and conversion already measures orders per session, multiplying by frequency again double-counts behavior.

**An AI task tree:**

Useful completed tasks = eligible tasks × share attempted with AI × share of AI attempts completed usefully.

This requires a consistent task definition and treatment of retries. Five generations for one task should not become five successful user outcomes.

Below these arithmetic branches, show causal hypotheses: missing context → corrections → longer review → abandonment. The arrows explain possible mechanisms; they are not multiplication formulas.

### 6.5 Movement → decomposition → segmentation → hypotheses

First define the changed outcome. Then break it into components. Then compare groups where mechanisms might differ.

**Katalon example:** Useful task completion fell. Setup completion stayed stable, but review abandonment rose. The change is concentrated in projects using custom conventions. Missing context becomes a stronger hypothesis; it is not yet proven.

**ShopeeFood example:** Completed orders fell. Placed orders stayed stable, while completion fell in one district at lunch. Inspect acceptance, assignment, pickup, delivery, and cancellation reasons within that segment.

Useful segments include geography, time, new versus existing users, app version, merchant type, task type, project complexity, and permission level. Choose a segment because it might reveal a mechanism, not because it appears on a standard checklist.

### 6.6 Averages, distributions and percentage points

**P1 — SHOULD KNOW**

An average can hide a bad tail. Two districts with delivery times of 20 and 60 minutes have an average of 40 minutes if their order counts are equal. That average describes neither district well.

A **percentile** describes a position in a distribution. A p90 delivery time of 50 minutes means roughly 90% of the measured deliveries took 50 minutes or less. Inspecting the tail helps detect severe delays. The exact value still depends on the measured population, including whether cancellations were excluded.

If conversion falls from 20% to 16%, it drops **4 percentage points** and **20% relatively**. Relative change is the 4-point difference divided by the original 20%. State which one you mean.

Averages can also change because the mix changes. If a platform gets more long-distance orders, average delivery time can rise even when each distance segment stays stable. Compare within segments and inspect their weights.

### 6.7 Metrics should resist easy gaming

Any measure can become misleading when optimized alone. A team can improve test pass rate by deleting strong assertions. A merchant can raise acceptance by accepting orders it cannot prepare. A platform can shorten quoted ETA while making actual lateness worse.

Ask: “Can this metric improve while the real outcome worsens?” If yes, add a companion measure or change the primary metric. More metrics are not automatically better; each should protect a specific decision.

**Check yourself:** A test-generation feature doubles generations and halves time per generation. What evidence is still missing before claiming that testers save time?

**Audio recap — Metrics:** A metric is a measuring tool, so define what it measures. Ten percent cancellation means little until you know ten percent of what. Break an outcome into compatible parts, then compare meaningful segments. The common mistake is treating a rising activity count as proof of value. Ask whether the number can improve while the user's job becomes harder.

## Part 7: Trade-offs and decision making

**P0 — MUST KNOW**

A trade-off exists when improving one outcome consumes a resource or risks another outcome. Good product judgment makes that cost visible and chooses deliberately.

### 7.1 Common trade-offs and their mechanisms

- **Speed versus reliability:** Skipping review can shorten a workflow but allow incorrect test changes into shared assets.
- **Automation versus control:** Automatic actions reduce interruptions but may exceed what users intended to authorize.
- **Growth versus profitability:** Discounts can increase orders while reducing contribution through subsidy.
- **Marketplace liquidity versus quality:** Easier merchant entry may expand choice while introducing unreliable menus or preparation.
- **Personalization versus privacy:** More project context can improve output, but access must respect project and customer boundaries.
- **AI quality versus latency and cost:** A more capable approach may improve difficult outputs while adding waiting, tool calls, and cost.

These are not permanent laws that one side must always worsen. Better design can improve both. For example, a clearer review interface may improve review speed and correctness. Still, ask what resources or residual risks remain.

### 7.2 Communicate a conditional recommendation

Use the pattern:

> This improves X, but risks Y. I would choose A if condition Z is true.

**ILLUSTRATIVE EXAMPLE:** “Automatic locator updates could reduce maintenance, but they risk pointing tests at the wrong element. I would start with isolated drafts if we cannot reliably verify that the test's meaning stays unchanged.”

**ILLUSTRATIVE EXAMPLE:** “Lunch incentives could improve assignment time, but they may move drivers from nearby areas. I would test them if driver availability is the constraint and monitor the neighboring zones.”

The condition should be observable. “If the idea is good” is not helpful. “If pickup wait is stable but unassigned order time has risen” is more useful.

### 7.3 Prioritization without hiding judgment inside a score

**P1 — SHOULD KNOW**

Prioritization means choosing the best use of limited resources. Consider problem impact, people affected, frequency, evidence strength, effort, risk, dependencies, and opportunity cost.

**Opportunity cost** is what you give up by choosing an option. A week spent building a full agent is a week unavailable for fixing setup friction.

**ILLUSTRATIVE EXAMPLE:** A team can improve project templates or build unattended repair. Template mismatch is repeatedly observed; unattended repair's user benefit is uncertain. A template trial may deserve priority because it addresses stronger evidence with less exposure and effort. If diagnosis later shows templates are irrelevant and approval delays dominate, the ranking can change.

Named scores such as RICE can organize reach, impact, confidence, and effort. They do not make uncertain estimates true. You should be able to explain the choice without the acronym.

### 7.4 Make the next step concrete

A useful recommendation specifies a target segment, action, owner or collaborating team, comparison, important guardrail, and change criterion.

For a hypothetical preparation-delay problem: work with operations and a small group of overloaded merchants to test more accurate availability and capacity settings. Compare comparable lunch periods. Track completed orders and pickup wait, while checking merchant receipts and buyer selection. Revisit the approach if delays stay unchanged or the lost selection causes greater abandonment.

That is concrete enough to discuss feasibility. It does not claim the experiment has already worked.

### 7.5 Act with incomplete information

If harm is immediate, separate mitigation from long-term diagnosis. A checkout outage may justify rolling back a recent release while investigating. A suspected automatic repair that hides defects may justify pausing that action class while preserving evidence.

For a reversible, limited action, you can often learn through a small trial. For an irreversible action with severe consequences, you need stronger evidence and control. There is no universal percentage of certainty required for every decision.

**Check yourself:** What would make you choose better preparation estimates over more driver incentives when both appear capable of reducing ETA?

## Part 8: Software testing for a PM

**P0 — MUST KNOW**

Testing creates evidence about whether software behaves as intended and where release risk remains. It cannot establish that every possible behavior is correct. A PM needs to understand the tester's job well enough to choose useful product improvements.

### 8.1 One running example: e-commerce checkout

Throughout this part, use this **ILLUSTRATIVE EXAMPLE**:

Browse product → add to cart → checkout → payment → confirmation.

Suppose the agreed requirements say an expired coupon must not reduce the price, successful payment must create one confirmed order, and a payment failure must not show a successful confirmation. These are invented teaching requirements.

A **test case** describes conditions, actions or inputs, and expected results. Example: with an expired coupon in the cart, submit checkout; expect an error explaining the coupon and no expired discount applied.

A **test suite** is a group of test cases organized for a purpose. A checkout regression suite could include expired coupons, valid payments, failed payments, and duplicate submissions.

An **assertion** is the specific check of an expected result. “The order total remains 100,000 VND” is stronger than merely opening the checkout page when the requirement concerns a discount.

A **bug** or **defect** is a flaw. The two words are often used interchangeably. A **test failure** means an observed result did not satisfy a test expectation or the test could not complete. It is a signal to investigate, not automatic proof of a product defect.

**QA**, or quality assurance, concerns practices that help a team produce quality software. Testing is part of this work. Clear requirements, risk discussion, and preventing repeated mistakes also contribute. QA is not simply “the team that finds bugs after development.”

### 8.2 Manual and automated testing

**Manual testing** uses a person to perform checks or explore behavior. A tester might notice that a payment error message is confusing and hides the next action. Human exploration is valuable when the right behavior or likely failure is still unclear.

**Automated testing** uses software to run checks and compare results. An automated test can repeatedly verify that an expired coupon never lowers the total.

Automation has setup, execution, diagnosis, and maintenance costs. A stable, frequently repeated permission check may be a good early candidate. A new experience with unclear requirements may first need human exploration.

Neither mode guarantees quality. An automated weak assertion is still weak. Manual testing can also overlook an important condition. Choose the method according to risk, repetition, clarity, and cost.

### 8.3 Unit, integration, API, UI and end-to-end testing

These categories describe different dimensions. **Unit, integration, and end-to-end** mainly describe scope. **API and UI** describe the interface used. They can overlap.

- **Unit testing:** Checks a small part in isolation. Test the function that calculates whether a coupon is expired. It is narrow and helps locate a fault, but cannot prove the whole checkout journey works.
- **Integration testing:** Checks parts working together. Verify that the order service passes the correct amount to a payment adapter and handles its failure response.
- **API testing:** Interacts through a programmatic interface. Send an order request and check status, totals, permissions, and effects. An API test can also be an integration test.
- **UI testing:** Interacts through the visible interface. Check that the buyer sees the expired-coupon message and can change the coupon. A UI test may cover one screen without being end-to-end.
- **End-to-end testing, or E2E:** Checks a complete journey across components. Browse, add to cart, pay in a controlled environment, and verify confirmation and order state.

Narrow tests can fail quickly and explain a local fault. Broader tests show whether the journey works together but often involve more dependencies and diagnosis effort. The mix should reflect product risks. Do not infer release confidence from the count at one level alone.

### 8.4 Regression, maintenance, coverage and CI/CD

**Regression testing** checks whether a change broke behavior that previously worked. After changing coupon logic, rerun important payment and order checks as well as coupon checks. Regression testing can be manual or automated.

**Test maintenance** keeps tests aligned with intended behavior, interfaces, data, and environments. If the requirement intentionally changes, a test may need updating. If the product violates an unchanged requirement, the product needs fixing. Maintenance should preserve the reason the test exists.

A **flaky test** produces inconsistent results under apparently unchanged relevant conditions. Hidden timing, shared state, network behavior, or data can still vary. A checkout test might click before a button is ready, passing on one run and failing on another. Investigate the cause; repeated reruns do not prove the product is safe.

**Test coverage** describes what the tests exercise or check. Code coverage measures executed code, while requirement or risk coverage concerns expected behaviors and risks. Executing payment code does not prove a test checks duplicate charging. A coverage percentage without its definition is incomplete.

**Continuous integration, or CI,** frequently integrates changes and runs checks. In this example, a proposed checkout change triggers selected automated tests and produces results for review.

**CD** can mean continuous delivery, which keeps software ready for release, or continuous deployment, which automatically releases passing changes under a team's process. Clarify which meaning applies. A green CI report is evidence from those checks, not proof that all users will have a correct experience.

### 8.5 The QA workflow, stage by stage

**Requirement → understand expected behavior → design tests → create tests → execute → capture failure → investigate → diagnose → fix → regression → release confidence.**

This is a learning map, not a rigid sequence. Successful runs may skip failure diagnosis. Discoveries can send the team back to requirements. The opportunities below are hypothetical product ideas, not claims about Katalon's implemented features.

#### Stage 1: Gather the requirement

- **QA job:** Identify what checkout is supposed to do and whose decision defines it.
- **Pain:** Requirements are scattered across tickets, conversations, and old documents.
- **Deterministic automation opportunity:** Link the requirement ID and version to affected tests; flag missing required fields.
- **AI opportunity:** Summarize relevant documents and identify conflicting statements.
- **AI risk:** An invented rule becomes a convincing summary that nobody actually approved.

For example, “expired coupon is invalid” does not establish whether checkout should block entirely or allow payment without the discount.

#### Stage 2: Understand expected behavior

- **QA job:** Resolve ambiguity and turn intent into observable expected results.
- **Pain:** Product, engineering, and support may interpret the same requirement differently.
- **Deterministic automation opportunity:** Require explicit acceptance criteria and an owner for unresolved questions.
- **AI opportunity:** Suggest clarification questions and examples of ambiguous behavior.
- **AI risk:** Quietly choosing a business rule instead of marking it unresolved.

For example, a payment timeout may mean failure or uncertain completion. The expected recovery behavior must be agreed, not guessed.

#### Stage 3: Design tests

- **QA job:** Select normal, boundary, negative, and high-risk scenarios.
- **Pain:** Time is limited, so important edge cases may be missed while easy cases multiply.
- **Deterministic automation opportunity:** Apply known boundary templates and check requirement-to-test links.
- **AI opportunity:** Suggest plausible scenarios, such as double-clicking payment or retrying after timeout.
- **AI risk:** Producing many shallow scenarios while missing duplicate charging or authorization failures.

The PM question is which risks matter most, not how many scenarios can be generated.

#### Stage 4: Create tests

- **QA job:** Write usable manual steps or automated checks with data, setup, and meaningful assertions.
- **Pain:** Locators, test accounts, framework conventions, and setup create repetitive work.
- **Deterministic automation opportunity:** Reuse approved fixtures, templates, selectors, and data builders.
- **AI opportunity:** Draft tests from verified requirements and project examples.
- **AI risk:** Inventing APIs, selecting the wrong element, using inappropriate data, or checking only that a page opens.

An executable checkout test still needs to verify the correct charge and order state.

#### Stage 5: Execute

- **QA job:** Run the right checks against the intended build and environment.
- **Pain:** Slow suites, unavailable environments, credentials, and unstable dependencies block work.
- **Deterministic automation opportunity:** Schedule CI runs, validate configuration, and collect structured results.
- **AI opportunity:** Help select relevant checks or coordinate permitted execution when the next step varies.
- **AI risk:** Running against the wrong environment, repeating expensive operations, or saying “completed” before checking results.

For example, payment tests should use the agreed controlled setup. The environment is part of the task's meaning.

#### Stage 6: Capture a failure

- **QA job:** Preserve what failed, when, against which build, with enough context to investigate.
- **Pain:** Alerts lack screenshots, request IDs, test data, or relevant logs.
- **Deterministic automation opportunity:** Attach timestamps, logs, screenshots, and environment identifiers automatically.
- **AI opportunity:** Summarize the failure and group similar symptoms.
- **AI risk:** Dropping a rare but serious failure because it looks unlike the main cluster.

Do not replace the underlying evidence with the summary. The summary is an interpretation.

#### Stage 7: Investigate

- **QA job:** Collect evidence that separates product, test, data, environment, and dependency explanations.
- **Pain:** Relevant information is spread across CI, code changes, test assets, and external services.
- **Deterministic automation opportunity:** Correlate known identifiers and show changes since the last comparable run.
- **AI opportunity:** Propose the next evidence source and compare patterns across artifacts.
- **AI risk:** Reading unrelated projects, assuming a recent code change caused the failure, or chasing an unbounded loop of tool calls.

If payment failed, inspect the response and environment before changing the assertion.

#### Stage 8: Diagnose

- **QA job:** Choose the best-supported explanation and state remaining uncertainty.
- **Pain:** Several causes produce the same visible symptom; intermittent problems are difficult to reproduce.
- **Deterministic automation opportunity:** Recognize established error signatures and separate known infrastructure failures.
- **AI opportunity:** Rank explanations and point to evidence for each.
- **AI risk:** Presenting a plausible narrative as confirmed root cause or expressing unsupported confidence.

“The payment provider timed out in these logs” is more defensible than “the provider caused all checkout failures” without broader evidence.

#### Stage 9: Fix the right thing

- **QA job:** Route or make the appropriate correction and verify its scope.
- **Pain:** Ownership is unclear, and a small fix may affect other behavior.
- **Deterministic automation opportunity:** Create a change request with linked evidence and enforce review rules.
- **AI opportunity:** Prepare a bounded patch or draft a defect report.
- **AI risk:** Changing expected behavior to match a broken application, weakening an assertion, or overwriting another person's work.

If checkout charges twice, weakening the test to accept two charges is not a successful repair.

#### Stage 10: Run regression checks

- **QA job:** Confirm the fix and check important neighboring behavior.
- **Pain:** Full suites can be slow; narrow reruns can miss related regressions.
- **Deterministic automation opportunity:** Run affected suites and track unresolved failures.
- **AI opportunity:** Suggest additional risk-relevant checks based on the change.
- **AI risk:** Skipping essential checks because the model incorrectly judges them irrelevant.

After fixing duplicate payment, include retries and failed-payment recovery, not only one successful purchase.

#### Stage 11: Support release confidence

- **QA job:** Explain tested behavior, unresolved defects, coverage gaps, and residual risk to the release decision-maker.
- **Pain:** Reports can be large, inconsistent, or reduced to an unhelpful pass percentage.
- **Deterministic automation opportunity:** Aggregate verified results, link unresolved issues, and show required checks.
- **AI opportunity:** Draft an evidence-linked summary for different stakeholders.
- **AI risk:** Hiding limitations, overstating certainty, or treating release authorization as implied by a green report.

The goal is a defensible decision about risk. “All selected checks passed, but retry behavior was not tested” communicates more than “quality is excellent.”

### 8.6 Test failure diagnosis: six different explanations

**Real application defect:** The requirement says one charge; the application creates two. Fix the application and retain the check that exposed it.

**Broken or outdated test:** An approved UI change renamed the payment button, but the test still uses the old locator. Update the locator while preserving the intended payment assertion.

**Environment issue:** The test environment cannot reach its configured service. Restore or correct the environment; do not change the business expectation to accept unavailable payment.

**Flaky behavior:** The test sometimes reads confirmation before the page finishes updating. Improve synchronization after establishing the cause. Also investigate whether the intermittent behavior exposes a real product timing problem.

**Bad test data:** A supposed “new customer” account already has an order, so a first-order coupon does not apply. Correct the setup or expectation for that data.

**Dependency issue:** A payment sandbox has an outage or returns unexpected errors. Capture the dependency failure and evaluate whether the application handles it correctly. A dependency incident and an application error-handling defect can coexist.

These categories can overlap. The purpose is to ask better questions, not force every failure into exactly one box.

### 8.7 What an AI testing feature should earn

An AI-generated test should be relevant, executable, meaningful, maintainable, and safe to use in context. Test execution is one requirement. Correct assertions and risk coverage are separate requirements.

Useful evaluation includes known defects and non-defective cases. Does the test catch the intended defect? Does it raise false alarms on correct behavior? Does a proposed repair preserve that ability? Include total human effort to review and maintain it.

**Check yourself:** A repair agent achieves a 99% post-repair pass rate in a hypothetical evaluation. What evidence would reveal whether it is fixing tests or removing their ability to catch defects?

**Audio recap — Testing:** Imagine a checkout test turning green because someone removed the duplicate-charge check. The report improved, but the buyer became less protected. A test failure is evidence that needs diagnosis. It may come from the application, test, data, environment, or dependency. Ask what the test was supposed to prove and whether that meaning survived the repair.

## Part 9: AI fundamentals for a PM

**P0 — MUST KNOW**

### 9.1 AI, machine learning and LLMs

**Artificial intelligence, or AI,** is the broad field of building systems that perform tasks associated with intelligence, such as recognizing patterns, understanding language, or planning actions.

**Machine learning, or ML,** is an approach in which a system learns patterns from data rather than having every behavior explicitly written as a rule. A delivery-time prediction model could learn relationships among distance, time, weather, and observed trip duration.

A **large language model, or LLM,** is a machine-learning model trained on large amounts of data to work with and generate token sequences. It can be useful for language, code, summarization, and reasoning tasks. Its fluency does not establish factual correctness.

The relationship is broad to specific: AI includes ML; LLMs are one kind of ML model. Not every AI product needs an LLM. Predicting an ETA from structured signals may use predictive models. Checking whether an order ID is missing can use a simple rule. Explaining a messy failure report may benefit from an LLM.

### 9.2 Tokens and the context window

A **token** is a unit a model processes, often a word or part of a word in text. Token count affects how much input and output a system can handle, and can influence cost and latency. One token does not always equal one word; language and content affect the count.

The **context window** is the bounded material available to the model during a call, subject to the model's limits. Think of it as a working desk. The model can work with the papers on that desk, but it does not automatically have every file in the office.

For test generation, the desk may contain the requirement, relevant test examples, project conventions, and recent failure evidence. A missing rule can cause a wrong test. Too much unrelated material can also make the relevant evidence harder to use.

Do not assume that a long conversation guarantees reliable memory of every detail. Stored information must still be selected and supplied when needed. The product should handle missing context explicitly.

### 9.3 Prompts, hallucination and grounding

A **prompt** provides instructions, task information, examples, or constraints to the model. A useful prompt says what outcome is needed, what evidence to use, and how to handle uncertainty.

**ILLUSTRATIVE EXAMPLE:** “Draft checkout tests from the supplied requirement and project examples. Identify missing rules. Do not invent expected behavior. Explain which requirement each assertion checks.”

A **hallucination** is plausible output that is false or unsupported by the relevant evidence. The model might invent a payment API or state that a coupon rule exists when no supplied requirement says so.

**Grounding** means connecting the answer to relevant evidence. Showing the source requirement makes verification easier, but a citation can still be irrelevant, stale, or misinterpreted. Check whether the source supports the claim.

Better prompting may improve a task. It cannot solve an irrelevant user problem, create missing permissions, or replace product-level enforcement of action boundaries.

### 9.4 Confidence is not correctness

A model saying “I am 95% confident” does not automatically mean it is correct 95% of the time. Fluent wording, output probability, and factual truth are different things.

**Calibration** means that confidence estimates match observed correctness across comparable cases. To trust a confidence score as a probability, you need evidence that it is calibrated for that task and population.

**ILLUSTRATIVE EXAMPLE:** A test-repair assistant confidently identifies a locator problem. The current requirement and screenshot may show that the button should be absent. Direct evidence matters more than confident wording.

For high-impact decisions, ask whether the output can be checked independently and what happens when the model is wrong. Do not use a self-reported score as the only permission to execute.

### 9.5 Structured output

**Structured output** follows a defined shape, such as fields for diagnosis, evidence, proposed change, and unresolved questions. This helps software and people use the result consistently.

For example, a failure report could require a category, cited artifact IDs, suggested next step, and an uncertainty field. The application can check whether required fields exist and whether values use an allowed format.

Correct structure does not prove correct content. A perfectly formatted report can identify the wrong project or invent a cause. Shape validation and task validation are separate checks.

**Check yourself:** If a model returns a valid structured response with a confident diagnosis, what still needs verification before changing the test?

## Part 10: RAG, tools, agents and MCP

**P0 — MUST KNOW**, with optional depth clearly marked below.

### 10.1 One continuous testing example

**ILLUSTRATIVE EXAMPLE:** A QA engineer asks an assistant to investigate failed checkout test T-42. The requirement is in Jira, test assets are in a testing project, application code is in GitHub, and execution evidence is in CI.

The requirement says a failed payment must not show confirmation. The test failed after a recent change. The correct next action is unknown: inspect evidence, report an application defect, update an outdated test, or investigate the environment.

These system names describe an imagined workflow. T-42 is a teaching identifier. This is not a claim that the candidate or Katalon implemented the specific integration.

### 10.2 LLM alone: general knowledge without private project evidence

Given only “T-42 failed,” an LLM can explain common failure categories and suggest questions. It cannot reliably know the current Jira requirement, private code, exact CI run, or project permissions unless the application supplies or retrieves them.

It may generate a plausible explanation anyway. A good product should encourage an explicit missing-information response. “I need the expected behavior and run evidence” is more useful than an invented root cause.

### 10.3 Context: putting relevant evidence on the desk

Supply the current requirement, the failing assertion, the relevant response, and the matching build identifier. The model can now compare expected and observed behavior.

Context needs **relevance, freshness, identity, and permission**. Logs from a different build may mislead. A similar test in another customer's project may be unauthorized and inappropriate. A project convention from last year may no longer apply.

More context is useful when it adds decisive evidence. It is wasteful when it adds noise or exposes unrelated data. The PM question is what the task needs, not how much text the system can collect.

### 10.4 RAG: retrieve relevant material before answering

**Retrieval-augmented generation, or RAG,** finds relevant source material and supplies it as context for generation. Retrieval means looking up useful information; it can use keyword search, semantic similarity, metadata, or a combination. RAG does not retrain the model each time. [Google Cloud's RAG overview](https://cloud.google.com/vertex-ai/generative-ai/docs/rag-engine/rag-overview)

In the T-42 example, retrieval might locate the linked requirement and the approved payment-retry convention. The assistant uses them to explain whether the observed behavior violates the requirement.

There are at least two separate failure points. Retrieval can return the wrong or stale material. Generation can misread good material. Evaluate both: did the system find the necessary evidence, and did the answer accurately use it?

If sources conflict, show the conflict and seek an authoritative clarification. Do not merge incompatible requirements into a new rule.

### 10.5 Tool calling: from text to an operation

With ordinary generation, the model produces content. With **tool calling**, it proposes an operation and arguments that the application can validate and execute.

For T-42, the proposed operation might be “read CI run R-17” or “retrieve the current requirement.” The model does not create access merely by naming the operation. The application must provide the tool, check permission and arguments, execute it, and return the result.

The sequence is:

**Choose operation → validate scope and inputs → execute allowed call → return result → interpret observed result.**

A tool can read information or change something. Reading a test and applying a test change have different consequences. Even reads can expose sensitive data; “read-only” is not the same as unrestricted.

If a write times out, completion is uncertain. The system should check the resulting state or operation status before retrying. Blind retries can duplicate actions. The assistant saying “done” is not evidence that the external system changed correctly.

### 10.6 Agent: choosing the next step from what happened

An **LLM-based agent** uses a model to choose actions as observations arrive. A helpful loop is:

**Goal → inspect context → choose action or tool → execute → observe → choose the next step → continue, ask, or stop.**

A predefined workflow follows a known sequence; an agent has more freedom to select its next step. This distinction follows [Anthropic's guidance on workflows and agents](https://www.anthropic.com/engineering/building-effective-agents). Product terminology varies.

In the T-42 example, a fixed process could always retrieve a run and format a report. An agent might inspect the requirement, notice that the error could be environmental, fetch environment health, and stop when the evidence is insufficient for a safe change. The value would come from choosing relevant investigation steps.

An agent does not need unlimited autonomy. It can investigate through permitted reads and still need a person to approve a write. Set stop conditions for missing access, conflicting evidence, repeated failures, excessive time, and actions outside scope.

### 10.7 Chatbot, workflow, agent and deterministic automation

A **chatbot** is a conversational interface. It can be a simple question-answer system or the interface to an agent. Chatbot and agent are not opposites.

A **workflow** is an organized sequence of steps. In this comparison, a fixed workflow has predefined routes and can include model calls. For example, always retrieve the requirement, ask an LLM for a summary, and show it for review.

**Deterministic automation** follows explicit rules for given inputs. A rule can reject a tool call with a missing project ID or run a known suite after a code change. It does not need an LLM to choose what to do.

An **agent** is useful when choosing the next action is part of the problem. If every task follows the same known sequence, a fixed workflow may be easier to verify and operate. Combining deterministic controls with flexible interpretation is often a sensible design hypothesis.

### 10.8 MCP: a common connection model

**Model Context Protocol, or MCP,** standardizes how AI applications exchange context and access exposed capabilities. The **host** is the AI application; its **client** communicates with an MCP **server**. The server exposes tools, resources such as data, or reusable prompt templates. It may run locally or remotely and may use underlying APIs. MCP does not define the application's reasoning strategy. [Official MCP architecture](https://modelcontextprotocol.io/docs/learn/architecture)

The basic relationship is:

**AI host → client → MCP server → exposed tools or resources → underlying systems.**

For the imagined T-42 investigation, an application could use connections to reach testing evidence and other authorized project material. A server supplies capabilities; it is not automatically the reasoning model. A product still needs to decide what the user can access and what actions require review.

The user benefit is potentially less manual copying between tools and a more reusable connection approach. That benefit should be tested against the actual workflow, connection quality, and maintenance cost.

### 10.9 MCP versus direct API integration

**P1 — SHOULD KNOW**

A **direct API integration** connects the application to a service through its specific interface. MCP can introduce a common interface for AI applications, while the server may still call that service's API underneath. They can coexist.

Consider the product decision across these dimensions:

| Dimension | Reason to consider MCP | Reason to consider direct APIs |
| --- | --- | --- |
| Integration scope | Several AI hosts or reusable capabilities may benefit from a shared model. | One narrow, stable integration may need little abstraction. |
| Control | Shared interfaces may simplify capability exposure. | A tailored integration can tightly shape behavior for one workflow. |
| Permissions | Common connection patterns may help organize access. | Existing service controls may already fit the application. Both require enforcement. |
| Maintenance | Reuse may reduce duplicated connection work. | Fewer layers may simplify debugging for a small scope. |
| Standardization | Valuable when compatible tools and clients are available. | Less valuable if the needed capability is poorly supported through the standard. |
| Security | Evaluate server trust, scope, and returned content. | Evaluate credentials, endpoint access, and returned content. Neither is automatically safe. |

These are **decision considerations**, not guaranteed advantages.

**ILLUSTRATIVE Katalon-track decision:** If customers work in several AI applications and need the same authorized testing evidence, reusable exposure may be valuable. If the immediate task is one tightly controlled internal CI check, a direct connection may be simpler. Compare required capabilities, reliable task completion, permissions, debugging effort, and total maintenance. “MCP is newer” is not a user benefit.

### 10.10 Fine-tuning and memory

**P2 — OPTIONAL DEPTH**

**Fine-tuning** further trains a model using selected examples to change aspects of its behavior. RAG supplies material during use. Fine-tuning might help with a repeated output style; retrieval is often relevant when the task needs current project facts. They can be combined, and neither guarantees correctness.

**Memory** is information stored across interactions. It must be selected and brought into current context to influence the next call. A remembered convention needs ownership, scope, freshness, and a way to correct it. Do not store an earlier model guess as a verified requirement.

**Check yourself:** In the T-42 scenario, which problem needs retrieval, which needs a tool, and which might justify an agent choosing the next step?

## Part 11: AI product judgment

**P0 — MUST KNOW**

The product question is whether the system helps a real user complete a valuable job at an acceptable cost and risk. More AI, a larger model, or more autonomy does not establish that value.

### 11.1 Ask why this amount of AI is needed

Move through these questions:

1. **Why AI?** What uncertainty or pattern cannot be handled well by simple rules?
2. **Why an LLM?** Does the task require interpreting language, code, or messy context?
3. **Why an agent?** Does the system need to choose changing next steps?
4. **What happens when it is wrong?** A poor suggestion and an incorrect external action have different costs.
5. **Can the result be verified?** What independent evidence establishes success?
6. **Can the action be reversed?** Does undo remove the consequences?
7. **Can people observe and control it?** Are scope, status, and recovery clear?
8. **Does it improve the whole job?** Include review, retries, waiting, and downstream errors.

**ILLUSTRATIVE EXAMPLE:** A rule can check whether a required test field is empty. An LLM may help interpret ambiguous requirement text. An agent may help investigate a failure whose next evidence source is unknown. Choosing the simplest adequate approach is product judgment.

### 11.2 Human-in-the-loop

**Human-in-the-loop** means a person participates at a meaningful decision point. They may provide missing context, approve a proposed change, correct an error, or handle an exception.

A useful review shows the exact proposed action, affected project, supporting evidence, important uncertainty, and expected consequences. “Allow AI to help?” is too broad to support an informed decision about changing shared tests.

Review also has costs. If every harmless step needs approval, the workflow becomes slow and users may approve automatically without reading. The design question is where human judgment adds value, and whether the reviewer has enough information and time to exercise it.

**ILLUSTRATIVE HYPOTHESIS:** Showing a clear assertion difference → easier verification → faster informed decisions → potentially greater use. If the view overwhelms users with irrelevant detail, it may instead increase abandonment. Test the task, not just whether people like the screen.

### 11.3 An intuitive autonomy spectrum

These are teaching levels, not an official industry or Katalon classification.

1. **AI suggests:** Gives an explanation or possible test. A person decides what to do. Useful when context or correctness is uncertain.
2. **AI prepares:** Creates a draft or proposed patch in a controlled space. Useful when reducing preparation effort without applying the final change.
3. **AI executes with approval:** Shows a concrete action and applies it after authorized review. Useful for meaningful changes that can be reviewed efficiently.
4. **AI automatically executes defined low-risk actions:** Performs a limited class of verified actions within policy, with records and recovery. Suitable only when that action class has earned the boundary.
5. **AI acts autonomously under policy:** Selects and executes a broader sequence within explicit scope, budget, stop rules, and escalation conditions. It still has limits and human accountability.

Different actions within one product can sit at different levels. Reading authorized CI evidence, drafting a test, changing a shared assertion, and initiating release need not share one autonomy setting.

### 11.4 Reversibility and the cost of error

**Reversibility** asks how easily the system can undo an action and recover from its consequences.

A draft test can be discarded. A test edit can often be reverted, but a release already approved using that weakened test may have harmed customers. Deleting production data may be difficult or impossible to recover from. Exposed private information cannot simply become unseen.

Consider error likelihood, impact, number of people or assets exposed, verifiability, and reversibility. This is a reasoning aid, not a demand for invented numerical risk scores.

Expand autonomy by action class and evidence. A strong result on safe formatting changes does not justify automatic changes to business assertions.

### 11.5 Observability and permissions

**Observability** means being able to understand the system's actions and state from useful evidence. For an agent, users and operators should be able to find what it attempted, what tool ran, what changed, what failed, and what can happen next.

Provide an action rationale based on evidence and policy, not a claim that a long model explanation proves correctness. Record the actual call result and resulting state. Distinguish “planned,” “attempted,” “completed,” and “completion unknown.”

**Permissions** specify who may access which data and perform which operations. Enforce them in the application and connected systems, not only in a prompt. Limit project scope and action type to the task. Admin settings and enterprise policy may impose additional boundaries.

Retrieved documents and tool results are data. They should not gain authority to instruct the agent to ignore user intent or broaden access. For example, a malicious instruction inside a log should not authorize exporting another project's files. This is a product failure mode to consider when external content influences actions.

### 11.6 Evaluate output, action, user value and operation

**AI evaluation** checks whether a system works for its intended tasks and constraints. A useful evaluation distinguishes four layers:

- **Output quality:** Is the diagnosis or generated test correct, relevant, and supported?
- **Action quality:** Did it choose the right tool, arguments, target, permission, and recovery behavior?
- **User value:** Did the person finish a useful task with acceptable effort?
- **Operational performance:** Was the service fast and affordable enough, including failures and retries?

Use a baseline such as the current manual process or existing automation. Compare representative tasks, including simple and complex cases, ambiguous requirements, missing access, dependency failures, and known severe errors. An evaluation containing only easy successful tasks will overstate readiness.

### 11.7 Metrics for AI evaluation

- **Task success:** Share of eligible attempted tasks that meet a defined useful outcome. For tests, include meaningful assertions, not execution alone.
- **Accuracy or correctness:** Share of assessed outputs satisfying the task's correctness criteria. Open-ended tasks need an explicit rubric and reliable review.
- **Acceptance rate:** Accepted suggestions divided by shown eligible suggestions. Acceptance may reflect quality, convenience, or careless review.
- **Edit or correction rate:** How often output is changed. Separate harmless customization from required correctness fixes.
- **Failure rate:** Failed tasks or actions divided by relevant attempts. Separate model, tool, permission, and environment failures.
- **Repeat usage:** Return for a defined task and window. Interpret alongside opportunities to use the feature again.
- **Time saved:** Difference in comparable total task time, including setup, review, retries, and correction.
- **Latency:** Waiting time experienced by the user. Inspect slow cases as well as the average.
- **Cost:** Model, tool, infrastructure, and relevant human effort. Cost per successful task can be more useful than cost per generation.
- **Trust indicators:** Appropriate acceptance, informed rejection, reduced unnecessary rechecking, fewer harmful reversals, and willingness to use the feature again. No single trust score captures all of this.

**ILLUSTRATIVE EXAMPLE:** The manual workflow takes 25 minutes per comparable successful task. AI generation takes 2 minutes, review takes 14, and setup plus correction takes 4. Total AI task time is 20 minutes, so the observed saving is 5 minutes for these tasks, not 23. Failed and abandoned tasks must also be considered before making a broader value claim.

### 11.8 Design a useful evaluation and rollout

Define the task and costly failures. Assemble representative examples with trusted requirements and expected outcomes. Use expert checks where needed, and avoid evaluating solely against the model's own answer.

Start with offline evaluation, where outputs and actions can be checked before broad exposure. Then trial a bounded workflow with appropriate users and monitor both successful and unsuccessful tasks. **Shadow mode** can let a system propose an action without applying it, enabling comparison with actual decisions.

Stop or narrow the action class if evaluation shows it can hide serious defects. A high average success rate should not cancel out an unacceptable severe failure. Expanding exposure requires evidence relevant to the new scope.

**P1 — SHOULD KNOW: error types.** A false positive signals a problem when the behavior is acceptable. A false negative misses a real problem. In a checkout test, a false alarm wastes investigation; missing duplicate charging can harm buyers. Their costs differ, so one combined accuracy number may hide the important trade-off.

**Check yourself:** A new model improves correctness but doubles waiting and increases abandonment. What comparison would tell you whether to offer it for all tasks, selected tasks, or no tasks yet?

**Audio recap — AI product judgment:** Picture an assistant preparing a change to a checkout test. Drafting it is one decision; applying it to a shared release suite is another. Ask why the task needs an LLM, why it needs an agent, and what happens if it is wrong. Confidence and usage do not prove value. Look for useful work completed, verified actions, appropriate control, and total effort saved.

## Part 12: Katalon product case mental models

**P0 — MUST KNOW**

All six scenarios are **ILLUSTRATIVE EXAMPLES**, not actual Katalon incidents or interview questions. These are investigation scaffolds. Try framing the problem before reading the rest of each scenario.

### Case A: High first use, low repeat use of generated tests

**Symptom:** Many people try generation once; few return within the reported window.

**Clarify:** What counts as first use and repeat use? Which users, projects, and tasks are eligible? Did non-returners have another test to create? Did they complete a useful first task?

**Breakdown:** Discovery → setup → generation → review → useful test → next eligible task → return. Distinguish failure to get value from lack of another occasion to use the feature.

**Possible hypotheses:** Poor assertions, missing project conventions, excessive review effort, slow response, difficult export, unavailable permissions, or a rare use case. High first use may reflect curiosity rather than demand.

**Distinguishing evidence:** Observe comparable tasks for returners and eligible non-returners. Classify edits and abandonment points. Compare total task time with the existing workflow. Inspect whether tests check meaningful requirements.

**Conditional action and trade-off:** If convention edits dominate and assertions are sound, test supplying approved examples. The chain is: better context → fewer repeated edits → less review effort → possibly more repeat value. The risk is spreading stale conventions or optimizing a narrow segment. If users lack another task, change the interpretation of repeat use before changing the product.

**Metrics:** Useful first-task completion, total task time, repeat use among a clearly defined eligible cohort; guardrails for wrong assertions and failed tasks. Also show broad usage so eligibility does not hide exclusion.

**Follow-up question:** Output quality improves but return remains flat. Which part of the workflow would you investigate next, and what would change your priority?

### Case B: Automatic repair sometimes hides real defects

**Symptom:** Post-repair tests pass, but some repairs make tests accept incorrect product behavior.

**Clarify:** What kinds of edits occur? Does the agent change locators, data, expected values, or assertions? How severe are the hidden defects? Where are changes applied, and can the affected releases be identified?

**Breakdown:** Requirement correctness → failure classification → proposed change → review and application → regression evidence → release use.

**Possible hypotheses:** The objective rewards passing tests; requirement context is missing; locator changes target the wrong element; the system cannot distinguish application bugs from outdated tests; review hides changes to test meaning.

**Distinguishing evidence:** Compare original and repaired assertions against authoritative requirements. Use known application defects and legitimate maintenance cases. Examine whether the repair preserves defect detection. Inspect action records to determine affected scope.

**Conditional action and trade-off:** Contain the harmful repair class while investigating. Keep useful evidence collection or drafting if its boundaries are sound. Require review for changes to expected behavior until evidence supports a narrower policy. This may reduce speed, but it protects the purpose of testing.

**Metrics:** Correct repair by failure category, real defects preserved and caught, harmful changes applied, false alarms, and total maintenance time. Pass rate is supporting evidence only.

**Follow-up question:** Most repairs are correct, but a small subset can weaken payment tests. Why might aggregate accuracy be insufficient for expanding autonomy?

### Case C: Users say they do not trust AI output

**Symptom:** Users express doubt, manually recheck everything, reject suggestions, or disable the feature.

**Clarify:** Trust in which task: generation, explanation, repair, or execution? What happened the last time they rejected an output? Is their concern correctness, missing evidence, predictability, privacy, or loss of control?

**Breakdown:** Actual output quality → ability to verify → action boundaries → experience of past outcomes. Trust is affected by all four.

**Possible hypotheses:** Output really is wrong; evidence is difficult to inspect; inconsistent results create uncertainty; unclear permissions worry administrators; even accurate output requires mandatory review.

**Distinguishing evidence:** Observe review behavior on correct and incorrect examples. Compare user judgments with expert assessments. Examine support incidents and reversals. Interview both users who reject and users who accept too readily.

**Conditional action and trade-off:** Improve the failure mechanism. If sources are hard to inspect, test an evidence-linked review. If output is poor, explanations alone may merely make bad answers more persuasive. More detail can help verification but also overload reviewers.

**Metrics:** Correct acceptance and rejection decisions, review effort, harmful acceptance, repeat use, and qualitative understanding of action boundaries. High acceptance alone is not the goal.

**Follow-up question:** Users accept more suggestions after a confidence badge is added, but correctness is unchanged. How would you judge the change?

### Case D: Engineering wants more autonomy

**Symptom or proposal:** Engineering attributes workflow delays to human approvals and proposes removing them. The claimed delay may be real, but the proposed cause needs evidence.

**Clarify:** Which actions need approval today? How much time is waiting versus active checking? Which tasks and users are affected? What mistakes does review currently catch?

**Breakdown:** Preparation time → waiting for review → review effort → execution → recovery. Separate avoidable friction from useful verification.

**Possible hypotheses:** Approval queues dominate; review is confusing; output quality creates long inspection; policies require review; users are unavailable during execution.

**Distinguishing evidence:** Measure task stages and inspect caught errors. Test whether a clearer review screen reduces effort. Evaluate specific automatic action classes in shadow mode before broad execution.

**Conditional action and trade-off:** If a well-defined, reversible action has reliable verification and approvals add little, trial automatic execution within policy. The possible chain is fewer interruptions → faster completion → more exposure to undetected errors. Scope limits and monitoring address that exposure; they do not make it disappear.

**Metrics:** End-to-end task time, review error detection, incorrect actions, recovery time, interruptions, and user control satisfaction.

**Follow-up question:** How would you respond if the fastest design saves time but reviewers lose the ability to notice changed assertions?

### Case E: A large customer requests full automation

**Symptom or request:** A major account wants unattended test edits and execution across projects.

**Clarify:** What business outcome and workflow drive the request? Who can authorize it? Which projects, environments, and action types are included? What current workaround, deadline, or renewal concern exists?

**Breakdown:** Customer value → shared needs across segments → action risk → integration and permission requirements → delivery and support cost.

**Possible hypotheses:** A genuine high-volume maintenance problem exists; review ownership is unclear; the customer really needs scheduled execution; the request reflects a procurement preference rather than user need.

**Distinguishing evidence:** Map real tasks with daily users and administrators. Estimate frequency and burden. Assess the requested action classes against existing evaluation evidence. Compare other customers with similar constraints without assuming the largest account represents everyone.

**Conditional action and trade-off:** Offer a clearly bounded pilot if it can solve a valuable repeated job within acceptable controls. Reusable capabilities may justify investment; a costly special case may displace broader needs. A commercial threat matters, but does not prove technical readiness or authorize unsupported guarantees.

**Metrics:** Useful tasks completed, total customer effort, harmful actions, scope violations, support load, and actual adoption. Treat retention or renewal impact as a hypothesis until observed.

**Follow-up question:** The account refuses extra approvals. Which actions could still be offered safely, and which uncertainty prevents broader automation?

### Case F: MCP integration versus direct APIs

**Symptom or decision:** The team wants to connect an AI testing workflow to several systems and must choose an integration approach.

**Clarify:** Which user task is blocked? How many systems and AI applications need the capability? Are mature connections available? Are operations read-only, writes, or both? What permission and debugging requirements matter?

**Breakdown:** User workflow → required capabilities → access boundaries → integration fit → ongoing ownership and cost.

**Possible hypotheses:** Reusable connections reduce repeated work; the actual bottleneck is missing capabilities; one narrow direct integration is sufficient; available servers introduce gaps or operational complexity.

**Distinguishing evidence:** Map one complete task, verify required capabilities and access behavior, and compare integration and maintenance effort. Include connection failures and ambiguous write outcomes in the evaluation.

**Conditional action and trade-off:** Choose the approach that best supports the required workflow with manageable control and maintenance. Standardization may help reuse but adds little if users cannot complete the task reliably. Direct integration may simplify a narrow need while creating duplicated work if the scope later expands.

**Metrics:** Successful connected tasks, setup time, connection failure rate, permission correctness, support effort, and total maintenance cost. “Number of connected tools” is not sufficient value evidence.

**Follow-up question:** Both options can read results, but only one supports the required safe update flow. How does that change the comparison?

## Part 13: Marketplace thinking from zero

**P0 — MUST KNOW**

A food-delivery marketplace coordinates **buyers, merchants, and drivers**. The platform is the coordinator and business around these three participating sides.

**Buyer ↔ Merchant ↔ Driver ↔ Platform**, with information, money, and decisions connecting all of them.

The buyer wants a suitable meal at an acceptable total price and time. The merchant wants profitable demand it can fulfill. The driver wants worthwhile work with reasonable waiting and travel. The platform wants reliable completed orders and a sustainable business.

### 13.1 One order connects all sides

A buyer opens the service, finds an available meal, evaluates price and ETA, and places an order. The merchant needs to receive and accept it, prepare the correct food, and hand it over. A driver must become available, accept the assignment, reach pickup, and deliver. The platform supports matching, information, payments, and recovery when something fails.

Some activities overlap: preparation can happen while a driver is being matched or travelling to the merchant. Exact operating rules vary and should be clarified in a case.

One side's local success does not guarantee an order's success. A merchant can accept an order that no driver can collect. A driver can arrive quickly and wait at an overloaded kitchen. A buyer can place an order that later cancels.

### 13.2 Buyer outcomes and metrics

- **Selection:** Suitable meals available to this buyer at this time. A large catalog is less useful if nearby items are out of stock.
- **Price:** Food cost and relevant charges after applicable discounts. Buyers experience the total amount they pay.
- **Delivery fee:** A buyer charge related to delivery. It is not necessarily equal to the driver's pay or actual delivery cost.
- **ETA:** Estimated time of arrival. The buyer needs both a useful estimate and a service that can meet it.
- **Conversion:** The share of defined opportunities becoming a specified action, such as eligible sessions producing an order.
- **Order frequency:** Orders per defined buyer over a period. State whether buyers are active, ordering, or all registered users.
- **Retention:** The share of a defined cohort returning for a meaningful action later.
- **Cancellation:** An order ending without completion, under a stated status and denominator definition.

Example: a buyer may find a cheap meal but abandon because the delivery fee and ETA make it unsuitable for a short lunch break. Study the whole choice, not the menu price alone.

### 13.3 Merchant outcomes and metrics

- **Merchant availability:** Whether the restaurant is open and can offer the relevant items. Online status alone may overstate real capacity.
- **Order acceptance:** Accepted eligible orders divided by incoming eligible orders. Separate explicit rejection from no response when useful.
- **Preparation time:** Time from a defined start to food ready for pickup. Variation matters because drivers and buyers plan around it.
- **Menu accuracy:** Whether displayed items, prices, options, and stock match what can actually be supplied.
- **Capacity:** How much work the kitchen can complete within a time window at acceptable quality.
- **Merchant cancellations:** Orders cancelled for merchant-related reasons, using a clearly defined measure.
- **Order volume:** Incoming, accepted, or completed orders; distinguish them.
- **Merchant economics:** What the merchant retains after fees, funded discounts, food, packaging, labor, and other relevant costs.

Example: more promoted orders may increase revenue but overload preparation and displace profitable walk-in business. Ask whether orders are incremental and profitable for the merchant.

### 13.4 Driver outcomes and metrics

- **Supply:** Drivers available for the relevant area and time, not merely registered accounts.
- **Acceptance rate:** Accepted assignment offers divided by eligible offers. The offer-level denominator differs from buyer-order completion.
- **Utilization:** The share of defined available time counted as busy or productive. State whether pickup waiting is included.
- **Idle time:** Time available without an active task under the chosen definition. Some idle capacity is a buffer for surges.
- **Pickup waiting:** Time a driver waits for food after arriving. It uses capacity even without moving a meal.
- **Trip distance:** Travel associated with pickup and delivery; unpaid repositioning may also affect earnings.
- **Earnings:** Pay after relevant costs, ideally considered per online hour as well as per order.
- **Incentives:** Additional rewards intended to change availability, acceptance, location, or behavior.

Example: pay per order rises, but restaurant waiting doubles. A driver may earn less per online hour because fewer orders fit into the shift. Counting people without their time cycle misses effective capacity.

### 13.5 Platform outcomes and metrics

- **Completed orders:** Orders successfully fulfilled under a stated definition.
- **GMV, or gross merchandise value:** The value of transactions included in the chosen definition. It is not platform revenue.
- **Revenue:** The platform's defined income from commissions, fees, or other included services.
- **Take rate:** Defined platform revenue divided by the corresponding GMV. State the numerator and denominator; it is not always the merchant commission rate.
- **Subsidy:** A platform-funded benefit reducing the effective cost or supporting participation.
- **Contribution margin:** Revenue minus included variable costs, shown as an amount or as a percentage with an explicit denominator.
- **Reliability:** Whether the marketplace consistently fulfills its promises, such as availability, completion, and arrival timing.
- **Retention:** Continued meaningful use by a specified buyer, merchant, or driver cohort.
- **Marketplace balance:** Demand and usable fulfillment capacity are reasonably matched within relevant places and times.

Part 16 works through the money in one order. For now, connect the measures: completed orders create transaction value; the platform receives only defined income from that activity and incurs costs to support it.

### 13.6 Liquidity is local and time-sensitive

**Marketplace liquidity** is the ability to match demand with suitable, available supply so a transaction can be fulfilled at acceptable terms. In food delivery, that requires a meal, kitchen capacity, delivery capacity, price, and timing that work together.

Imagine many drivers online across a city but none close enough to an office district at noon. The citywide driver count looks healthy, yet local liquidity is weak. More buyer traffic can increase frustration if it cannot turn into completed orders.

**Check yourself:** How can merchants complain about low orders while nearby buyers complain about long ETA? Consider location, selection, driver cycles, and where demand is concentrated.

## Part 14: Marketplace systems thinking

**P0 — MUST KNOW**

Every chain in this part is a **HYPOTHESIS in an ILLUSTRATIVE EXAMPLE**. It describes what might happen if the stated conditions hold. Ask for evidence at each important link. The stage labels are a thinking aid, not a claim that behavior unfolds in a fixed number of steps.

### 14.1 Promotion

**Action and first-order effect:** A discount lowers the effective price for eligible buyers and may increase order attempts.

**Second-order effect:** If kitchens and drivers lack spare capacity, the extra work creates queues and longer delivery times.

**Possible third-order effect:** Late or cancelled deliveries reduce future buyer trust, while merchant waste and driver waiting weaken participation.

**Stakeholders:** Buyers receive a lower price but may experience worse service. Merchants receive demand but may exceed capacity. Drivers may gain work but spend more time waiting. The platform funds discounts and handles failed service.

**Metrics and guardrails:** Track incremental completed orders, placed orders, acceptance, pickup wait, cancellation, contribution, and later retention. Watch neighboring areas if drivers move.

**Evidence that changes the chain:** Spare kitchen and driver capacity, low redemption, or demand shifting from another time may make the overload prediction wrong. A promotion can use idle capacity productively. Establish whether the orders are new, shifted, or subsidized existing demand.

### 14.2 Driver incentives

**Action and first-order effect:** A targeted reward may attract drivers online or into a lunch zone.

**Second-order effect:** More available capacity may shorten assignment time. However, some drivers may simply move from nearby zones rather than add working hours.

**Possible third-order effect:** Neighboring shortages worsen, or driver availability falls when the incentive ends. If the incentive supports durable participation, some benefit may persist instead.

**Stakeholders:** Drivers compare expected hourly earnings and travel; buyers and merchants depend on coverage; the platform bears the incentive cost.

**Metrics and guardrails:** Available driver hours, accepted assignments, completion, assignment time, earnings after relevant costs per online hour, incentive cost per incremental completion, and neighboring-zone service.

**Evidence that changes the chain:** Trace where extra capacity came from and whether pickup queues were already the real constraint. Paying more drivers to wait at the same kitchens may add cost without solving throughput.

### 14.3 Rain

**External change and first-order effect:** Rain may increase demand for delivery and reduce willingness or ability to drive. It can also slow travel. The strength of each response depends on severity and location.

**Second-order effect:** Longer trips and fewer available drivers reduce effective capacity, potentially increasing assignment failures and ETA.

**Possible third-order effect:** Cancellations create merchant waste and buyer dissatisfaction; drivers may end shifts if conditions become unsafe or earnings do not justify the work.

**Stakeholders:** All sides face a different form of risk: access to meals, prepared-food loss, travel conditions, and failed-service costs.

**Metrics and guardrails:** Local rainfall timing, order attempts, available driver hours, assignment acceptance, reassignment, order cancellation, travel time, and safety incidents. Do not make risky driving the route to meeting a speed target.

**Conditional response:** More accurate promises, restricted service in unsafe areas, or appropriately scoped incentives may help different conditions. None should be selected solely because “rain means pay drivers more.”

### 14.4 Merchant onboarding

**Action and first-order effect:** Reducing unnecessary onboarding friction may bring more merchants onto the platform sooner.

**Second-order effect:** More relevant available meals may improve conversion and demand distribution. If quality checks are weakened, inaccurate menus or poor operations may increase failed orders.

**Possible third-order effect:** Reliable new selection can encourage repeat buying. Unreliable selection can create distrust and support costs, or cause good merchants to lose demand to misleading offers.

**Stakeholders:** Buyers need dependable choice; new merchants need access and guidance; existing merchants face competition; drivers encounter unfamiliar pickup operations.

**Metrics and guardrails:** Time to first fulfillable order, active available selection, completed orders per new merchant, menu accuracy, acceptance, preparation reliability, complaints, and cancellations.

**Evidence that changes the chain:** Determine which checks create delay and which prevent meaningful harm. Faster information collection differs from removing essential quality checks. Raw merchant registrations are not sufficient proof of supply improvement.

### 14.5 Restaurant preparation delays

**Change and first-order effect:** Overloaded kitchens or inaccurate preparation estimates delay food readiness.

**Second-order effect:** Drivers wait longer and complete fewer trips per hour. Effective delivery capacity falls despite stable driver counts.

**Possible third-order effect:** Assignment delays spread to other orders, driver earnings decline, and buyers reduce future use after late deliveries.

**Stakeholders:** Merchants face queues and quality pressure; drivers lose time; buyers receive late or lower-quality meals; the platform sees worse reliability.

**Metrics and guardrails:** Preparation duration, readiness estimate error, pickup waiting, deliveries per online hour, late delivery, cancellation, and merchant receipts.

**Conditional response:** Improving readiness information may better coordinate pickup if information is the issue. If the kitchen is physically overloaded, information alone cannot create capacity; adjust demand, availability, or operations. Do not mistake a scheduling problem for a staffing problem without evidence.

### 14.6 Free delivery

**Action and first-order effect:** Removing the buyer's delivery fee lowers the visible total price and may improve checkout conversion.

**Second-order effect:** Buyers may place more small or distant orders that are expensive to fulfill. Demand can also shift from orders they would have placed anyway.

**Possible third-order effect:** Contribution deteriorates or capacity becomes overloaded. Alternatively, stronger repeat use or denser short trips may improve longer-term economics if supported by evidence.

**Stakeholders:** Buyers receive a lower charge; drivers still need compensation; merchants may gain volume; the platform or another identified payer funds the benefit.

**Metrics and guardrails:** Incremental completed orders, average food value, distance mix, delivery cost, subsidy per order, contribution, lateness, and post-offer retention.

**Evidence that changes the chain:** Identify who pays and what eligibility rules apply. “Free” to the buyer does not mean delivery has no cost. Compare benefits with the counterfactual and total system capacity.

### 14.7 Geographic expansion

**Action and first-order effect:** Serving a new area increases potential reach and may make more meals accessible.

**Second-order effect:** Longer travel or low order density can reduce driver productivity and make selection less reliable than a catalog suggests.

**Possible third-order effect:** Poor early experiences weaken repeat demand, making the area harder to serve efficiently. A dense, well-supported launch could instead build a healthier local cycle.

**Stakeholders:** New buyers and merchants gain access; drivers may face repositioning and longer trips; existing areas may lose capacity; the platform funds launch and support.

**Metrics and guardrails:** Local fulfillable selection, time to match, completed orders, distance, driver earnings per online hour, contribution, retention, and effects on existing zones.

**Conditional response:** A limited area and time window can test whether supply and demand match. More geographic coverage is not equivalent to more useful service.

### 14.8 Driver shortage

**Change and first-order effect:** Too little available delivery capacity leaves more orders waiting for assignment or pickup.

**Second-order effect:** Longer waits can create merchant food waste, buyer cancellation, and pressure on the remaining drivers.

**Possible third-order effect:** Lower driver satisfaction or buyer trust can reduce future participation, making the imbalance harder to fix.

**Stakeholders:** Each side is affected, even if the initial shortage is measured in driver supply.

**Metrics and guardrails:** Available driver hours, assignment time, driver cycle time, pickup wait, acceptance, unfulfilled orders, earnings, cancellations, and incentive spending.

**Evidence that changes the chain:** Distinguish too few online drivers from poor positioning, rejected offers, longer trips, and kitchen waiting. Increase capacity at the binding constraint. A larger registered driver pool may not help today's lunch period.

### Marketplace systems check

Choose one intervention above. Explain its intended benefit, a condition needed for that benefit, one downstream risk, and the evidence that would reveal it. Avoid treating every possible risk as equally likely.

## Part 15: Marketplace diagnosis

**P0 — MUST KNOW**

The interviewer says, “Orders dropped 20%.” You do not know the cause yet. Your first job is to make the number meaningful and choose a comparison that narrows the investigation.

### 15.1 Verify what changed

Clarify placed versus completed orders, the comparison period, geography, and whether the decline is relative. Check that reporting is complete and definitions did not change. Compare the event pipeline with another reliable source when available.

Your technical background can help here. An event-name change, missing DataLayer field, duplicated event, or broken tracking tag can change a report without the same change in transactions. This is a hypothetical application of technical intuition, not a claim about the candidate's past incidents.

Also avoid the opposite error: assuming a real business decline is “just analytics.” If order records and payment or fulfillment evidence agree, prioritize the real mechanism.

### 15.2 Locate when and where

Ask when the decline began. Sudden changes suggest different hypotheses from gradual ones. Compare similar weekdays and time windows; consider holidays, weather, campaign timing, recent releases, and data delays.

Then locate the affected city, district, meal period, customer cohort, merchant type, distance band, or app version. Do not request every segment at once. Choose the next split that is most likely to separate mechanisms.

New users falling while existing buyers stay stable points toward acquisition or first-use issues. Existing buyers reducing frequency may point toward recurring value, price, or prior service experience. Both still need evidence.

### 15.3 Decompose the outcome

For consistent definitions:

**Completed orders = placed orders × completion rate.**

If placed orders fall, examine the demand funnel: eligible traffic, meal availability, menu interaction, checkout, payment, and order creation. If placement is stable but completion falls, inspect fulfillment and cancellation stages.

Use a buyer-based view when frequency matters:

**Placed orders = ordering buyers × orders per ordering buyer.**

For a session-based view, use eligible sessions × orders per eligible session. Do not add frequency to that formula unless definitions explicitly require it.

**ILLUSTRATIVE EXAMPLE:** Last period, 10,000 placed orders at 90% completion produced 9,000 completed orders. Now 9,000 placed orders at 80% completion produce 7,200. Completed orders fell 20%, caused arithmetically by both fewer placements and a lower completion rate. This does not identify the business causes of either component.

One descriptive bridge is to hold the old completion rate while changing placement: 9,000 × 90% = 8,100, a loss of 900. Then change completion to 80%, a further loss of 900. The allocation depends on the bridge order; do not present it as unique causal attribution.

### 15.4 Investigate each side and the shared system

**Buyer hypotheses:** Lower traffic, higher total price, worse selection, longer quoted ETA, payment friction, reduced frequency after poor experiences, or fewer relevant occasions.

**Merchant hypotheses:** Fewer open restaurants, missing stock, missed notifications, lower acceptance, overloaded kitchens, or inaccurate preparation estimates.

**Driver hypotheses:** Fewer available hours, poor positioning, low offer acceptance, longer distances, more pickup wait, or weather disruption.

**Technical and operational hypotheses:** Checkout errors, stale availability, payment incidents, delayed notifications, matching problems, reporting changes, or external dependency failures.

The sides interact. A driver shortage can worsen quoted ETA before buyers order, reducing placement as well as completion. Do not assume every demand-funnel decline originates solely with buyers.

### 15.5 Rank hypotheses instead of collecting everything

Rank by fit with timing and segment, potential contribution to the decline, prior evidence, and the cost of checking. A sudden drop on one app version makes a release issue a useful early check. A lunch-only problem with long pickup queues makes kitchen-related capacity plausible.

Say what you expect to see. “If missing notifications explain merchant rejection, non-response should rise more than explicit rejection, especially on affected devices.” That prediction tells the interviewer why the evidence matters.

Look for evidence against your favorite explanation. If preparation time is stable and drivers are waiting for offers, kitchen overload becomes less convincing.

### 15.6 Choose action and measurement

Match the action to the mechanism. A verified checkout regression may need a rollback or fix. Inaccurate stock may need availability updates. Overloaded restaurants may need capacity management. Insufficient delivery capacity may call for targeted supply action or a more realistic service promise.

Define the scope and collaborating team. Use completed orders as an outcome when recovering fulfillment, with relevant reliability and economic guardrails. Monitor neighboring zones if capacity moves.

Ask what would change the action. If assignment improves but completion stays low because preparation worsens, reassess the constraint. Do not keep funding the first intervention just because it improved its local metric.

### 15.7 Causal evaluation in a shared marketplace

**P1 — SHOULD KNOW**

Buyers in a treatment and control group can share kitchens and drivers. A promotion for treated buyers may overload restaurants serving control buyers. This **spillover** means the comparison group is also affected.

Depending on the decision, consider geographic clusters or a **switchback**, which alternates treatment across defined times. These designs still face movement, weather, seasonality, and effects that carry into later periods. Explain the main limitation instead of saying “A/B test” as though it settles causality.

**Check yourself:** Completed orders recover in the target district while nearby districts decline. What additional evidence do you need before calling the intervention successful?

## Part 16: Unit economics from zero

**P0 — MUST KNOW**

**Unit economics** asks how much income and cost are associated with one unit of activity, such as one completed order. It helps you understand whether growth improves or weakens the business under stated assumptions.

### 16.1 The important terms

**GMV** is the transaction value counted under a defined rule. For this teaching example, it is food value before the platform voucher and excludes delivery fees. Real organizations may define it differently.

**Revenue** is the platform's defined income. **Merchant commission** is a charge to the merchant for the platform's service. **Delivery fee** is a buyer charge. These may contribute to platform revenue, but neither automatically equals profit.

A **subsidy** funds a benefit, such as a buyer voucher. A **driver incentive** is an additional payment intended to encourage supply or behavior. Identify the payer: platform, merchant, or another party. A discount displayed to buyers does not tell you who bears it.

A **variable cost** changes with the activity under analysis. Driver compensation, payment processing, and some support or refund costs may be included in an order model. State which costs are included.

**Contribution margin amount = defined revenue − included variable costs.** It describes what remains to cover excluded costs and potentially profit. It is not total company profit. Fixed costs such as office rent and some salaried functions are outside this simplified order model.

### 16.2 One hypothetical order, with the money reconciled

**ILLUSTRATIVE EXAMPLE — All numbers below are invented for learning. They are not ShopeeFood's prices, commission, pay, costs, or accounting policy.**

A buyer orders food priced at **100,000 VND**. The listed delivery fee is **20,000 VND**. A platform-funded voucher reduces the buyer's payment by **10,000 VND**.

The buyer pays **110,000 VND**: 100,000 for food + 20,000 delivery − 10,000 voucher.

Assume a hypothetical merchant commission of **20,000 VND**. The merchant receives **80,000 VND** from the order, before its food, packaging, labor, rent, and other costs. That receipt is not the merchant's profit.

Assume the driver receives **22,000 VND**, with no additional incentive in this example. Other included variable costs total **3,000 VND** for payment and allocated order-related service costs. Taxes, tips, refunds, settlement timing, and other possible charges are omitted to keep the model simple.

**Cash reconciliation:**

110,000 buyer payment = 80,000 merchant receipt + 22,000 driver compensation + 3,000 other included costs + **5,000 platform contribution**.

The equation accounts for every VND in this simplified example. The voucher has already reduced buyer cash received.

### 16.3 View the same order through revenue and costs

Using a **gross revenue before voucher** convention for this exercise:

- Food GMV: **100,000 VND**.
- Merchant commission revenue: **20,000 VND**.
- Delivery-fee revenue: **20,000 VND**.
- Total defined revenue before voucher: **40,000 VND**.
- Included costs: **10,000 voucher + 22,000 driver compensation + 3,000 other = 35,000 VND**.
- Contribution margin amount: **40,000 − 35,000 = 5,000 VND**.

Some accounting presentations treat a promotion as a reduction in revenue. With that presentation, net revenue here would be 30,000 VND and remaining included costs 25,000 VND, still leaving 5,000 VND contribution. **Do not subtract the same voucher twice.** This example teaches reconciliation, not a company's reporting rules.

### 16.4 Take rate and margin percentage

**Take rate = defined platform revenue ÷ corresponding GMV.**

Using the exercise's gross revenue of 40,000 and food GMV of 100,000 gives a 40% gross take rate. Using revenue after the voucher gives 30%. The merchant commission rate is 20%, a different measure. These unusually simple teaching numbers are not benchmarks.

A contribution margin percentage also needs a denominator. With 5,000 contribution and 40,000 gross revenue, it is 12.5% of gross revenue. With GMV as denominator, it is 5% of GMV. Say which measure you mean; do not compare unlike percentages.

For an interview, start with the amount per order and ask how the company defines its reported measures. Correct definitions matter more than memorized rates.

### 16.5 Why more orders can weaken economics

Without the 10,000 voucher, the same simplified order would contribute **15,000 VND**, assuming every other value stays unchanged.

**ILLUSTRATIVE EXAMPLE — Two comparable periods under a strong teaching assumption:** Suppose a credible comparison suggests 100 orders would occur without the promotion, each contributing 15,000 VND. Total contribution would be **1,500,000 VND**.

With the promotion, suppose 140 orders occur and every order receives the voucher. At 5,000 VND contribution each, total contribution is **700,000 VND**.

Orders rise **40%**, but near-term contribution falls **800,000 VND**. The arithmetic does not prove the promotion is always wrong. It shows what longer-term or other benefit would need evidence and a deliberate budget to justify the trade-off.

### 16.6 Incrementality and the counterfactual

An **incremental order** is one caused by the intervention beyond what would otherwise occur in the relevant scope and period. A redeemed voucher is not automatically incremental.

Some buyers would order anyway. Some move an order from dinner to lunch. Some switch from another merchant on the same platform. Some generate new demand. Each pattern has different value.

The key comparison is **total contribution with the intervention minus total contribution under a credible no-intervention comparison**, including costs paid on non-incremental orders. Looking only at the promoted order count misses subsidized existing demand.

Longer-term retention may justify a bounded acquisition investment, but measure it over a suitable period with a credible comparison. Do not use “lifetime value will improve” as an unsupported escape from poor current economics.

### 16.7 Buyer, merchant, driver and platform economics differ

The buyer's discount may be funded by the merchant, the platform, or both. The driver may receive more per order while earning less per hour if waiting increases. The merchant may gain sales but lose contribution after food cost, discounts, and congestion. Platform contribution does not measure whether the other sides can sustain participation.

**P1 — SHOULD KNOW:** Average order contribution can hide costly segments. Long distances, small baskets, refunds, and peak incentives can change economics. Compare segments before scaling a promotion across all orders.

**Check yourself:** In the hypothetical order, who funds the voucher, why is 100,000 VND GMV different from 40,000 VND revenue, and why is the merchant's 80,000 VND receipt not profit?

**Audio recap — Marketplace and economics:** A delivered meal needs a buyer, a ready kitchen, and available delivery capacity at the same time. More demand helps only if the system can serve it. The food's full value is not platform income, and platform income is not profit. In our invented order, the money must cover the merchant, driver, voucher, and other costs. Ask who pays, what remains, and whether the order would have happened anyway.

## Part 17: ShopeeFood case mental models

**P0 — MUST KNOW**

All eight cases are **ILLUSTRATIVE EXAMPLES**. They demonstrate investigation routes, not memorized answers. Attempt the initial framing before reading each scaffold. Any predicted effect is a hypothesis until evaluated.

### Case A: Orders decline 20%

**Clarifying questions:** Placed or completed orders? Compared with which period? Is reporting complete? When, where, and among which buyers did the change start?

**Decomposition:** Completed orders = placed orders × completion rate. Then examine the ordering funnel or fulfillment stages according to the branch that changed.

**Hypotheses:** Lower traffic, higher total price, unavailable meals, checkout errors, merchant rejection, driver capacity, or tracking changes. Rank by timing and affected segment.

**Evidence:** Counts and rates for comparable periods, city and meal-period splits, new versus existing buyers, app releases, acceptance, assignment time, and cancellation stages. Request the next decisive comparison rather than every possible metric.

**Stakeholders:** Buyers lose access or reliability; merchants lose fulfilled sales; drivers may lose productive work or face queues; platform contribution may fall.

**Conditional action and trade-off:** Fix the verified constraint. A promotion may help a price-sensitive demand gap but consume subsidy. If fulfillment is constrained, more demand can worsen delays and cancellations.

**Metrics and second-order effects:** Recover completed orders while checking reliability, contribution, and local capacity. Watch whether the fix moves demand or drivers and creates a problem elsewhere.

**Follow-up:** Placed orders are stable. Which part of your initial investigation becomes less urgent, and where do you go next?

### Case B: Rain causes rider cancellations

**Clarifying questions:** Does “cancellation” mean a rider rejects an offer, cancels an assignment, or the whole order cancels? How severe is the rain, in which areas, and at which stage? Treat the prompt's causal wording as something to inspect.

**Decomposition:** Available hours → offers → acceptance → pickup travel → wait → delivery. Separate safety, travel, willingness, and reassignment.

**Hypotheses:** Unsafe routes, longer travel, low expected hourly earnings, flooded pickup points, or demand exceeding the remaining capacity.

**Evidence:** Cancellation stage and reason, local weather timing, distance, trip duration, driver availability, reassignment success, and accounts of actual affected trips. Compare similar conditions when feasible.

**Stakeholders:** Driver safety matters directly. Buyers need honest promises; merchants risk prepared-food waste; the platform handles disrupted service.

**Conditional action and trade-off:** Match the response to the mechanism: accurate ETA, restricted unsafe service, clearer disruption information, or targeted compensation where service remains feasible. An incentive costs money and may attract capacity; it cannot make an unsafe route safe.

**Metrics and second-order effects:** Completion, assignment cancellation, order cancellation, severe delay, driver earnings, safety incidents, and merchant waste. More demand encouraged during a shortage may deepen the problem.

**Follow-up:** Rider reassignment increases but order completion stays stable. What has improved or worsened for drivers and buyers?

### Case C: ETA increases

**Clarifying questions:** Quoted ETA, actual arrival time, or error between them? Mean or slow tail? Which distance, zone, meal period, and merchant segment?

**Decomposition:** Matching and pickup travel, preparation, handoff, delivery travel, and buffers. Preparation and matching can overlap, so use the actual timeline rather than adding overlapping durations twice.

**Hypotheses:** A more accurate estimate, slower kitchens, fewer available drivers, traffic, longer-distance order mix, batching effects, or stale readiness signals. Do not assume a specific matching or batching policy exists.

**Evidence:** Stage timestamps, readiness and arrival times, actual-versus-promised errors, distance mix, pickup waiting, and assignment patterns. Compare like-for-like orders before blaming operational speed.

**Stakeholders:** Buyers plan around the promise; merchants and drivers coordinate readiness; the platform balances conversion and reliability.

**Conditional action and trade-off:** If quoting is more accurate while actual time is stable, shortening the displayed promise could mislead buyers. If preparation drives delay, address that constraint. More conservative estimates may lower conversion while reducing surprise.

**Metrics and second-order effects:** Actual duration, ETA error, lateness, checkout conversion, completion, driver cycle time, and retention. Poor promises can affect future orders even if today's conversion rises.

**Follow-up:** Quoted ETA rises, but late deliveries decrease. How would you decide whether the change benefits buyers?

### Case D: Merchant acceptance decreases

**Clarifying questions:** Explicit rejection or no response? Which incoming orders are eligible? Is the decline concentrated by merchant, device, time, cuisine, or menu item?

**Decomposition:** Receive notification → notice it → assess stock and capacity → accept or reject → prepare. An apparent willingness problem may be a delivery or interface problem.

**Hypotheses:** Missed notifications, incorrect open status, unavailable items, overloaded kitchens, poor order economics, or a changed acceptance process.

**Evidence:** Notification delivery and acknowledgement, response times, rejection reasons, stock accuracy, kitchen load, recent product changes, and observed merchant tasks.

**Stakeholders:** Merchants need fulfillable work; buyers need accurate availability; drivers need reliable pickup; the platform needs successful orders.

**Conditional action and trade-off:** If notifications fail, restore them. If the kitchen is full, more pressure to accept could worsen the service. Better stock and capacity information may reduce displayed selection while increasing the chance that available offers can be fulfilled.

**Metrics and second-order effects:** Acceptance and non-response separately, accepted-to-completed rate, preparation time, cancellation, merchant contribution, and complaints. Raising acceptance can move failure downstream rather than remove it.

**Follow-up:** Acceptance improves but merchant cancellations rise. What does that suggest about the intervention?

### Case E: A promotion raises orders but hurts economics

**Clarifying questions:** Which orders increased? What is the contribution definition? Who funds the offer? What objective, budget, duration, and retention horizon were intended?

**Decomposition:** Order volume × contribution per order, then revenue, buyer discount, driver compensation, incentives, payment, refunds, and other included costs. Compare totals as well as averages.

**Hypotheses:** Existing demand is subsidized; baskets are smaller; distances or peak costs increase; capacity causes refunds; newly acquired demand has weak repeat value.

**Evidence:** A credible counterfactual, redemption and eligibility, segment economics, later cohorts, service quality, and who would likely have ordered without the offer.

**Stakeholders:** Buyers benefit immediately; merchants and drivers may gain or lose depending on load and costs; the platform funds part of the activity.

**Conditional action and trade-off:** Narrow, modify, stop, or continue within an explicit learning budget according to incremental value. Short-term negative contribution may be deliberate, but future benefits need evidence rather than optimism.

**Metrics and second-order effects:** Incremental completed orders, total contribution, subsidy per incremental completion, service reliability, and later unsubsidized behavior. Congestion may create costs beyond the voucher itself.

**Follow-up:** Promoted users retain better than other users. Why does that comparison alone not prove the promotion caused retention?

### Case F: Easier merchant onboarding increases supply but reduces quality

**Clarifying questions:** Which steps were relaxed? What does supply mean: listed merchants, available meals, or fulfilled orders? Which quality outcome worsened?

**Decomposition:** Sign up → provide information → verification and setup → activate → accept → prepare reliably → remain active.

**Hypotheses:** Essential checks were removed; merchants misunderstand operations; stock and menu data are incomplete; support capacity cannot handle the new cohort.

**Evidence:** Compare onboarding cohorts and merchant types, identify where defects originate, observe new-merchant tasks, and inspect early cancellation, complaints, and preparation.

**Stakeholders:** New merchants gain access, buyers face uncertain quality, drivers may wait, and existing merchants compete with the expanded selection.

**Conditional action and trade-off:** Preserve useful friction reduction while restoring or redesigning checks tied to observed harms. Assisted setup or limited early exposure may help if lack of understanding is the issue. Additional review can slow activation and add operating cost.

**Metrics and second-order effects:** Time to first reliable order, active fulfillable supply, acceptance, accurate menus, early cancellations, support cost, and retention. Poor early experiences may damage trust beyond the new merchants.

**Follow-up:** Registrations double but completed orders remain flat. Which definition of supply should guide the decision?

### Case G: One district grows while another falls

**Clarifying questions:** Absolute counts or percentage rates? Same baseline size and time window? Did boundaries or attribution change? Are the districts sharing drivers, merchants, or promotions?

**Decomposition:** Demand and fulfillment in each district, then overall totals. Compare traffic, ordering, completion, local capacity, and movement between areas.

**Hypotheses:** Different price sensitivity, merchant selection, office demand, local events, weather, delivery distances, or capacity moved by incentives.

**Evidence:** Comparable segmented funnels, order origins, available driver hours, repositioning, local merchant operations, and campaign exposure. A city average can conceal redistribution.

**Stakeholders:** Buyers and merchants in the declining district may bear the cost of growth elsewhere; drivers respond to expected earnings; the platform must evaluate the broader result.

**Conditional action and trade-off:** Use local responses when mechanisms differ. If the campaign merely shifts drivers, adjust the coverage or incentive design before expanding it. A uniform policy is simpler but may miss local constraints.

**Metrics and second-order effects:** Completed orders and contribution by district and in total, neighboring ETAs, driver earnings, and retention. A successful test area can create an unhealthy control area through spillover.

**Follow-up:** Growth in one district exactly offsets losses elsewhere. What evidence would show whether the platform created any additional value?

### Case H: Driver shortage during lunch

**Clarifying questions:** Fewer online drivers, fewer available nearby, low acceptance, or longer cycles? Is demand unusually high? Are drivers waiting at merchants?

**Decomposition:** Available driver time × approximate orders completed per unit of time, with location and matching constraints. Inspect pickup travel, kitchen wait, delivery, and repositioning.

**Hypotheses:** Lunch demand surge, drivers positioned elsewhere, unattractive offers, long trips, kitchen congestion, or weather. Stable driver count does not establish stable capacity.

**Evidence:** Available hours, location, assignment time, acceptance, pickup waiting, trip duration, kitchen readiness, and net hourly earnings. Determine whether drivers are absent or occupied inefficiently.

**Stakeholders:** Buyers need timely lunch; merchants face meal queues; drivers need productive and feasible trips; the platform funds interventions.

**Conditional action and trade-off:** Target the actual constraint. Add supply support if availability is limiting; address readiness or kitchen load if waiting dominates. Manage buyer promises or demand when capacity cannot recover immediately.

**Metrics and second-order effects:** Completed lunch orders, assignment delay, pickup wait, cycle time, driver earnings, contribution, cancellations, and nearby-zone coverage. New incentives can move the shortage rather than solve it.

**Follow-up:** More drivers join, but deliveries per online hour fall. Where should the investigation go next?

## Part 18: Product communication

**P0 — MUST KNOW**

Speak so another person can follow the decision. Short sentences with clear relationships are more useful than advanced vocabulary. Explain what you know, what you think may be happening, and what evidence would change the action.

### 18.1 Clarify the ambiguity that matters

Use **“I'd first clarify…”** when a definition changes the investigation.

“I'd first clarify whether orders means placed or completed orders.”

Avoid asking several unrelated questions without explaining why. Follow the first answer and choose the next useful question.

### 18.2 Give a small structure

Use **“I'd break this into…”** when the situation needs manageable branches.

“I'd break this into demand and fulfillment. First, I would check which one changed.”

For AI: “I'd separate output quality, review effort, and whether users have another relevant task.” These branches guide evidence collection; do not defend them if the evidence suggests a better breakdown.

### 18.3 Name a hypothesis and its test

Use **“My initial hypothesis would be…”** for a possible explanation, not an established fact.

“My initial hypothesis would be kitchen delays. I'd check whether pickup waiting rose in the affected lunch areas.”

Use **“The evidence I'd want to see is…”** to explain the comparison.

“The evidence I'd want to see is the type of edits users make. Convention changes would suggest a different response from incorrect assertions.”

### 18.4 Challenge an assumption respectfully

Use **“I wouldn't conclude that yet because…”** when the proposed conclusion exceeds the evidence.

“I wouldn't conclude that review is unnecessary yet because we do not know which errors it catches.”

Accept the useful part of the other person's point. “The delay is worth investigating. I'd first separate waiting for review from the time spent checking.” This keeps the discussion about the problem.

### 18.5 Make the trade-off and recommendation explicit

Use **“The main trade-off is…”** to identify the important cost.

“The main trade-off is faster activation versus reliable merchant operations.”

Use **“Given the information we have…”** to make a decision under uncertainty.

“Given the information we have, I'd test better project context first. The observed edits are mostly conventions, and the change is limited enough to evaluate quickly.”

Then name a change criterion: “I'd reconsider if correctness errors remain the main cause of review effort.” Finish after the recommendation, main reason, and material risk. Expand if asked.

### 18.6 Handle uncertainty and pressure

Use **“I don't know enough to conclude that confidently, but here's how I'd investigate it.”** Then give one useful next comparison.

If asked to decide anyway: “Assuming assignment capacity is the constraint, I'd trial a limited lunch incentive. I would monitor neighboring zones and change course if the issue is actually pickup waiting.”

If new evidence contradicts you: “That changes my view. Stable assignment time makes driver availability less likely, so I'd focus on preparation.” Changing your mind with evidence is a strength of the reasoning.

### 18.7 Translate technical detail into user impact

**P1 — SHOULD KNOW**

Instead of stopping at “the event payload is missing an ID,” connect the consequence: “Without the ID, we cannot link checkout attempts to results, so the conversion report may be misleading.”

Instead of “the model needs retrieval,” explain: “It needs the current requirement before it can judge whether the test or application is wrong.”

**Audio recap — Communication:** Help the listener follow one decision. Clarify the important ambiguity, give a small structure, request evidence with a purpose, and make a conditional recommendation. The common mistake is speaking for a long time without choosing anything. Ask yourself: could the interviewer repeat my recommendation and the evidence behind it?

## Part 19: Behavioral interview thinking

**P0 — MUST KNOW**

A behavioral answer explains something you actually did. Hypothetical case reasoning and polished teaching examples must not become employment or project history.

### 19.1 What the repository currently supports

The primary candidate source is the [evidence ledger](pm-interview-bootcamp/stories/evidence-ledger.md), supported by its preserved raw sources. Its evidence levels matter:

- **E001, SELF-REPORT:** Broad computer science/software engineering background. Exact degree, dates, and achievements are not established.
- **E002, SELF-REPORT:** Previous technical consultant or technical integrations type work. Exact title, dates, scope, and incident ownership are not established.
- **E003, SELF-REPORT:** Experience areas include GTM/GA4, APIs and data flows, troubleshooting, and explaining technical issues in understandable business language. Specific customer incidents and outcomes are missing.
- **E004, SELF-REPORT:** PRJ226 is identified as a side project. The current brief describes AI-agent/workflow exploration, but implemented capabilities, architecture, users, evaluations, and outcomes are not established by artifacts.
- **E006, OBSERVED EXERCISE:** A typed simulated case answer exists. It is evidence of an attempt at case reasoning, not evidence of customer interviews, shipped features, experiments, or business impact.

“Self-report” means the candidate stated it. It is not independent verification. The repository has no complete interview-ready, verified behavioral story. Detailed TDCX/FPT incidents and PRJ226 capabilities remain **PERSONAL EVIDENCE REQUIRED**.

### 19.2 Shape a true event

Use **Context → Problem → My responsibility → Action → Why I chose it → Result → Learning**.

Each step answers a different question:

- **Context:** Where and when did the event happen? Include only what the listener needs.
- **Problem:** What observable gap or difficulty mattered?
- **My responsibility:** What were you personally expected and authorized to do?
- **Action:** What did you actually inspect, discuss, decide, or change?
- **Why I chose it:** What evidence and alternatives informed the choice?
- **Result:** What was observed afterward, and how was it checked?
- **Learning:** What did the event change about your later judgment or behavior?

This is a structure for extracting facts, not a license to fill empty sections with plausible content.

### 19.3 Story areas that still need personal evidence

**Integration diagnosis — PERSONAL EVIDENCE REQUIRED.** The broad background suggests a relevant area to explore. Supply one actual customer request, what you observed, your personal investigation, the change made, and the verified outcome. Do not claim a conversion lift because tracking was repaired unless business conversion was separately measured.

**PRJ226 AI judgment — PERSONAL EVIDENCE REQUIRED.** Supply an actual output or behavior, how you checked it, the decision you made, and what happened. Interest in agents does not prove deployed agents, MCP implementation, customer adoption, or time savings.

**Disagreement or failure — PERSONAL EVIDENCE REQUIRED.** Identify a real initial belief, contrary evidence, your response, and its result. Do not create a dramatic conflict to demonstrate leadership.

### 19.4 Product signals must come from the event

An actual story may demonstrate challenging an assumption, diagnosing a cause, using evidence, handling disagreement, making a trade-off, learning from failure, explaining technical detail, or using AI thoughtfully.

Choose the strongest supported signal. Ordinary troubleshooting can show disciplined diagnosis without being renamed “customer discovery research” or “a product experiment.” A team outcome should not be presented as your individual achievement.

Useful honest language includes: “My part was…”, “I checked this by…”, “The result I observed was…”, and “I did not measure the wider business impact.” A modest precise result is more defensible than an invented metric.

### 19.5 A safe preparation exercise

Recall one real event. Ask only the first question now: **What happened, and what were you personally responsible for?** After answering, identify what evidence is available and what remains unknown. Build the story from those facts at your pace; no mandatory log or state update is needed.

No polished personal story is supplied here because the missing incident details cannot be filled confidently.

## Part 20: Common beginner failure modes

**P0 — MUST KNOW**

Use each pattern as **weak behavior → why it is weak → better reflex**.

### 20.1 Jumping directly to solutions

“Orders fell, so launch discounts.” This assumes demand is the problem and ignores fulfillment. First define the order measure and locate the changed stage.

### 20.2 Treating a feature request as the problem

“Users need automatic repair.” This embeds one answer before explaining the job. Ask what happened in the last failed-test investigation and what outcome was difficult.

### 20.3 Believing the first hypothesis

“Rain caused everything.” Several mechanisms can coexist, and timing alone does not prove cause. Name a competing explanation and the observation that separates them.

### 20.4 Listing metrics without causal reasoning

“I'll track retention, revenue, conversion, and engagement.” The list does not explain the decision. Pick the outcome, the mechanism you need to diagnose, and the harm you need to detect.

### 20.5 Forgetting segmentation

“The citywide driver count is stable, so supply is fine.” This hides local availability and time cycles. Compare the affected zone and meal period, then inspect how drivers spend their time.

### 20.6 Optimizing one marketplace side

“Give buyers the lowest fee.” Drivers still need compensation and merchants still need workable operations. Follow the effect through all sides and identify the payer and capacity constraints.

### 20.7 Ignoring economics

“Orders rose, so the campaign worked.” Orders may be expensive or non-incremental. Reconcile revenue and included costs, then compare total contribution with the counterfactual.

### 20.8 Assuming AI is always appropriate

“Let's add an agent.” Flexible action can introduce unnecessary failure points. Ask which part requires language interpretation or adaptive next steps, and compare a simpler baseline.

### 20.9 Treating confidence as certainty

“It is 99% confident, so it can execute.” The score may be uncalibrated and the error cost may be high. Verify relevant behavior and choose permissions from evidence and risk.

### 20.10 Ignoring meaningful human control

“Humans can approve everything.” Review can become confusing or automatic rubber-stamping. Put understandable approval at the decisions where it protects value, and enforce boundaries outside the prompt.

### 20.11 Ignoring second-order effects

“More incentives will solve the district shortage.” Drivers may leave neighboring areas. Ask where the added capacity comes from and measure the wider effect.

### 20.12 Overusing frameworks

Reciting nine labels can hide a weak next question. Use the underlying logic to explain one useful breakdown and the evidence it requires. The framework serves the problem.

### 20.13 Speaking at length without a recommendation

A long list of possibilities leaves the decision unresolved. Rank the explanations, choose a limited next step, name the main risk, and stop.

### 20.14 Pretending to know

Invented company policies, costs, or project achievements cannot survive follow-up. State what is known, what is assumed, and what evidence you would seek. Use hypothetical numbers only when clearly labeled.

### 20.15 Confusing a green test with a useful test

A weak assertion can pass while the application is wrong. Check what behavior the test protects and whether the generated or repaired test preserves that meaning.

### 20.16 Claiming causality from before and after

“Retention rose after launch, so the feature caused it.” Seasonality, different users, or other releases may explain the movement. Seek a credible comparison and state remaining uncertainty.

### 20.17 Hiding the denominator

“Cancellation improved by 5%.” The population, relative change, and status definition are unclear. State the numerator, denominator, period, and whether the change is percent or percentage points.

**Check yourself:** Which weak reflex appears in your own case attempts? Choose one and replace it with a concrete question in the next case.

## Part 21: Mini case walkthroughs

**P0 — MUST KNOW**

These are teaching demonstrations of observable analysis and decisions. They are not polished interview scripts. Each walkthrough has its own **ILLUSTRATIVE dataset**; do not merge the numbers or treat them as company facts. The useful habit is: **“I don't know the answer yet, so what question should I ask next?”**

### Walkthrough 1: Food-delivery orders dropped

**Try first:** Completed orders fell 20%. What is your first question, and why?

#### Step 1: Make the symptom precise

The case supplies this invented information: comparable weekly completed orders fell from 9,000 to 7,200 in one city. Reporting is complete and order definitions are unchanged.

**Decision implication:** The decline appears real within the case. Next separate placement from completion, because a discount addresses a different mechanism from a fulfillment repair.

#### Step 2: Request the decisive decomposition

The case supplies 10,000 placed orders in both weeks. Completion fell from 90% to 72%: 10,000 × 90% = 9,000; 10,000 × 72% = 7,200.

**Decision implication:** Fewer placements do not explain this particular decline. Investigate why already-placed orders fail to complete. This does not mean buyer behavior is irrelevant; buyers may cancel in response to fulfillment problems.

#### Step 3: Locate the affected workflow

Suppose the extra cancellations are concentrated at weekday lunch near several busy restaurants. Merchant acceptance and initial driver assignment time are stable. Pickup wait increased from a measured average of 6 to 18 minutes in that segment.

**Next question:** Are kitchens actually taking longer, or are drivers arriving too early because readiness information changed?

That comparison matters because the same waiting symptom can require either capacity changes or better coordination.

#### Step 4: Compare mechanisms

Suppose order-to-food-ready timestamps also increased and observation shows a kitchen queue. That supports an overload explanation more than early arrival alone. The evidence is local; it does not establish that every restaurant in the city has the same problem.

The hypothesis is now: concentrated lunch demand → overloaded preparation → longer pickup wait → later deliveries and cancellations. Check order timelines and cancellation reasons to see whether this chain explains a meaningful share of the loss.

#### Step 5: Recommend a bounded action

Work with operations and affected merchants on capacity and accurate availability for lunch. Depending on feasible options, limit overload, adjust promises, or direct buyers toward suitable available alternatives. Do not add a broad demand promotion while this constraint is unresolved.

**Trade-off:** Some immediate selection or merchant order attempts may decrease. The intended benefit is more reliable fulfillment of the orders accepted. Other merchants may receive more work, so monitor their capacity too.

#### Step 6: Define the learning result

Track completed orders, pickup wait, cancellation stage, merchant receipts, and contribution in the target segment and nearby areas. Compare suitable periods or a practical rollout comparison. If waiting improves but completion does not, investigate the remaining delivery or buyer-response stage.

**Transfer question:** If placed orders had fallen while completion stayed stable, how would your next request change?

### Walkthrough 2: Katalon AI adoption is low

**Try first:** Users try an AI test generator but rarely return. What does “adoption” need to mean before you diagnose it?

#### Step 1: Clarify opportunity to return

An invented cohort has 100 first users. During the next fourteen days, 40 have another relevant task, and 12 use AI again. The broad repeat share is 12%; repeat among users with another task is 30%.

**Decision implication:** Both numbers are informative, but they answer different questions. Some non-return is explained by opportunity. There is still a value question among the 40 eligible users. Confirm that the method for detecting another task is reliable and does not omit people working outside the product.

#### Step 2: Understand the first task

Suppose generated tests execute successfully in 95% of assessed attempts, and 70% of outputs are edited. These are synthetic observations, not Katalon performance figures.

**Next question:** What are the edits for? High execution success does not establish correct assertions; a high edit rate does not establish bad output.

#### Step 3: Classify evidence

Suppose six observed task sessions suggest many edits adapt setup and conventions. Comparable successful tasks take about 20 minutes including generation and review, versus 25 minutes manually.

**Decision implication:** AI appears to save 5 minutes on these observed tasks. The small sample suggests a mechanism but does not establish population prevalence or exclude failed-task costs. Removing review is not justified merely because most edits are conventions.

#### Step 4: Choose the smallest useful test

Hypothesis: supplying approved project examples → fewer repetitive convention edits → shorter review → greater useful task value.

With limited engineering capacity, test that context improvement on representative tasks. Compare assertions, edit categories, total effort, and failure handling against the current version. Keep human review while its error-detection role remains uncertain.

#### Step 5: State what would change the decision

If convention edits fall and total task effort improves without harmful assertion changes, broaden the trial and observe later eligible usage. If correct output already requires little effort but return remains low, investigate task relevance, integration, and access instead.

If the feature saves time only for one project type, a segment-specific experience may make more sense than forcing the same workflow on everyone.

#### Step 6: Avoid a premature conclusion

The recommendation is a test of a causal mechanism. It is not “templates will solve adoption.” The missing evidence is whether that mechanism is common enough and whether improved task value changes repeated use.

**Transfer question:** If edits mainly corrected wrong business assertions, why would a convention template be an insufficient first response?

### Walkthrough 3: An AI agent is proposed to have more autonomy

**Try first:** Engineering says approvals make the agent slow. What must you know before removing them?

#### Step 1: Recover the goal

The goal is faster useful QA work with acceptable reliability and control. “More autonomy” is an option. Ask which actions and which delays are involved.

#### Step 2: Separate waiting from checking

Suppose a hypothetical task spends 12 minutes in the approval stage: 9 waiting for a reviewer and 3 actively reviewing. The total approval stage is large, but removing useful checking is not the only way to reduce it.

**Next question:** What errors does the three-minute review catch, and why does the nine-minute wait occur?

The wait might reflect unclear ownership, notification delays, required senior approval, or reviewer availability. Those mechanisms suggest different interventions.

#### Step 3: Split the action classes

Reading authorized CI results is different from drafting a locator change. Both differ from changing an expected payment amount in a shared release suite.

Suppose existing evidence is strongest for authorized reads and controlled drafts. There is no reliable estimate of harmful assertion changes.

**Decision implication:** Use the available evidence only for the action class it supports. Do not generalize from harmless drafts to shared writes.

#### Step 4: Compare options

One option is automatic execution of well-defined low-risk actions under policy. Another is a clearer reviewer assignment and notification path for higher-risk changes. A third is better presentation so review becomes easier. Compare these against the actual waiting and error mechanisms.

Hypothesized chain: clearer review ownership → less queue time → faster task completion while preserving meaningful inspection. A possible downside is interrupting reviewers more often, so measure their workload too.

#### Step 5: Recommend and protect the boundary

Trial the supported low-risk actions and improve review routing for higher-risk edits. Use shadow proposals to gather evidence on broader action classes. Require concrete review where correctness, reversibility, or scope remains uncertain.

Track task time, review effort, caught errors, incorrect actions, interruptions, and recovery. An average time improvement is insufficient if the change begins to hide serious defects.

**Transfer question:** If a test edit can be reverted, what downstream consequences might still make automatic application risky?

### Walkthrough 4: Driver supply shortage

**Try first:** Lunch orders wait for drivers even though the online driver count is unchanged. What would you inspect next?

#### Step 1: Define effective capacity

Available people and productive time are different. A driver is occupied by pickup travel, waiting, delivery, and repositioning. Ask where the cycle has changed, in the affected location and period.

#### Step 2: Use a rough model, with assumptions visible

**ILLUSTRATIVE simplification:** Suppose 60 drivers each provide one usable hour in the district. Total driver time is 60 hours. Ignore batching and assume that all this time can be allocated to comparable order cycles.

At 30 minutes per order, the rough upper-bound throughput is 60 hours ÷ 0.5 hour = 120 orders. At 40 minutes, it is 60 ÷ two-thirds of an hour = 90 orders. The same people can support fewer completions because each order occupies more time.

This is a teaching model, not a precise operational forecast. Positioning, idle buffers, variable trips, and matching can reduce practical throughput.

#### Step 3: Locate the extra time

Suppose lunch demand is 120 orders, average pickup waiting rose by 10 minutes, and other cycle stages stayed similar. Preparation congestion becomes a plausible explanation for the capacity loss.

**Next question:** Would more drivers reduce the waiting, or would they join the same restaurant queues?

Ask for food-ready and driver-arrival timestamps and inspect the most affected merchants. Separate real kitchen overload from inaccurate readiness estimates.

#### Step 4: Choose the mechanism to change

If the kitchen is overloaded, work on manageable order load and preparation operations. If readiness information is wrong, improve pickup coordination. Add targeted supply support only where drivers are actually unavailable after considering these causes.

The intended chain is less unproductive waiting → shorter cycles → more effective capacity → better completion. Possible downstream effects include more demand at newly reliable merchants and a new bottleneck in delivery travel.

#### Step 5: Leave room for uncertainty and surges

Returning the simplified cycle to 30 minutes produces a theoretical 120-order capacity, equal to demand. That leaves no buffer in the model. Real variation means the team may still need additional capacity, demand management, or more realistic promises.

Track cycle components, completed orders, severe waits, driver earnings per online hour, merchant load, contribution, and neighboring coverage. If pickup waiting improves but assignment remains poor, reassess positioning and available supply.

**Transfer question:** Why might maximizing driver utilization make the lunch service fragile even when average earnings look good?

## Part 22: Concept comparisons

**P0 — MUST KNOW**, except the fine-tuning comparison marked P2. Use these distinctions to explain a decision, not just recite definitions.

### Problem versus symptom

A symptom is an observed signal; a problem is an important gap in an outcome. “Completed orders fell” is a symptom. “Buyers cannot receive lunch reliably in this zone” is a possible problem framing that still needs evidence.

### Problem versus solution

A problem describes what prevents progress. A solution proposes how to improve it. Slow failure diagnosis is a problem; an AI investigation assistant is one possible solution. Better linked logs might be another.

### Assumption versus hypothesis

An assumption is a premise not yet sufficiently checked. A hypothesis is a claim made testable through predicted observations. “Users have another task” is an assumption; “users do not return because their task is monthly” suggests a comparison with actual task frequency.

### Hypothesis versus fact

A hypothesis is a possible explanation. A fact is supported within a defined scope. “Pickup wait rose in these orders” can be an observed fact; “kitchen overload caused the rise” requires further evidence.

### User versus customer

A user interacts with the product. A customer buys or pays for it. A QA engineer may use software purchased by a company through a department lead. Their needs overlap but can differ.

### Metric versus goal

A goal describes the desired outcome. A metric measures something relevant to it. Reliable lunch delivery is a goal; on-time completion is one measure. A metric can improve without fully achieving the goal.

### Primary metric versus guardrail

A primary metric judges the intended improvement. A guardrail detects important harm. Completed orders may be primary for a promotion; contribution and cancellation can constrain whether the increase is acceptable.

### Correlation versus causation

Correlation is a relationship in observed movement. Causation concerns what changes because of an intervention or mechanism. More incentives and more orders may both occur in busy districts without proving incentives created the demand.

### AI versus LLM

AI is the broad field; an LLM is a particular kind of model. A structured ETA predictor can be AI without being a language model. Interpreting a messy requirement may be an LLM task.

### RAG versus fine-tuning

**P2 — OPTIONAL DEPTH.** RAG supplies retrieved information during use. Fine-tuning changes model behavior through further training. Current requirements and repeated output style are different needs; the approaches can complement each other.

### Tool calling versus agent

Tool calling enables an operation. An agent chooses actions over a task as observations arrive. Reading one CI result is a tool call; deciding which evidence to inspect next may be agent behavior.

### Agent versus workflow

In this comparison, a fixed workflow follows predefined steps; an agent chooses more of the route dynamically. A fixed process can still contain AI. Choose flexibility when the task actually needs changing next steps.

### MCP versus direct API

MCP offers a common connection model for AI applications; direct integration uses a service's specific interface. A server may itself call APIs. Compare actual task coverage and ownership rather than treating the choices as mutually exclusive.

### Automation versus AI

Automation executes work with reduced manual effort. It can follow explicit rules without AI. AI can interpret uncertain input but may produce only advice. A scheduled regression run can be automated without using an LLM.

### Confidence versus correctness

Confidence is an estimate or expression of certainty. Correctness is whether the output satisfies the relevant truth or task criteria. A confident failure diagnosis can still contradict the current requirement.

### Manual testing versus automated testing

A person performs manual checks or exploration; software performs automated checks. Both need sound expectations. Manual exploration may find confusing recovery behavior; automation can repeatedly verify a stable coupon rule.

### Unit versus integration versus E2E

Unit checks a small isolated part; integration checks parts together; E2E checks a whole journey. Correct discount calculation does not prove the payment adapter receives the amount or the buyer gets confirmation.

### Growth versus profitability

Growth increases an activity or business scale. Profitability concerns income exceeding relevant costs. Orders can grow through subsidy while contribution falls. State the horizon and costs before judging business health.

### GMV versus revenue

GMV counts defined transaction value. Revenue counts the platform's defined income. In the hypothetical order, food GMV is 100,000 VND, while gross platform revenue before voucher is 40,000 VND.

### Revenue versus contribution margin

Revenue is income before the included variable costs are deducted. Contribution is what remains after those costs. In the hypothetical order, 40,000 VND revenue minus 35,000 VND included costs leaves 5,000 VND contribution.

### First-order versus second-order effect

A first-order effect is close to the intervention. A second-order effect follows through another behavior or constraint. An incentive may attract drivers to a zone; their departure from neighboring zones may reduce service there.

### Extra useful distinctions

**Acceptance versus correctness:** People can accept wrong AI suggestions. **Pass rate versus defect detection:** Tests can pass because checks are weak. **Quoted ETA versus actual duration:** A better estimate can rise without deliveries getting slower. **Driver assignment cancellation versus order cancellation:** Reassignment may preserve the buyer's order. Each distinction changes the measurement and decision.

## Part 23: Glossary

Each entry has a priority, plain-English definition, and short **illustrative example**. These are concise recall cues; the earlier parts teach how the ideas work together.

### Foundation and discovery terms

- **Product management — P0:** Helping a team choose valuable problems and judge outcomes. **Example:** Prioritize failure diagnosis after observing tester effort.
- **User problem — P0:** An obstacle to a person's desired outcome. **Example:** Cannot distinguish a bug from a broken test.
- **Business problem — P0:** An obstacle to a business outcome. **Example:** Declining completed orders.
- **Symptom — P0:** An observable signal requiring interpretation. **Example:** Repeat use falls.
- **Root cause — P0:** An underlying mechanism explaining a problem at a useful level. **Example:** Stale stock causes rejected orders.
- **Goal — P0:** The outcome to improve. **Example:** More reliable lunch completion.
- **Constraint — P0:** A limit on possible action or output. **Example:** One engineer available this week.
- **Bottleneck — P0:** The step most limiting current throughput. **Example:** An overloaded kitchen.
- **Segment — P0:** A group sharing a decision-relevant trait. **Example:** First-time automation users.
- **Customer — P0:** The buying or paying party. **Example:** A company purchasing testing software.
- **User — P0:** The person interacting with the product. **Example:** A tester reviewing output.
- **Pain point — P0:** A specific difficulty in a workflow. **Example:** Repeatedly searching for logs.
- **Need — P0:** What is required to make progress. **Example:** Reliable evidence before release.
- **Feature request — P0:** A proposed product behavior. **Example:** “Add automatic repair.”
- **Workflow — P0:** Actions and handoffs used to complete a job. **Example:** Create, review, and run a test.
- **Workaround — P0:** An alternative method used to overcome friction. **Example:** Copying logs into a shared document.
- **JTBD — P1:** The progress wanted in a situation. **Example:** Diagnose failure before a release decision.
- **Persona — P1:** An evidence-based description of a relevant user group. **Example:** A QA lead with shared-project responsibility.
- **Requirement — P0:** Intended behavior or a constraint to satisfy. **Example:** Failed payment must not confirm an order.
- **Acceptance criterion — P0:** An observable condition for meeting a requirement. **Example:** Rejecting a suggestion leaves the file unchanged.
- **Product spec — P1:** A shared description of problem, behavior, boundaries, and measures. **Example:** A single-test review feature specification.
- **Opportunity cost — P1:** The alternative value forgone by a choice. **Example:** Agent work delays a setup fix.

### Evidence and metric terms

- **Assumption — P0:** A premise used without enough verification. **Example:** Every user has a weekly task.
- **Hypothesis — P0:** A testable explanation or prediction. **Example:** Missing conventions cause lengthy edits.
- **Evidence — P0:** Information supporting or challenging a claim. **Example:** Observed edits and task durations.
- **Validation — P0:** Gathering evidence for a particular decision. **Example:** Test whether users can review a prototype.
- **Qualitative evidence — P0:** Information about experiences and mechanisms. **Example:** A recent-incident interview.
- **Quantitative evidence — P0:** Numerical observations of activity or outcomes. **Example:** Completion rate by district.
- **Correlation — P0:** Two measures vary together. **Example:** Incentives and orders rise together.
- **Causation — P0:** One change contributes to another. **Example:** A verified checkout bug prevents order creation.
- **Counterfactual — P0:** What would happen without the intervention. **Example:** Expected orders without a voucher.
- **Confounder — P1:** A factor affecting both the suspected cause and outcome. **Example:** High demand drives incentives and orders.
- **Baseline — P0:** The reference performance for comparison. **Example:** Current manual task time.
- **Metric — P0:** A defined measurement. **Example:** Completed orders per week.
- **Denominator — P0:** The reference count in a rate. **Example:** Placed orders in cancellation rate.
- **Funnel — P0:** Defined stages toward an outcome. **Example:** Visit, checkout, placement, completion.
- **Metric tree — P0:** An outcome broken into related components. **Example:** Placements multiplied by completion rate.
- **Input metric — P0:** A condition or activity that can influence outcomes. **Example:** Available driver hours.
- **Output metric — P0:** A measured result. **Example:** Successfully delivered meals.
- **Leading indicator — P1:** An earlier signal of a later result. **Example:** Useful first-task completion before repeat use.
- **Lagging indicator — P1:** An outcome measured after the process. **Example:** Monthly retention.
- **Primary metric — P0:** The main result judging a decision. **Example:** Useful tasks completed.
- **Supporting metric — P0:** A measure helping explain the result. **Example:** Review abandonment.
- **Guardrail metric — P0:** A measure detecting important harm. **Example:** Harmful automatic edits.
- **Vanity metric — P0:** An impressive count with weak value evidence in context. **Example:** Generations inflated by retries.
- **Cohort — P1:** A group sharing a defined starting event or time. **Example:** First users from one week.
- **Percentage point — P0:** The arithmetic difference between percentages. **Example:** 20% to 16% is down four points.
- **Percentile — P1:** A position in an ordered distribution. **Example:** p90 shows the slower delivery tail.
- **Spillover — P1:** Treatment affects people or resources outside its intended group. **Example:** Drivers move from a control district.
- **Switchback experiment — P2:** Alternating treatment across defined time periods. **Example:** Compare comparable lunch windows under two policies.

### Testing and AI terms

- **QA — P0:** Practices supporting software quality. **Example:** Clarifying checkout acceptance criteria.
- **Test case — P0:** Conditions, actions, and expected results for a check. **Example:** Reject an expired coupon.
- **Test suite — P0:** A group of related test cases. **Example:** Checkout regression checks.
- **Assertion — P0:** A specific check of expected behavior. **Example:** Exactly one order is created.
- **Manual testing — P0:** Checks or exploration performed by a person. **Example:** Explore payment recovery messages.
- **Automated testing — P0:** Checks executed by software. **Example:** Repeated coupon validation.
- **Unit test — P0:** A check of a small part in isolation. **Example:** Discount calculation.
- **Integration test — P0:** A check of parts working together. **Example:** Order service and payment adapter.
- **API test — P0:** A check through a programmatic interface. **Example:** Verify order creation response and effects.
- **UI test — P0:** A check through the visible interface. **Example:** Verify the coupon error is shown.
- **E2E test — P0:** A check across a complete journey. **Example:** Browse through payment confirmation.
- **Regression testing — P0:** Checking existing behavior after change. **Example:** Recheck payments after coupon edits.
- **Flaky test — P0:** A test with inconsistent results under apparently unchanged conditions. **Example:** A timing-sensitive confirmation check.
- **Test maintenance — P0:** Keeping tests aligned and usable. **Example:** Update a locator after an approved UI change.
- **Test coverage — P0:** What behavior, risks, or code tests check or exercise. **Example:** Include duplicate-payment risk.
- **Bug or defect — P0:** A flaw in software or an artifact. **Example:** Checkout charges twice.
- **Failure diagnosis — P0:** Determining the best-supported explanation of a failure. **Example:** Separate bad data from a product bug.
- **CI/CD — P1:** Frequent integration and checks, with delivery or deployment processes. **Example:** Run regression checks on a proposed change.
- **AI — P0:** Systems performing tasks associated with intelligence. **Example:** Predict delivery duration.
- **Machine learning — P0:** Learning patterns from data. **Example:** Learn travel-time relationships.
- **LLM — P0:** A large model that works with and generates token sequences. **Example:** Explain failure evidence.
- **Token — P0:** A unit processed by a model. **Example:** A word fragment in a requirement.
- **Context window — P0:** Bounded material available for a model call. **Example:** Requirement and selected logs.
- **Prompt — P0:** Instructions and information supplied to a model. **Example:** Request tests grounded in a requirement.
- **Hallucination — P0:** False or unsupported plausible output. **Example:** An invented API.
- **Grounding — P0:** Connecting output to relevant evidence. **Example:** Link an assertion to its requirement.
- **Structured output — P0:** Output following a defined format. **Example:** Diagnosis, evidence, and uncertainty fields.
- **RAG — P0:** Retrieve material and supply it for generation. **Example:** Find the current coupon rule.
- **Tool calling — P0:** Request an operation through an exposed capability. **Example:** Read an authorized CI run.
- **Agent — P0:** A system selecting actions as observations arrive. **Example:** Choose the next failure evidence to inspect.
- **MCP — P0:** A common protocol for AI applications to access exposed context and capabilities. **Example:** Connect to permitted testing evidence.
- **Human-in-the-loop — P0:** Meaningful human involvement at a decision point. **Example:** Review a proposed assertion change.
- **Autonomy — P0:** How much a system acts without intervention. **Example:** Execute only approved low-risk actions automatically.
- **Permission — P0:** Authorization for a defined resource or action. **Example:** Read this project but do not edit it.
- **Reversibility — P0:** Ability to undo an action and recover consequences. **Example:** Discard an unapplied test draft.
- **Observability — P0:** Evidence showing actions and system state. **Example:** Tool result and applied change history.
- **AI evaluation — P0:** Checking task quality, actions, value, and operating behavior. **Example:** Test repairs against known defects.
- **Calibration — P1:** Confidence estimates matching observed correctness. **Example:** Check stated confidence against labeled outcomes.
- **Latency — P0:** Time spent waiting for a response or outcome. **Example:** Waiting for generation to finish.
- **False positive — P1:** Signalling a problem when behavior is acceptable. **Example:** A correct payment produces a false alarm.
- **False negative — P1:** Missing a real problem. **Example:** A test misses duplicate charging.
- **Fine-tuning — P2:** Further training to adjust model behavior. **Example:** Learn a repeated output style from examples.

### Marketplace, systems and economics terms

- **Marketplace liquidity — P0:** Ability to match demand with suitable fulfillable supply. **Example:** A meal and driver available at lunch.
- **Demand — P0:** Willingness to request the service under given conditions. **Example:** Lunch order attempts at a stated price.
- **Supply — P0:** Relevant available capacity or offerings. **Example:** Nearby drivers and ready kitchens.
- **Conversion — P0:** A defined action per eligible opportunity. **Example:** Orders per eligible session.
- **Frequency — P0:** Actions per defined user in a period. **Example:** Monthly orders per ordering buyer.
- **Retention — P0:** A cohort returning for meaningful use later. **Example:** Buyers ordering again next month.
- **Merchant availability — P0:** Whether relevant meals can be offered and fulfilled. **Example:** Open kitchen with items in stock.
- **Acceptance rate — P0:** Accepted items divided by defined eligible requests or offers. **Example:** Merchant accepted orders per incoming order.
- **Preparation time — P0:** Time until food is ready from a defined start. **Example:** Acceptance to pickup readiness.
- **Utilization — P1:** Busy or productive time as a share of defined available time. **Example:** Driver busy minutes per online hour.
- **Idle time — P1:** Available time without an active task under the definition. **Example:** Waiting for an order offer.
- **Pickup wait — P0:** Time at the merchant before collecting food. **Example:** Driver waits for cooking to finish.
- **ETA — P0:** Estimated time of arrival. **Example:** A promised delivery window.
- **Cancellation — P0:** Termination of a defined order or assignment. **Example:** An unfulfilled buyer order ends.
- **GMV — P0:** Transaction value under a stated definition. **Example:** 100,000 VND food value in Part 16.
- **Revenue — P0:** Defined income to the business. **Example:** Commission and included fees.
- **Take rate — P0:** Defined revenue divided by corresponding GMV. **Example:** Specify gross or net revenue first.
- **Merchant commission — P0:** A platform charge to the merchant. **Example:** The invented 20,000 VND charge in Part 16.
- **Delivery fee — P0:** The buyer's delivery charge. **Example:** It can differ from driver compensation.
- **Subsidy — P0:** Funding for a participation or price benefit. **Example:** A platform-funded voucher.
- **Incentive — P0:** A reward intended to change behavior. **Example:** A lunch availability bonus.
- **Variable cost — P0:** A cost changing with the modeled activity. **Example:** Driver compensation per fulfilled order.
- **Contribution margin — P0:** Revenue minus included variable costs. **Example:** 5,000 VND remains in Part 16.
- **Unit economics — P0:** Income and cost for one defined unit. **Example:** Economics of a completed order.
- **Incrementality — P0:** Change beyond what would otherwise happen. **Example:** Extra orders caused by a voucher.
- **Trade-off — P0:** A benefit requiring a cost or risk elsewhere. **Example:** Faster approval versus less review.
- **First-order effect — P0:** A direct response near the intervention. **Example:** A discount lowers buyer payment.
- **Second-order effect — P0:** A downstream response through the system. **Example:** Extra demand creates pickup queues.
- **Feedback loop — P1:** A chain returning to influence its starting condition. **Example:** Reliability encourages demand that changes capacity.

## Part 24: Active recall question bank

**P0 — MUST KNOW**, with selected P1 extensions. These questions test understanding. For a practice session, use one at a time, attempt an answer, then request feedback. The brief answer cues after the bank are for checking, not memorizing. More than one defensible action may exist if the reasoning and conditions are clear.

### Foundation

1. **F1:** Why is “orders dropped 20%” a symptom rather than a complete problem statement?
2. **F2:** A stakeholder requests automatic repair. What question would reveal the underlying need?
3. **F3:** Turn “increase AI autonomy” into an outcome goal with one constraint.
4. **F4:** How is a testable hypothesis different from an assumption?
5. **F5:** Why might observing the last real task be more useful than asking whether someone likes a feature?
6. **F6:** A proposed solution is technically impressive but saves time in a minor workflow stage. What would you investigate before prioritizing it?

### Katalon

1. **K1:** Users edit many generated tests. What evidence distinguishes useful customization from incorrect output?
2. **K2:** Generated tests run successfully but miss important defects. Which outcome is missing from the evaluation?
3. **K3:** A customer asks for unattended changes across projects. What must be clarified before discussing autonomy?
4. **K4:** Users distrust accurate output. Which verification or control problems could still explain their behavior?
5. **K5:** Give one testable acceptance criterion and one failure behavior for accepting an AI-proposed test change.
6. **K6:** First use is high and repeat use is low. Why must you check whether users had another relevant task?

### AI

1. **A1:** Why might an ETA predictor and a failure-report explainer use different types of AI?
2. **A2:** The assistant lacks the current requirement. What can better context or retrieval fix, and what does it not guarantee?
3. **A3:** What happens between a model requesting a tool call and an external action actually completing?
4. **A4:** When would choosing the next evidence source justify an agent rather than a fixed workflow?
5. **A5:** Why might a product use MCP when connecting several AI applications to the same capabilities, and when might direct APIs be simpler?
6. **A6:** Why is a model's stated confidence insufficient to authorize a high-impact action?

### Testing

1. **T1:** A payment test fails. Name three explanations other than an application bug and one check for each.
2. **T2:** Explain the difference between checking a discount function and testing checkout through confirmation.
3. **T3:** Can an API test also be an integration test? Explain using payment.
4. **T4:** Why can automated repair make the test report better while making release risk worse?
5. **T5:** How could code coverage be high while duplicate charging remains undetected?
6. **T6:** A flaky test passes after three reruns. What is still unresolved?

### ShopeeFood

1. **S1:** Completed orders fall while placed orders stay stable. Which part of the investigation comes next?
2. **S2:** Rain coincides with rider cancellations. Why should assignment cancellation and order cancellation be measured separately?
3. **S3:** Quoted ETA rises while actual delivery time stays stable. What alternative to “operations got slower” should you consider?
4. **S4:** Merchant non-response rises on one device version. What evidence would separate notification failure from low willingness to accept?
5. **S5:** A promotion raises orders and lowers contribution. Under what conditions might a bounded continuation still be defensible?
6. **S6:** One district grows while another falls during an incentive. What movement between districts should you investigate?

### Metrics

1. **M1:** Why can “sessions × conversion × frequency” double-count orders?
2. **M2:** What five things should be defined before interpreting a repeat-use rate?
3. **M3:** Traffic falls from 10,000 to 8,000 sessions and conversion rises from 20% to 22%. Under a one-order-per-session model, do placed orders rise?
4. **M4:** Conversion falls from 20% to 16%. State the percentage-point and relative changes.
5. **M5 — P1:** Why might an improved average delivery time hide a worse experience for some buyers?
6. **M6:** Choose one primary, one supporting, and one guardrail metric for an AI review improvement. Explain each role.

### Marketplace

1. **MP1:** Why can a city have many registered drivers but poor lunch liquidity?
2. **MP2:** Follow a free-delivery offer through one possible capacity effect and one economic effect.
3. **MP3:** How can longer kitchen preparation reduce delivery capacity without changing driver count?
4. **MP4:** Why can easier merchant onboarding increase listed supply without improving buyer outcomes?
5. **MP5 — P1:** How can a user-level promotion experiment affect its own control group?
6. **MP6:** What happens next if an incentive attracts drivers from a neighboring zone instead of adding new available hours?

### Unit economics

1. **U1:** Why is food GMV different from the platform's revenue?
2. **U2:** In Part 16, reconcile the buyer's 110,000 VND payment across merchant, driver, other costs, and platform contribution.
3. **U3:** Why should a voucher recorded as reduced revenue not also be deducted again as a cost?
4. **U4:** How can order volume rise 40% while total contribution falls in the hypothetical promotion example?
5. **U5:** Why is a redeemed promoted order not automatically incremental?
6. **U6:** Why can the merchant receive more order volume or the driver receive more per order without earning more overall?

### Product judgment

1. **J1:** What would make you choose deterministic logic instead of an LLM?
2. **J2:** Why does reversibility depend on downstream consequences as well as undoing a file edit?
3. **J3:** Human approvals take twelve minutes, but nine are waiting. What alternatives should be considered before removing review?
4. **J4:** A stronger model is more accurate but slower and costlier. What user-level evidence should guide the decision?
5. **J5:** Your preferred hypothesis is contradicted by new evidence. How should your recommendation change?
6. **J6:** What makes a recommendation concrete enough to evaluate even when some data is missing?

### Answer cues: read after attempting

These cues identify essential reasoning. They are not full case answers.

**Foundation:** F1 needs definition, affected user, impact, and mechanism. F2 asks about a recent failure, actions, and consequences. F3 targets useful effort or speed with reliability/control constraints. F4 needs predicted observable evidence. F5 reveals actual behavior and trade-offs, with memory limits. F6 checks the end-to-end bottleneck and opportunity cost.

**Katalon:** K1 classifies edits against requirements and conventions. K2 needs meaningful defect detection, not execution alone. K3 clarifies job, scope, actors, authorization, and error costs. K4 considers inspectable evidence, predictable actions, and policy obligations. K5 can use unchanged files on rejection, exact-change acceptance, and visible conflict handling. K6 distinguishes lack of opportunity from lack of value.

**AI:** A1 distinguishes structured prediction from language interpretation. A2 supplies relevant facts but still needs source and answer verification. A3 requires validation, permission, execution, result observation, and recovery. A4 needs variable next steps that create user value. A5 weighs reuse against narrow control and maintenance. A6 requires calibrated evidence, verification, and consequence-aware boundaries.

**Testing:** T1 can use test, data, environment, or dependency checks. T2 compares narrow isolation with the complete integrated journey. T3 yes: the interface and scope describe different dimensions. T4 a repair can weaken expected behavior. T5 executing code does not guarantee the right assertion. T6 the intermittent cause and product risk remain unresolved.

**ShopeeFood:** S1 investigates completion stages and affected segments. S2 reassignment may preserve the buyer's order. S3 estimates may be more accurate or the mix may differ. S4 checks delivery and acknowledgement logs plus actual merchant behavior. S5 needs an explicit objective, budget, counterfactual, and credible later value test. S6 traces demand and usable driver capacity across boundaries.

**Metrics:** M1 session conversion may already count order production. M2 defines population, event, denominator, window, and comparison. M3 no: 2,000 becomes 1,760, down 12%. M4 down four percentage points and 20% relatively. M5 examines tails, segments, and changed mix. M6 could use correct completed reviews, review time, and harmful changes applied, tied to the stated goal.

**Marketplace:** MP1 needs location, time, willingness, and cycle capacity. MP2 traces subsidized demand into cost and possible queues. MP3 drivers become occupied waiting. MP4 listed meals may not be fulfillable or reliable. MP5 groups share kitchens and drivers. MP6 neighboring service may worsen; evaluate net system effects.

**Economics:** U1 the platform does not retain the full food value. U2 is 80,000 + 22,000 + 3,000 + 5,000. U3 avoids double-counting the same subsidy. U4 140 × 5,000 is below 100 × 15,000. U5 asks what would otherwise happen, including shifted demand. U6 considers costs, discounts, waiting, and productive time.

**Judgment:** J1 stable explicit rules may be adequate and easier to verify. J2 an edit can affect releases or expose data before undo. J3 consider queue ownership, notifications, clear reviews, and action classes. J4 compare useful completion and total effort, latency, and cost by task. J5 update openly and seek the new decisive comparison. J6 specifies scope, action, rationale, owner, evaluation, risk, and change condition.

## Part 25: Flashcard-ready facts

**P0 — MUST KNOW**

These cards focus on reasoning moves. The glossary provides terminology, so these do not repeat every definition.

### What should come before proposing a feature?

**Answer:** Establish the user, job, obstacle, impact, and evidence.

**Example:** Investigate the last failed-test task before proposing automatic repair.

### What turns a hypothesis into a useful investigation?

**Answer:** A predicted observation that distinguishes it from another explanation.

**Example:** Compare wrong assertions with harmless convention edits.

### What question connects a goal to a guardrail?

**Answer:** What are we improving, and what must not become materially worse?

**Example:** Increase completed orders while protecting reliability and contribution.

### Why define placed and completed orders separately?

**Answer:** They separate order creation from successful fulfillment.

**Example:** Stable placement with lower completion points toward later stages.

### When can frequency be multiplied into an order tree?

**Answer:** When it is not already counted by the other factors and definitions match.

**Example:** Ordering buyers × orders per ordering buyer is compatible.

### Why is editing AI output not automatically a failure?

**Answer:** Edits can be useful customization or required correctness repairs.

**Example:** Project naming changes differ from fixing a wrong payment assertion.

### Why does a passing generated test need further evaluation?

**Answer:** Execution success does not prove it checks meaningful behavior.

**Example:** Opening checkout does not check duplicate charging.

### What is the first rule of test repair?

**Answer:** Establish whether the application, test, data, or environment is wrong.

**Example:** Preserve a failing assertion that correctly detects a defect.

### What does RAG fail to guarantee?

**Answer:** Correct retrieval, current sources, and accurate use of evidence still need checking.

**Example:** A retrieved old requirement can support the wrong test.

### When is an agent useful?

**Answer:** When choosing changing next steps is part of a valuable task.

**Example:** Select logs or recent code changes based on failure evidence.

### What does MCP not decide for the product?

**Answer:** Whether a task is useful, an action is appropriate, or access should be allowed.

**Example:** A connection does not authorize editing every project.

### What should happen after an uncertain write timeout?

**Answer:** Check whether the operation completed before retrying.

**Example:** Inspect the saved test to avoid applying the same change twice.

### Why can full rollback still leave harm?

**Answer:** Downstream consequences may already have occurred.

**Example:** A weakened test may have supported a release before being restored.

### What makes human review meaningful?

**Answer:** The reviewer can understand the concrete action, evidence, scope, and uncertainty.

**Example:** Show the assertion change and its requirement before approval.

### What is missing from “the AI saves 23 minutes of generation”?

**Answer:** Setup, review, correction, retries, and failed-task effort.

**Example:** Two-minute generation plus eighteen other minutes saves five against a twenty-five-minute baseline.

### Why is registered driver count a weak capacity measure?

**Answer:** Availability depends on time, location, acceptance, and the whole trip cycle.

**Example:** Drivers waiting at kitchens cannot immediately take new work.

### Why is free delivery still costly?

**Answer:** Removing the buyer's charge does not remove delivery expense.

**Example:** Someone must fund driver compensation and other service costs.

### How should a promotion be judged economically?

**Answer:** Compare incremental total contribution and relevant later value against a credible counterfactual.

**Example:** Include discounts paid on orders that would happen anyway.

### What does “and then what happens?” add?

**Answer:** It reveals downstream behavior, constraints, and unintended effects.

**Example:** More lunch demand may increase kitchen queues and driver waiting.

### What should never fill a missing behavioral story?

**Answer:** Invented actions, metrics, customer outcomes, or project capabilities.

**Example:** Mark an unverified PRJ226 achievement as PERSONAL EVIDENCE REQUIRED.

## Part 26: Audio-ready recaps

**P0 — MUST KNOW**

These standalone recaps repeat the central mental models in conversational form. Each includes an example, a common mistake, and a question. Shorter recaps also appear at the ends of the main teaching domains.

### PM Thinking Recap

A PM helps the team decide which problem deserves attention. Imagine a customer asking for a button to fix every failed test. The button is a proposed answer. The real need might be understanding failures before a release. Start with the job, obstacle, and consequence, then ask what evidence supports them. The common mistake is jumping from a request to a feature. Ask yourself: what outcome is difficult today, and could several solutions address it?

### AI Product Judgment Recap

Imagine an assistant proposing a test change. It may need current requirements, tools to inspect evidence, and an agent loop to choose its next step. None of that proves it should apply every change automatically. Compare value with error cost, verification, reversibility, and control. The common mistake is treating more autonomy as automatic progress. Ask yourself: what can this action improve, what happens if it is wrong, and how will we know it completed correctly?

### Testing Recap

Follow a buyer from product browsing through checkout and confirmation. A small calculation test checks one part; an end-to-end test checks the journey. Both need meaningful expected results. If an automatic repair removes the duplicate-charge assertion, the suite may turn green while buyers become less protected. The common mistake is equating a pass with quality. Ask yourself: what risk does this test detect, and did the proposed repair preserve that protection?

### Marketplace Recap

A completed lunch order needs a willing buyer, a ready merchant, and usable delivery capacity. Those conditions must meet in the same place and time. A promotion can attract demand but also overload a kitchen and trap drivers in pickup queues. That is a possible chain to test, not a guaranteed result. The common mistake is optimizing only the buyer's price or the driver's count. Ask yourself: who responds next, and where could the constraint move?

### Metrics Recap

Metrics help you locate a change; they do not explain it by themselves. If visits fall but conversion improves, orders can still decline. If generated tests pass, they may still miss defects. Define the population, event, denominator, window, and comparison, then break the outcome into compatible parts. The common mistake is celebrating a number without checking the job. Ask yourself: could this metric improve while the actual user outcome gets worse?

### Unit Economics Recap

In the invented food order, the buyer's payment must cover merchant receipts, driver compensation, other included costs, and what remains for the platform. The full food value is GMV; only defined income is revenue. After included variable costs, the remainder is contribution, not total company profit. The common mistake is assuming more orders automatically make the business healthier. Ask yourself: who funds the discount, what is left per order, and which orders would happen without it?

### Interview Communication Recap

You can think clearly in simple English. Clarify one important ambiguity, offer a small structure, and explain what evidence would change your action. Then recommend something within the information available. If the evidence changes, update your view. The common mistake is speaking for several minutes without choosing a next step. Ask yourself: can the listener identify my recommendation, its main reason, its main risk, and what would make me change it?

## Sources and evidence boundaries

### Repository sources used for the synthesis

This source synthesizes the existing learner-facing notes and adds clearly labeled teaching examples. The original files remain available for focused study and preserve their research and evidence separately.

- [README](README.md) and [roadmap](pm-interview-bootcamp/ROADMAP.md): learning scope and learner-controlled pace.
- [Product thinking](pm-interview-bootcamp/study/PRODUCT_THINKING.md), [customer discovery](pm-interview-bootcamp/study/CUSTOMER_DISCOVERY.md), and [testing](pm-interview-bootcamp/study/TESTING_FOR_PM.md): foundational explanations and workflow distinctions.
- [AI, agents and MCP](pm-interview-bootcamp/study/AI_AGENTS_MCP.md) and [marketplace thinking](pm-interview-bootcamp/study/MARKETPLACE_FOR_PM.md): technical and marketplace mental models.
- [Katalon cases](pm-interview-bootcamp/katalon/CASES.md) and [ShopeeFood cases](pm-interview-bootcamp/shopeefood/CASES.md): hypothetical practice themes. Some numerical teaching observations are adapted from existing synthetic follow-ups.
- [English phrase bank](pm-interview-bootcamp/english/phrase-bank.md) and [quick review](pm-interview-bootcamp/QUICK_REVIEW.md): concise communication and recall patterns.
- [Evidence ledger](pm-interview-bootcamp/stories/evidence-ledger.md) and [story bank](pm-interview-bootcamp/stories/story-bank.md): candidate claim boundaries. Broad self-report is kept distinct from independently verified experience.
- [Katalon research](pm-interview-bootcamp/katalon/research.md) and [ShopeeFood research](pm-interview-bootcamp/shopeefood/research.md): existing research dated September 10, 2026, including access limitations and distinctions between documented facts and preparation inferences.

### Limited external verification

The narrow AI architecture checks for this synthesis were made on September 12, 2026. Relevant explanations link their supporting source in the teaching section:

- [Official MCP architecture](https://modelcontextprotocol.io/docs/learn/architecture): host, client, server, exposed capabilities, and protocol scope.
- [Anthropic: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents): distinction between predefined workflows and adaptive agents.
- [Google Cloud: RAG overview](https://cloud.google.com/vertex-ai/generative-ai/docs/rag-engine/rag-overview): retrieval and supplied context in generation.

The product recommendations and causal examples in this source are educational applications, not findings from those sources. No hands-on product benchmark or new customer research was performed.

### Material gaps kept explicit

The repository does not establish complete candidate incidents, quantified impact, deployed PRJ226 capabilities, or specific TDCX/FPT achievements. These remain **PERSONAL EVIDENCE REQUIRED**. Practice performance is not work experience.

Actual company financial rates, internal metrics, matching rules, detailed permission defaults, and exact interview assessment mechanics are not assumed. Product capabilities and recruitment details can change; use the preserved research's cited originals if a specific current claim becomes necessary. This source teaches decisions without requiring those unknown facts.

## Part 27: Final 15-minute review

**P0 — MUST KNOW**

Use this on interview morning. Spend a few minutes on each relevant reflex, then explain one example aloud. The suggested timing is optional; you control the pace.

### Product Reflex

**User → Workflow → Problem → Evidence → Hypothesis → Test → Action → Metric.**

What is the person trying to accomplish? What happens today? Which obstacle matters, and what proves it exists? A feature request is one possible answer. Frame the outcome as **improve X without materially harming Y**.

Choose the smallest useful next step that resolves an important uncertainty. A clear requirement describes observable behavior. Acceptance criteria should let another person judge whether it works.

### Case Reflex

**What happened? → Why might it happen? → How do I know? → What should we do? → What else changes?**

Define the symptom and comparison. Break the outcome into a few useful branches. Compare meaningful segments. Rank explanations and request evidence with a purpose. Make a conditional recommendation rather than waiting for perfect information.

Say what would change your mind. If evidence contradicts you, update the action.

### AI Reflex

**Why AI? → Why an LLM? → Why an agent? → Failure? → Verify? → Reverse? → Human? → Measure value?**

Use rules for clear rules. Use relevant current context for project-specific facts. A tool call needs permission, valid inputs, execution, and an observed result. A server connection does not guarantee correct reasoning or authorize unrestricted action.

Choose autonomy by action class and consequence. A draft, shared edit, and release decision carry different risks. Measure useful task completion and total effort, including review and retries. Confidence and acceptance are not proof of correctness.

### Testing Reflex

**Requirement → Design → Create → Execute → Investigate → Diagnose → Fix → Regression → Release confidence.**

A failed test may correctly reveal a defect. A passing test may check very little. Before repair, identify whether the application, test, data, environment, or dependency is wrong. Preserve meaningful assertions and check important risks.

### Marketplace Reflex

**Buyer ↔ Merchant ↔ Driver ↔ Platform.**

Then ask: **And then what happens?**

Liquidity is local and time-sensitive. Drivers waiting at kitchens consume capacity. A promotion can change demand, queues, costs, and future trust. Every chain is a hypothesis to test. Check all affected sides and nearby areas.

### Metrics and Money Reflex

- Completed orders = placed orders × completion rate, with compatible definitions.
- Ordering buyers × orders per ordering buyer is a different valid view. Do not double-count frequency.
- Define population, event, denominator, window, and comparison.
- Pair the intended outcome with a relevant diagnostic measure and important guardrail.
- GMV is not revenue. Revenue minus included variable costs gives contribution, not full-company profit.
- Identify the subsidy payer and ask how many orders are incremental.

### Communication Reflex

**Clarify → Structure → Evidence → Trade-off → Recommendation → Stop.**

“I'd first clarify…”

“One possible explanation is…”

“The evidence I'd want to see is…”

“Given the information we have, I'd…”

“I'd change my recommendation if…”

For personal stories: context, your responsibility, your actual action, observed result, and learning. Say “I did not measure that” when needed. Never turn a hypothetical case into experience.

### Final spoken check

Without reading an answer, explain one at a time:

1. Why could an AI testing feature work technically but fail to create value?
2. Why could more food orders make the marketplace less healthy?
3. What evidence would make you change your first recommendation?
