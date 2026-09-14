# Agile for Product Managers

[Study notes](README.md) · [Roadmap](../ROADMAP.md) · [Katalon cases](../katalon/CASES.md) · [ShopeeFood cases](../shopeefood/CASES.md)

This is interview preparation, not Scrum certification preparation. Start with the **P0** sections. Try each case before reading its reasoning path.

**Priority key**

- **P0 — MUST KNOW:** likely to affect PM interview performance.
- **P1 — SHOULD KNOW:** useful depth for follow-up questions.
- **P2 — OPTIONAL:** helpful context, not a memorization target.

**Evidence key**

- **OFFICIAL SCRUM:** required or defined by the current official Scrum Guide.
- **COMMON PRACTICE:** often used with Agile or Scrum, but not required by the Scrum Guide.
- **HYPOTHETICAL / INTERVIEW EXERCISE:** invented to teach reasoning; not a claim about a company or the candidate.
- **SELF-REPORT:** stated by the candidate, not independently verified.
- **PERSONAL EVIDENCE REQUIRED:** the repository does not yet support the claim.

The official source check for this note was made on September 14, 2026. The [Scrum Guides download page](https://scrumguides.org/download) identifies the November 2020 guide as the current official version.

## 1. Why does Agile exist? — P0

Complex product work contains uncertainty. Customers may describe symptoms rather than needs. A technical approach may fail. A competitor, regulation, incident, or experiment may change the priority. A detailed six-month plan cannot remove those uncertainties.

The risky mental model is:

> Plan everything → build for months → integrate late → discover that important assumptions were wrong.

The Agile mental model is:

> Choose a valuable problem or hypothesis → build or test something small → inspect the result → learn → adapt.

This does not mean “never plan.” It means plan at a level justified by current evidence, preserve a direction, and update the route when reality teaches the team something important.

Agile is useful when customer needs, technology, priorities, or solution behavior cannot be predicted perfectly. Small increments limit how much time is exposed to a wrong assumption. Frequent feedback does not guarantee success, but it can reveal error sooner.

**PM example — HYPOTHETICAL:** A testing-product team assumes QA engineers need faster AI test generation. Before building a large autonomous system, it observes the workflow and learns that reviewing inconsistent output is the real bottleneck. The team first builds a small comparison view. It measures correct review completion and harmful changes applied, then decides what to expand.

Agile is therefore mainly about **value, learning, collaboration, feedback, and adaptation under uncertainty**. Two-week Sprints and Daily Scrums are possible structures, not the reason Agile exists.

**Interview answer:**

> “Agile means delivering value in small increments, getting evidence early, and adapting when we learn. It still needs direction, quality, and disciplined choices; it is not permission to change everything at any time.”

## 2. The Agile Manifesto — P0

The [Agile Manifesto](https://agilemanifesto.org/) says that the items on the right still have value, but the items on the left are valued more.

### 2.1 Individuals and interactions over processes and tools

**Beginner meaning:** A board, ticket template, or meeting cannot replace people understanding one another and solving a problem together.

**It does not mean:** Ignore processes, documentation systems, or useful tools.

**PM example — HYPOTHETICAL:** A requirement ticket is ambiguous. The PM, designer, engineer, and QA discuss the actual failure flow and update the requirement together instead of passing the ticket between functions.

**Interview misunderstanding:** “Agile teams do not need process.” Better: use enough process to support collaboration and transparency.

### 2.2 Working software over comprehensive documentation

**Beginner meaning:** A usable, verified product increment provides stronger evidence of progress than a large document about future work.

**It does not mean:** Documentation is useless. Security decisions, APIs, operations, regulated evidence, and user guidance may require it. Documentation can also be part of quality.

**PM example — HYPOTHETICAL:** The team writes a concise test-change specification and builds a narrow review flow rather than spending two months detailing every future AI action.

**Interview misunderstanding:** “If coding is finished, the work is done.” Working software must meet the product's quality standard and be usable; raw code is not enough.

### 2.3 Customer collaboration over contract negotiation

**Beginner meaning:** Keep learning with customers or stakeholders instead of treating an early agreement as perfect knowledge.

**It does not mean:** Ignore contracts, commercial commitments, or scope control.

**PM example — HYPOTHETICAL:** An enterprise asks for full automation. The PM clarifies the underlying release delay and tests a review-assisted workflow before promising unattended changes.

**Interview misunderstanding:** “The loudest customer chooses the roadmap.” Collaboration supplies evidence; the PM or Product Owner still weighs strategy, reach, risk, and opportunity cost.

### 2.4 Responding to change over following a plan

**Beginner meaning:** A plan is a current best route, not a reason to ignore new facts.

**It does not mean:** Accept every request instantly or disrupt a Sprint without considering cost.

**PM example — HYPOTHETICAL:** A serious production defect appears. The team assesses severity and the Sprint Goal, mitigates harm, and renegotiates scope. A normal feature request waits for backlog ordering.

**Interview misunderstanding:** “Agile means priorities can change without consequence.” Better: change deliberately and make the displaced work visible.

### 2.5 The principles, grouped for PM use — P0

Do not memorize all [twelve principles](https://agilemanifesto.org/principles) word-for-word. Remember their logic:

- **Customer value:** satisfy customers through early and continuous delivery of valuable software.
- **Frequent delivery:** shorten the distance between an idea and observable evidence.
- **Responsiveness:** welcome useful change, including late learning, without pretending the cost is zero.
- **Business and engineering collaboration:** bring product context and technical reality together throughout the work.
- **People and sustainable pace:** trust capable people and avoid a pace that cannot be maintained.
- **Technical quality:** good design and technical excellence preserve the ability to adapt.
- **Simplicity:** maximize work not done; solve the important problem with the least unnecessary scope.
- **Reflection and adaptation:** regularly examine how the team works and change it.

## 3. Agile, Scrum, and Kanban are not synonyms — P0

Use a travel analogy:

- **Agile** is the travel philosophy: move toward a valuable destination, check conditions often, and change route when evidence warrants it.
- **Scrum** is one lightweight travel rhythm: a small team works toward goals in fixed-length Sprints and inspects product and process at defined events.
- **Kanban** is a flow system: visualize how work moves, control work in progress, manage items actively, and improve flow.

The [Scrum Guide](https://scrumguides.org/scrum-guide.html) defines Scrum as a lightweight framework for generating value through adaptive solutions to complex problems. The May 2025 [Kanban Guide](https://kanbanguides.org/the-kanban-guide/2025.5/pdf/kanban-guide.v2025.5.en.pdf) defines Kanban as a strategy for optimizing the flow of value through a process.

| Choice | Useful fit | Watch out for |
|---|---|---|
| Scrum | A stable, cross-functional team can pursue a coherent goal in Sprints and benefit from regular product and process inspection | Treating events as status rituals; forcing unrelated urgent work into one Sprint Goal |
| Kanban | Work arrives continuously or unpredictably, such as support, incidents, platform requests, or operations; flow and WIP need control | A board alone is not Kanban; starting everything creates queues |
| Hybrid practices | The context benefits from a Sprint goal plus Kanban flow controls, or discovery and delivery need different cadences | Mixing practices without an explicit reason or claiming partial Scrum is formal Scrum |

Not every product team needs Scrum. Choose practices for the work and risks, then inspect whether they help.

## 4. Official Scrum versus common practice — P0

This distinction prevents certification language from being mixed with workplace convention.

| Concept | Status | Interview-safe explanation |
|---|---|---|
| Scrum Team: Product Owner, Developers, Scrum Master | **OFFICIAL SCRUM** | Three accountabilities, not necessarily three job titles |
| Sprint, Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective | **OFFICIAL SCRUM** | Five events; the Sprint contains the other four |
| Product Backlog, Sprint Backlog, Increment | **OFFICIAL SCRUM** | Three artifacts |
| Product Goal, Sprint Goal, Definition of Done | **OFFICIAL SCRUM** | Commitments associated with the three artifacts |
| Transparency, inspection, adaptation | **OFFICIAL SCRUM** | Empirical pillars that make adaptation possible |
| Commitment, focus, openness, respect, courage | **OFFICIAL SCRUM** | Scrum values |
| Product Backlog refinement | **OFFICIAL ACTIVITY, not a formal event** | Ongoing breaking down and clarification; teams choose how and when |
| User stories | **COMMON PRACTICE** | One useful format for expressing a need; not required for backlog items |
| Acceptance criteria | **COMMON PRACTICE** | Item-specific behavior or conditions; useful but not named as a required Scrum element |
| Story points and planning poker | **COMMON PRACTICE** | Relative sizing and a discussion technique; neither is required |
| Velocity | **COMMON PRACTICE** | A team's completed estimate per interval; absent from the Scrum Guide |
| Definition of Ready | **COMMON PRACTICE** | A team-created readiness aid; not an official commitment like DoD |
| Burndown, burnup, cumulative-flow charts | **OPTIONAL FORECASTING PRACTICES** | The Scrum Guide acknowledges such practices but does not require them or call them artifacts |
| A two-week Sprint | **COMMON CHOICE** | Officially, a Sprint is fixed length and one month or less; two weeks is not mandatory |
| Releasing only at Sprint Review | **NOT A SCRUM RULE** | A usable Increment may be delivered earlier; Review is not a release gate |

## 5. Scrum from zero: the logic of the system — P0

Scrum is based on **empiricism**: learn from experience and observed results. Its three pillars are:

- **Transparency:** people share a sufficiently accurate view of goals, work, quality, and results.
- **Inspection:** they examine the product, progress, and way of working frequently enough to detect problems.
- **Adaptation:** they change the product plan or working method when inspection reveals a material gap.

The loop is simple:

> Product Owner orders work toward a Product Goal → Scrum Team chooses a Sprint Goal and plan → Developers create a usable Increment → team and stakeholders inspect results → backlog and working approach adapt → repeat.

### 5.1 The three accountabilities

**Product Owner**

- Accountable for maximizing product value.
- Develops and communicates the Product Goal.
- Creates and communicates Product Backlog items, orders them, and ensures the backlog is visible and understood.
- May delegate tasks, but remains accountable.
- Is one person, not a committee; listens to many stakeholders but makes coherent value decisions.

**Developers**

- The people who create any aspect of a usable Increment; the term is broader than software programmers.
- Create and update the Sprint Backlog, adhere to the Definition of Done, adapt their plan toward the Sprint Goal, and hold one another accountable.
- Select what they can take into a Sprint and decide how to create the Increment.

**Scrum Master**

- Accountable for establishing Scrum as defined and for the Scrum Team's effectiveness.
- Coaches self-management and cross-functionality, helps remove impediments, and helps events be productive.
- Supports Product Owner, Scrum Team, and organization. This is not the team's task secretary or command-and-control manager.

The whole Scrum Team is accountable for creating a valuable, useful Increment every Sprint.

### 5.2 Product Manager versus Product Owner

**Product Owner is an official Scrum accountability. Product Manager is not a role defined by the Scrum Guide.** Company structures differ.

| Area | Product Manager often emphasizes | Product Owner is accountable for in Scrum |
|---|---|---|
| Direction | Market, users, strategy, outcomes, roadmap | Product Goal and maximizing value |
| Discovery | Customer problems, evidence, solution risks | May lead or participate; Scrum does not prescribe a separate discovery role |
| Delivery decisions | Scope, trade-offs, release and stakeholder alignment | Effective Product Backlog management and ordering |
| Engineering collaboration | Context, requirements, trade-offs, outcome measurement | Clear items and collaboration with Developers around value and scope |
| Organizational form | May cover several teams or a broader business area | One person for the Scrum Team's product; not a committee |

One person may be both PM and PO. Some organizations split them. If split badly, strategy and delivery can become disconnected. Never claim one universal structure; ask how the company assigns accountabilities.

**Interview answer:**

> “A Product Owner is a specific Scrum accountability for maximizing value and managing the Product Backlog. A Product Manager often has broader strategy, market, discovery, and outcome responsibilities. They may be the same person or separate roles depending on the organization, but the value direction and delivery decisions must stay connected.”

## 6. Artifacts and commitments through one example — P0

Everything in this section is **HYPOTHETICAL / INTERVIEW EXERCISE** for a Katalon-like testing product.

Users struggle to diagnose failed automated tests. The team wants to reduce incorrect release decisions without hiding genuine defects.

1. **Product Goal — future target:** “Help QA teams diagnose failed automated tests with trustworthy evidence before a release decision.”
2. **Product Backlog — emergent, ordered work:** interview QA users; link failure logs; group likely causes; show evidence beside suggestions; add permission checks; evaluate false diagnoses; improve slow queries.
3. **Sprint Goal — one Sprint objective:** “Let a QA engineer connect one failed test to the relevant logs and inspect the evidence in one view.”
4. **Selected Product Backlog items:** correlation identifier, linked-log query, evidence panel, access-control check, evaluation sample.
5. **Sprint Backlog — Developers' plan:** the Sprint Goal (**why**), selected items (**what**), and actionable delivery plan (**how**). It changes as Developers learn.
6. **Increment — usable step:** authorized QA users can open a failed test and view the correct linked logs. It integrates with prior product behavior and meets the DoD.
7. **Definition of Done — product quality bar:** for this hypothetical product, relevant review completed, automated and permission tests pass, integration works in the target environment, required operational logging exists, and required documentation is updated.
8. **Feedback:** users find linked evidence useful, but identical errors still require repetitive comparison.
9. **Next backlog decision:** order failure grouping above a broad AI explanation feature because the observed repeated task is better supported and narrower.

The relationships are:

```text
Product Goal
└── Product Backlog (all currently known work, ordered and adaptable)
    └── Sprint Backlog
        ├── Sprint Goal
        ├── selected Product Backlog items
        └── Developers' delivery plan
            └── Increment
                └── must meet Definition of Done
                    └── feedback changes the Product Backlog
```

**Product Backlog versus Sprint Backlog:** The Product Backlog is the emergent ordered source of work for the product. The Sprint Backlog is the Developers' current-Sprint plan toward one Sprint Goal.

## 7. Scrum events: purpose before ceremony — P0

| Event | Purpose and participants | Decision supported | Beginner misunderstanding | PM/PO focus |
|---|---|---|---|---|
| **Sprint** | Fixed-length container of one month or less; all Scrum events and product work happen within it | How to turn ideas into value with a bounded learning horizon | “A Sprint is just a two-week deadline” | Preserve goal and quality; clarify or renegotiate scope as learning occurs |
| **Sprint Planning** | Entire Scrum Team creates the Sprint plan; others may advise | Why is this Sprint valuable? What can be Done? How will it be done? | “PO assigns tickets and hours” | Bring ordered priorities and Product Goal context; collaborate on a coherent Sprint Goal; respect Developers' selection and delivery plan |
| **Daily Scrum** | Fifteen-minute event for Developers to inspect progress toward the Sprint Goal and adapt the plan | What needs to change in the next day's work? | “Each person reports status to a manager” | Ensure context is available; do not turn it into PM surveillance; follow up separately where needed |
| **Sprint Review** | Scrum Team and key stakeholders inspect the Sprint outcome and changed environment | What should the team do next? Does the Product Backlog need adaptation? | “A presentation or approval gate” | Seek real feedback, discuss Product Goal progress and outcomes, adapt future work |
| **Sprint Retrospective** | Scrum Team inspects individuals, interactions, processes, tools, and DoD | How can quality and effectiveness improve? | “A stakeholder demo or blame meeting” | Participate openly if on the Scrum Team; improve the system, not assign blame |

### Review versus Retrospective — the essential distinction

- **Sprint Review asks:** What did the product produce, what changed around us, and what should we do next? It includes key stakeholders and can adapt the Product Backlog.
- **Sprint Retrospective asks:** How did the Scrum Team work, and what change would improve quality or effectiveness? It is for the Scrum Team and adapts the working system.

**Memory aid:** Review the **product and direction**; retrospect on the **team's way of working**.

## 8. Backlog, prioritization, and refinement — P0

A Product Backlog is not a promise to build everything. It is an **emergent, ordered list of what is needed to improve the product**. It changes as evidence, risk, strategy, and the product change.

A useful Product Backlog item gives enough shared understanding for a decision. Depending on context, it may include:

- the customer problem or desired outcome;
- evidence and why it matters now;
- scope and observable behavior;
- important constraints, risks, or dependencies;
- acceptance criteria or another way to confirm the item;
- size information useful for forecasting.

Not every low-priority idea deserves detailed specification. Delete, archive, merge, or reframe stale requests. A backlog becomes a graveyard when it stores every request but communicates no current order, goal, evidence, or decision.

### 8.1 How a PM or PO orders work

Reason across these factors instead of obeying a label or score:

- **Customer problem:** what job is blocked, and how severe is the harm?
- **Product Goal and strategy:** does this move the intended future state?
- **Evidence:** observed behavior or only an opinion?
- **Expected value and reach:** who benefits, how often, and by how much?
- **Effort and uncertainty:** what does Engineering know, and what remains unknown?
- **Risk:** security, reliability, legal, reputation, or reversibility.
- **Dependencies:** does one item unlock or block another?
- **Opportunity cost and cost of delay:** what waits, and what worsens if delayed?
- **Learning value:** can a small step resolve a major uncertainty?

The Product Owner orders the Product Backlog in Scrum. That does not mean ordering alone: Developers supply feasibility, size, dependencies, and technical risk; design, data, operations, sales, support, and customers supply other evidence.

### 8.2 Backlog refinement — P1

Refinement is ongoing clarification and decomposition of Product Backlog items. It is part of Scrum, but **not one of the five formal Scrum events**. Teams decide how and when it happens.

Useful refinement asks:

1. Why does this matter and how does it connect to the Product Goal?
2. What behavior or outcome is in scope?
3. What is uncertain, risky, or dependent?
4. Is the item small and understood enough for a Sprint forecast?
5. What would show it is acceptable?

Refinement is not an attempt to eliminate all uncertainty or write every future ticket in detail.

## 9. User stories, acceptance criteria, and Definition of Done — P0

### 9.1 A user story is a conversation aid

A common format is:

> As a **[user]**, I want **[capability]**, so that **[outcome]**.

User stories are **COMMON PRACTICE, not required Scrum syntax**. A defect, research question, technical risk, experiment, or infrastructure change may be a valid Product Backlog item without pretending it is a user-facing feature.

A user story is not the customer problem. It already expresses one possible capability. The underlying problem may support several different solutions.

**Weak:** “As a user, I want AI so that testing is better.” The user, task, value, and boundary are vague.

**Better:** “As a QA engineer, I want to inspect an AI-proposed test change so that I can decide whether it preserves intended behavior.”

The underlying problem might be: QA engineers spend effort checking uncertain changes and risk weakening meaningful assertions. A comparison view is one response, not the problem itself.

### 9.2 Acceptance criteria

Acceptance criteria describe **item-specific behavior or conditions** used to confirm shared expectations. For the better story:

- original and proposed changes are both visible;
- rejecting leaves the test unchanged;
- an unauthorized user cannot apply the change;
- a conflict is surfaced if the source changed after the proposal;
- the system records whether the proposal was accepted or rejected, subject to appropriate data rules.

This connects to [Product thinking](PRODUCT_THINKING.md): problem → user flow → scope → acceptance criteria → measurement. Criteria clarify behavior; they do not prove that users need the feature or that it creates the desired outcome.

### 9.3 Definition of Done

The **Definition of Done (DoD)** is an **OFFICIAL SCRUM commitment**: the formal description of the Increment's state when it meets the product's required quality measures.

“Coding finished” may omit review, testing, integration, permissions, required documentation, operational readiness, or other product-specific quality requirements. The Scrum Guide does not prescribe one universal checklist. If the organization has a standard, teams follow it as a minimum; otherwise the Scrum Team creates an appropriate DoD. Developers conform to it.

Work that does not meet the DoD is not part of the Increment. In official Scrum it cannot be released or presented as part of the Increment at the Sprint Review; it returns to the Product Backlog for future consideration.

| Acceptance criteria | Definition of Done |
|---|---|
| Specific to one item or behavior | Shared quality standard for the Increment |
| Example: reject leaves the test unchanged | Example: relevant tests pass, required review and integration are complete |
| Helps answer “Did this item behave as agreed?” | Helps answer “Is this work truly part of a usable Increment?” |
| Common practice | Official Scrum commitment |

## 10. Estimation without false precision — P0

An estimate supports a decision; it is not a guarantee. Product development estimates contain uncertainty about implementation, integration, dependencies, quality, and newly discovered work.

- **Effort estimate:** a forecast of how difficult or large the work may be.
- **Capacity:** the team's realistically available ability in the period, affected by people, support work, leave, and other obligations.
- **Story points — COMMON PRACTICE:** a team's relative sizing unit that may combine effort, complexity, and uncertainty. **Five points do not equal five days.** Points have meaning only within the team's own method and context.
- **Planning poker — COMMON PRACTICE:** people reveal estimates and discuss important differences. The conversation about assumptions is more valuable than voting precision.
- **Velocity — COMMON PRACTICE:** amount of estimated work completed in an interval, often points per Sprint. It can help the same stable team forecast. It is not an official Scrum metric, customer value, or a fair cross-team performance ranking.

**Scenario — HYPOTHETICAL:** A team usually completes around 30 locally defined points. A director demands 40 next Sprint. A strong PM does not pressure the team to inflate points or trade away quality. Ask what business outcome is urgent, examine capacity and changed work, split scope, remove a dependency, and make uncertainty visible. Forecast from comparable history, then judge success by the Sprint Goal, usable value, quality, and product outcome—not the point total.

**Interview phrase:** “I would use estimates for forecasting and trade-offs, not as promises or individual productivity scores.”

## 11. Product discovery and delivery — P0

**Discovery asks whether to build:** Are we solving the right problem? Do users need help? Which solution looks promising? Which assumption is most dangerous?

**Delivery asks whether we can create and sustain it:** Can we build, verify, ship, operate, and improve the product correctly?

They can overlap. Engineers can expose feasibility risks during discovery. A small delivered Increment can create discovery evidence. Shipping is not the end of learning.

```text
Customer behavior
→ problem and hypothesis
→ prototype, interview, data analysis, or experiment
→ evidence
→ backlog decision
→ small delivered Increment
→ product outcome and guardrails
→ learning
→ adapt
```

**Dual-Track Agile — COMMON PRODUCT PRACTICE, not official Scrum:** discovery and delivery activities proceed continuously and inform each other. “Two tracks” should not mean a discovery team throws specifications over a wall to a delivery team. [Product Talk](https://www.producttalk.org/adopting-continuous-product-discovery/) describes discovery as deciding what to build and delivery as building and shipping it.

**Connection to this repository:** [Customer discovery](CUSTOMER_DISCOVERY.md) helps establish the problem; [Product thinking](PRODUCT_THINKING.md) turns a supported problem into scope and criteria; delivery creates a usable change; [metrics](../../NOTEBOOKLM_MASTER_SOURCE.md#part-6-metrics-from-zero) test whether the expected outcome occurred.

## 12. Agile does not mean “accept every change” — P0

A stakeholder arrives halfway through a Sprint: “This enterprise request is urgent. Add it now.” Do not answer yes or no from the label **urgent**.

### 12.1 Reasoning path

1. **Clarify urgency:** What happened, who is affected, and what deadline or harm makes it urgent?
2. **Classify the work:** production/customer harm, contractual or legal risk, new feature, or preference?
3. **Check evidence and reach:** one request, a shared problem, or a severe exception?
4. **Protect the Sprint Goal:** Would the change endanger it? The Scrum Guide says no change should endanger the Sprint Goal.
5. **Expose opportunity cost:** What current work, learning, or quality would be displaced?
6. **Ask Engineering:** What is the size, uncertainty, dependency, and safest mitigation?
7. **Choose deliberately:** wait and reorder the Product Backlog; swap or renegotiate scope while preserving the Sprint Goal; mitigate an incident; or, in an extreme case, cancel and replan if the Sprint Goal is obsolete.
8. **Communicate:** decision, reason, displaced work, owner, and next checkpoint.

Only the Product Owner can cancel a Sprint in official Scrum, and cancellation is for an obsolete Sprint Goal—not ordinary scope anxiety.

### 12.2 Three different “urgent” requests

- **Severe production data exposure:** contain harm now. Current feature work may stop. Preserve evidence, involve security and engineering, and replan transparently.
- **Enterprise feature tied to a sales conversation next week:** clarify whether a demo, manual workaround, or discovery session can address the immediate need. Usually order the backlog rather than silently insert work.
- **Executive preference with no new deadline or harm:** explain current Sprint Goal and trade-off; capture the request and compare it in the normal product decision.

**Interview phrase:** “I’d be responsive, but I would not confuse responsiveness with disruption. I’d clarify the harm, protect the Sprint Goal, and make the opportunity cost explicit.”

## 13. Technical debt, bugs, features, and learning work — P0

### 13.1 Technical debt in product language

Technical debt is not “engineers want to rewrite everything.” It is a useful metaphor for internal technical deficiencies that make future change harder or riskier. [Martin Fowler](https://martinfowler.com/bliki/TechnicalDebt.html) describes the extra effort required for future changes as the “interest” paid on the debt.

Possible product chain:

```text
fragile internal design
→ slower or riskier changes
→ more incidents and harder testing
→ greater engineering effort
→ weaker ability to respond to customers
```

Each arrow is a hypothesis to support with evidence: recurring defects, change failure, cycle time, incident load, dependency delays, or repeated effort in the same area.

### 13.2 Prioritize the consequence, not the label

Ask Engineering to explain:

- which product area or future work is affected;
- what evidence shows recurring cost or risk;
- consequence and likelihood if delayed;
- smallest meaningful reduction, not only a total rewrite;
- expected effect and how the team will observe it;
- opportunity cost of doing it now.

**Katalon-style scenario — HYPOTHETICAL:** Enterprise users ask for another test framework, but the shared execution adapter causes repeated integration failures. If the adapter work is a dependency for the requested framework and reduces recurring incidents, doing a bounded refactor first may produce customer value sooner overall. The PM should connect it to reliability and future delivery, not reserve “two Sprints for debt” without a goal.

**Marketplace scenario — HYPOTHETICAL:** A city team wants a new promo rule, while a brittle pricing service has caused incorrect fee calculations during peaks. Compare financial and trust risk, incident frequency, affected orders, and whether the service blocks safe experiments. A contained reliability change may outrank another promo even if it is invisible to users.

### 13.3 Limited-capacity prioritization exercise

**HYPOTHETICAL:** Capacity permits roughly two substantial items:

| Candidate | Evidence | Reasoning |
|---|---|---|
| Enterprise export feature | One large customer's request; renewal impact unclear | Strategic potential, but validate underlying job and broader reach |
| Checkout production bug | 2% of payment attempts duplicate a pending order; recovery is confusing | High-severity trust and operational risk; mitigate and fix first |
| Payment-module debt | Engineers show it caused three recent incidents and doubles change effort | Strong risk/dependency link; pair a bounded reduction with the fix |
| Analytics instrumentation | Team cannot distinguish payment rejection from timeout | High learning value; a narrow instrumentation slice may be part of diagnosis/verification |

**Possible recommendation:** Contain and fix the production bug; include the minimal instrumentation needed to verify it; use remaining capacity to reduce the specific payment-module fragility that caused or magnifies the issue. Refine the export request with the customer for later ordering. This is conditional: if the “bug” is rare, harmless, and already mitigated while a contractual deadline is verified, the order may change.

Labels do not set priority. Compare **severity, reach, strategic value, risk, urgency, dependencies, learning value, cost of delay, and opportunity cost**.

## 14. When the Sprint Goal is missed — P0

“The team committed to several items but missed the Sprint Goal” mixes two ideas. In current Scrum, Developers commit to the **Sprint Goal**; selected items support a forecast and plan. Finishing every ticket does not prove the goal was valuable, and leaving one optional item unfinished does not automatically mean the goal failed.

### 14.1 Diagnose before prescribing speed

Investigate:

- Was the Sprint Goal clear, coherent, and valuable?
- Did the team select too much work relative to capacity and history?
- Was scope too vague or insufficiently refined?
- Did an external dependency block the goal?
- Did unexpected technical complexity emerge?
- Did a production incident or stakeholder interruption consume capacity?
- Did an assumption change, making the original work less useful?
- Did hidden quality work appear because DoD was misunderstood?
- Was the estimate treated as certainty?
- Did the team split work horizontally so nothing became usable?

“Engineers need to work faster” ignores the system, encourages quality shortcuts, and produces little learning.

### 14.2 What happens next?

**At Sprint Review:** Be transparent about the actual Increment and goal result. Inspect the product outcome and changed environment with stakeholders. Do not present unfinished work as Done. Discuss what matters next and adapt the Product Backlog.

**At Sprint Retrospective:** Inspect how the work happened. Identify one or two high-leverage changes—such as earlier dependency checks, smaller slices, clearer goal boundaries, or protected incident capacity—without blame.

**Afterward:** Reorder unfinished work; do not automatically roll it into the next Sprint. Reassess value, dependencies, and the next Sprint Goal. Track whether the selected improvement changes the repeated pattern.

**Interview answer:**

> “I’d first separate missing tickets from missing the Sprint Goal. I’d make the real Increment visible at Review, learn whether the product direction should change, and use the Retrospective to improve the delivery system. Then I’d reorder unfinished work rather than carrying it over automatically.”

## 15. Delivery, flow, quality, and outcome metrics — P0

Metrics support questions; they do not replace judgment.

| Metric | What it can help reveal | Misuse to avoid |
|---|---|---|
| **Cycle time** | Elapsed time from work started to finished under a defined workflow | Ignoring how “started” and “finished” are defined or which work classes differ |
| **Lead time** | Often, elapsed time from request to delivery; definitions vary, so state yours | Treating queue time as only an Engineering problem |
| **Throughput** | Number of work items finished per unit of time | Comparing unequal item types or equating count with value |
| **Work in progress (WIP)** | Work started but not finished; excess WIP can expose queues and context switching | Pushing more work to look busy |
| **Work item age** | How long current work has been in progress | Punishing difficult work instead of unblocking it |
| **Predictability** | Difference or distribution between forecast and actual delivery | Demanding perfect conformance in complex work |
| **Escaped defects / incidents** | Quality problems found after release | Gaming through reclassification or ignoring severity and reach |
| **Sprint Goal success** | Whether the Sprint's intended objective was achieved | Writing vague goals so every Sprint “succeeds” |
| **Velocity — common practice** | A stable team's locally estimated completion history for forecasting | Comparing teams, rating individuals, demanding increases, or treating points as value |
| **Product outcome** | Whether user or business behavior improved | Claiming causation without a comparison or ignoring guardrails |

The Kanban Guide's minimum flow metrics are WIP, throughput, work item age, and cycle time. Scrum does not require these metrics, but teams can use evidence that helps them inspect and adapt.

### Delivery metric is not product outcome

```text
Velocity ↑
does not imply
customer value ↑
```

A team can complete more points by changing point scales, splitting work differently, choosing easy items, or building unused features. Delivery evidence asks **how work flows and whether the team can create a usable Increment**. Product evidence asks **whether the intended customer and business outcome changed without unacceptable harm**.

**Example — HYPOTHETICAL:** The team ships an AI failure summary on time and meets its Sprint Goal. That is delivery success. If QA users ignore it because evidence is unclear, the product outcome failed. Inspect usage by eligible task, correct decision rate, total diagnosis effort, harmful guidance, and qualitative reasons; adapt the backlog.

## 16. Working with Engineering and other functions — P0

A PM brings **problem, evidence, priority, constraints, and outcome**. Engineers bring **implementation options, effort, dependencies, operational risk, and technical evidence**. Both challenge assumptions. Developers decide how to build; Product Owner orders the Product Backlog. Good collaboration is not Product writing commands and Engineering receiving them.

When an engineer disagrees with priority:

1. Restate the shared goal.
2. Ask which assumption, cost, dependency, or risk they see differently.
3. Compare evidence and consequences, including opportunity cost.
4. Seek a smaller option or sequencing change.
5. Make the decision and reasoning visible; define what new evidence would reopen it.

When Product keeps changing requirements, treat the complaint as system evidence. Separate true new learning from avoidable ambiguity, hidden stakeholders, weak discovery, and preference changes. Preserve a stable goal where possible, improve refinement and decision records, and make displaced work visible.

### Katalon-like cross-functional loop — HYPOTHETICAL

Customer discovery → observed difficulty reviewing AI-generated changes → Product Goal → ordered risk and value items → Sprint Goal for inspectable change proposals → implementation plus permission and conflict testing → Sprint Review with stakeholders → evidence on correct review and effort → backlog adaptation.

An AI safety evaluation failure is not “QA blocking release.” If the DoD or release guardrail requires acceptable safety behavior, the Increment is not ready for that release. Product, Engineering, QA, security, and relevant stakeholders decide mitigation and scope from the risk.

### ShopeeFood-like cross-functional loop — HYPOTHETICAL

A driver-cancellation spike mid-Sprint may require Product, Engineering, Analytics, Operations, Marketing, and merchant/driver teams. First verify segment and immediate harm. A product change may need city operations, communications, instrumentation, and a controlled rollout. Sprint events can help coordination and inspection; they do not choose marketplace strategy.

If a promo experiment increases orders but worsens merchant rejection and driver waiting, inspect the shared marketplace. Adapt eligibility, capacity controls, or the experiment rather than celebrating the buyer-side metric alone.

## 17. Agile interview question bank — P0

These 21 questions are synthesized around recurring PM interview signals: conceptual accuracy, value judgment, execution, collaboration, learning, and truthful communication. They are not claimed questions from Katalon or ShopeeFood. Use the reasoning structures, not the sample wording as a script.

### A. Fundamentals

#### Q1. What does Agile mean to you?

- **Testing:** First-principles understanding rather than ceremony vocabulary.
- **Weak answer:** “Agile means two-week Sprints and daily stand-ups.”
- **Strong structure:** uncertainty → small value increment → evidence → adaptation → discipline.
- **Spoken example:** “Agile is a way to create value under uncertainty. I would choose a useful small step, deliver or test it, inspect customer and delivery evidence, and adapt. Planning and documentation still matter; they support learning rather than prevent change.”
- **Likely follow-up:** When would Agile be less useful?

#### Q2. What is the difference between Agile, Scrum, and Kanban?

- **Testing:** Ability to distinguish philosophy, framework, and flow strategy.
- **Weak answer:** “They are three names for the same process.”
- **Strong structure:** Agile values/principles; Scrum accountabilities/events/artifacts in Sprints; Kanban workflow/WIP/flow; contextual choice.
- **Spoken example:** “Agile is the wider philosophy. Scrum is one lightweight framework using Sprints and explicit inspection points. Kanban optimizes flow by visualizing work and controlling WIP. A product team might use Scrum, Kanban, or complementary practices depending on its work.”
- **Likely follow-up:** What work would lead you toward Kanban?

#### Q3. What are a Product Backlog, Sprint Backlog, and Increment?

- **Testing:** Understanding of the Scrum system, not ticket names.
- **Weak answer:** “They are the to-do list, current tickets, and released feature.”
- **Strong structure:** product-wide emergent order → current Developers' goal/selection/plan → usable verified step; connect commitments.
- **Spoken example:** “The Product Backlog is the ordered, evolving source of product work and carries the Product Goal. The Sprint Backlog is the Developers' current plan: Sprint Goal, selected items, and delivery plan. The Increment is the usable integrated result that meets the Definition of Done.”
- **Likely follow-up:** Can an Increment be released before the Sprint Review?

### B. PM and Product Owner role

#### Q4. What does a Product Owner do?

- **Testing:** Current Scrum accountability and value orientation.
- **Weak answer:** “Writes tickets and assigns them to engineers.”
- **Strong structure:** maximize value → Product Goal → transparent, understood, ordered Product Backlog → one accountable person who collaborates.
- **Spoken example:** “The Product Owner is accountable for maximizing product value and for effective Product Backlog management. That includes the Product Goal, clear backlog items, ordering, and transparency. Developers still select the Sprint work and decide how to deliver it.”
- **Likely follow-up:** Who can change the Product Backlog?

#### Q5. How are Product Manager and Product Owner different?

- **Testing:** Role nuance without universal organizational claims.
- **Weak answer:** “The PM is senior and the PO writes stories.”
- **Strong structure:** PO is official Scrum accountability; PM often broader strategy/discovery/outcomes; overlap; company-specific structure.
- **Spoken example:** “Product Owner has a defined Scrum accountability for value and backlog management. Product Manager often covers wider market, strategy, discovery, and business outcomes. One person may do both, or a company may split them; I would clarify where accountability sits.”
- **Likely follow-up:** What risk appears when the roles are split?

#### Q6. How do you communicate priorities to Engineering?

- **Testing:** Collaboration, clarity, and respect for technical expertise.
- **Weak answer:** “I send the ranked roadmap and make sure they deliver.”
- **Strong structure:** goal/problem/evidence → order and opportunity cost → invite feasibility/risk → agree observable scope → update transparently.
- **Spoken example:** “I explain the customer problem, evidence, goal, and why this item is above alternatives. I ask Engineering to challenge feasibility, dependencies, and risk. We clarify the smallest useful scope and success evidence; I keep changes and displaced work visible.”
- **Likely follow-up:** What if the engineer still disagrees?

### C. Prioritization

#### Q7. A stakeholder wants a feature halfway through the Sprint. What do you do?

- **Testing:** Responsiveness without chaos.
- **Weak answer:** “Agile welcomes change, so we add it.”
- **Strong structure:** clarify harm/deadline → classify request → check Sprint Goal → size/risk → opportunity cost → wait, swap, mitigate, or exceptionally cancel.
- **Spoken example:** “I’d first clarify why it is urgent. If it is a severe production issue, we may interrupt and mitigate. If it is a normal request, I’d compare it in the Product Backlog. If we change current work, I’d collaborate with Developers and the PO, protect the Sprint Goal where possible, and state what moves out.”
- **Likely follow-up:** Who can cancel the Sprint?

#### Q8. Two executives demand conflicting priorities. How do you decide?

- **Testing:** Independent product judgment and stakeholder management.
- **Weak answer:** “I follow the more senior executive.”
- **Strong structure:** shared outcome → affected segment/evidence → value, urgency, risk, dependency, effort → options and opportunity cost → accountable decision.
- **Spoken example:** “I’d translate both requests into outcomes and compare evidence, strategic fit, urgency, reach, and cost of delay. I’d show the capacity constraint and what each choice displaces. Then the accountable product leader decides and records what evidence would change the order.”
- **Likely follow-up:** What if neither accepts the decision?

#### Q9. How do you choose among a bug, feature, technical debt, and analytics gap?

- **Testing:** Reasoning beyond labels.
- **Weak answer:** “Critical bugs first, then features, then debt.”
- **Strong structure:** severity/reach → strategic value → risk/urgency → dependency → learning value → cost of delay and smallest package.
- **Spoken example:** “I would not use the labels as rank. A narrow analytics change might be needed to diagnose a severe bug, while bounded debt work may prevent its recurrence. I’d compare customer harm, reach, strategic value, risk, dependencies, and opportunity cost, then select a coherent package.”
- **Likely follow-up:** How would you explain invisible debt work to a customer?

### D. Execution

#### Q10. The Sprint Goal was missed. What happens next?

- **Testing:** System diagnosis and correct Review/Retro separation.
- **Weak answer:** “Move unfinished work to next Sprint and ask the team to go faster.”
- **Strong structure:** goal versus tickets → causes → Review product/direction → Retro working system → reorder work.
- **Spoken example:** “I’d make the actual Increment and missed goal transparent. At Review we inspect the product outcome and decide what matters next. At the Retrospective the Scrum Team examines scope, dependencies, interruptions, and quality. Unfinished work returns for reordering, not automatic carryover.”
- **Likely follow-up:** Which metric would you watch afterward?

#### Q11. Engineering says a feature needs twice the estimate. What do you do?

- **Testing:** Scope, uncertainty, and partnership.
- **Weak answer:** “Hold them to the estimate.”
- **Strong structure:** ask what was learned → outcome and must-have constraints → split/de-scope/sequence → update forecast → communicate impact.
- **Spoken example:** “An estimate is not a promise. I’d ask which assumption changed and whether there is a smaller end-to-end slice that still creates evidence or value. We might reduce scope, address a dependency, or change the date. I’d communicate the new range and decision, not hide uncertainty.”
- **Likely follow-up:** What if the deadline cannot move?

#### Q12. A dependency blocks delivery. How do you respond?

- **Testing:** Risk management and practical adaptation.
- **Weak answer:** “Escalate the other team because they are late.”
- **Strong structure:** impact on goal → owner and evidence → workaround/sequence/decouple → updated scope and stakeholders → prevention learning.
- **Spoken example:** “I’d clarify whether the dependency blocks the Sprint Goal or only one item. Engineering and I would explore a mock, interface contract, smaller slice, or reordered work. I’d align with the dependency owner, expose the forecast, and later improve early dependency discovery.”
- **Likely follow-up:** When should dependencies be found?

### E. Collaboration and conflict

#### Q13. An engineer disagrees with your priority. What do you do?

- **Testing:** Curiosity, evidence, and accountable decision-making.
- **Weak answer:** “Product owns priority, so they must follow it.”
- **Strong structure:** shared goal → invite technical evidence → compare assumptions and consequences → smaller option → decide and revisit condition.
- **Spoken example:** “I’d ask what technical risk or opportunity cost I may be missing. I would explain the customer evidence and goal, then compare options together. If the product priority remains, I’ll explain why; if their evidence changes the decision, I’ll update it openly.”
- **Likely follow-up:** Tell me about a real disagreement. **PERSONAL EVIDENCE REQUIRED.**

#### Q14. Design and Engineering disagree on scope. How do you help?

- **Testing:** Facilitation around outcomes and constraints.
- **Weak answer:** “Split the difference.”
- **Strong structure:** user outcome and critical behavior → technical constraints → alternatives → smallest coherent slice → evidence and guardrails.
- **Spoken example:** “I’d move the discussion from preferred solutions to the user outcome and constraints. We can identify which behavior is essential, compare smaller end-to-end options, and test the highest-risk assumption. A compromise is useful only if it remains usable and safe.”
- **Likely follow-up:** Who makes the final decision?

#### Q15. The team says Product keeps changing requirements. What do you do?

- **Testing:** Ownership and process learning.
- **Weak answer:** “Change is normal in Agile.”
- **Strong structure:** acknowledge cost → inspect examples → distinguish new evidence from ambiguity/preferences → stabilize goal → improve discovery/refinement/change communication.
- **Spoken example:** “I’d inspect recent changes with the team and own avoidable ambiguity. Some change may come from valid evidence, but it still has a cost. I’d improve early stakeholder and engineering involvement, keep the outcome stable where possible, and record what was displaced and why.”
- **Likely follow-up:** How would you know this improved?

### F. Metrics and outcomes

#### Q16. How do you know a Sprint succeeded?

- **Testing:** Separation of activity, delivery, and value.
- **Weak answer:** “All stories were completed and velocity increased.”
- **Strong structure:** Sprint Goal → Done Increment and quality → learning → product outcome over an appropriate window.
- **Spoken example:** “First I check whether the Sprint Goal was achieved with a usable Increment meeting the DoD. Then I inspect what we learned and, when measurable, whether the intended user outcome changed without unacceptable guardrail harm. Ticket completion alone is insufficient.”
- **Likely follow-up:** What if the goal was met but users did not benefit?

#### Q17. Velocity fell 30%. Is that bad?

- **Testing:** Metric literacy and resistance to gaming.
- **Weak answer:** “Yes, productivity fell 30%.”
- **Strong structure:** verify definition/comparability → capacity, work mix, point scale, quality, incidents → goal/outcome → trend and action.
- **Spoken example:** “Not necessarily. Velocity is a team's local planning signal, not value. I’d check leave, support incidents, larger uncertainty, changed estimation, and DoD. If quality and outcomes improved, lower points may not be harmful. I’d investigate the system rather than set a point target.”
- **Likely follow-up:** What delivery metrics would you pair with it?

#### Q18. A feature shipped on time but the user metric did not improve. What now?

- **Testing:** Post-release learning and causal reasoning.
- **Weak answer:** “Marketing needs to drive adoption.”
- **Strong structure:** verify eligibility/exposure and metric → adoption versus usefulness → segmented behavior and qualitative evidence → revise hypothesis or execution → adapt backlog.
- **Spoken example:** “I’d separate whether users encountered the feature, tried it, completed the job, and benefited. I’d inspect segments, instrumentation, and user behavior. The solution or original problem hypothesis may be wrong; I would adapt rather than call shipping success the final outcome.”
- **Likely follow-up:** When would you remove the feature?

### G. Retrospective and learning

#### Q19. How would you run a useful Retrospective?

- **Testing:** Psychological safety and action orientation.
- **Weak answer:** “Ask what went well and badly, then write notes.”
- **Strong structure:** facts and goal → patterns and contributing system → choose controllable high-leverage change → owner/checkpoint → no blame.
- **Spoken example:** “I’d create a safe view of what happened, compare it with the Sprint Goal, and explore process, interaction, tool, and DoD factors. The team chooses one or two useful improvements with an owner or clear working agreement, then checks whether they helped.”
- **Likely follow-up:** What if the same issue repeats?

#### Q20. Tell me about a project that went wrong.

- **Testing:** Honest ownership, diagnosis, adaptation, and learning.
- **Weak answer:** A polished success story disguised as failure, or blaming Engineering.
- **Strong structure:** true context → your responsibility → observable gap → your decision/action → result without invented metrics → learning and changed behavior.
- **Spoken example:** “I would use a real incident and be precise about what I owned. I’d explain what evidence showed the plan was wrong, how I adapted, and what I changed afterward. I would say when an outcome was not measured.”
- **Likely follow-up:** What would you do differently now? **A full personal example requires candidate evidence.**

#### Q21. What would you change after a failed release?

- **Testing:** Incident response plus durable learning.
- **Weak answer:** “Add more QA and approvals.”
- **Strong structure:** contain/recover → evidence and affected users → contributing conditions → targeted prevention and detection → outcome and guardrail.
- **Spoken example:** “First I’d limit customer harm and confirm recovery. Then I’d examine requirement, design, implementation, test, rollout, and monitoring evidence. I’d choose the smallest high-leverage system change—perhaps a specific regression check or staged rollout—rather than adding process everywhere.”
- **Likely follow-up:** How do you avoid a blame culture?

## 18. Hard Agile and product-execution case bank — P0

All cases are **HYPOTHETICAL / INTERVIEW EXERCISES**. Pause after each prompt and answer aloud before reading the reasoning. Clarifying questions are possibilities, not a checklist to recite.

### Beginner 1 — Five requests, capacity for two

**Prompt:** A PM wants five roadmap features this Sprint. Engineering believes only two can become Done. What do you do?

**Clarifying questions:** What Product Goal and user outcome matter? What evidence supports each request? Which work is dependent, risky, or time-sensitive? Is “two” based on comparable capacity and DoD?

**Concepts:** backlog ordering, capacity, opportunity cost, coherent Sprint Goal, estimates.

**Strong reasoning path:** Translate features into problems and outcomes. Compare evidence, value, urgency, risk, dependencies, and effort. Ask Developers what can be Done without reducing quality. Prefer a coherent goal over two unrelated high-status requests. State what waits.

**Trade-offs:** breadth versus a usable end-to-end Increment; responsiveness versus predictability.

**Possible recommendation:** Select the two items that jointly achieve the highest-value Sprint Goal, or split one large item into a usable narrow slice. Keep the other work ordered in the Product Backlog.

**Metrics/evidence:** Sprint Goal result, DoD, affected-user outcome, escaped defects, forecast variation.

**Interviewer follow-ups:** What if the CEO owns the fifth request? What if all five are contractual?

### Beginner 2 — Critical production bug during a Sprint

**Prompt:** A merchant-app bug prevents some restaurants from accepting orders halfway through the Sprint.

**Clarifying questions:** What share and segments are affected? Is there a safe workaround? Is data or money at risk? Does the issue worsen? What current Sprint work would stop?

**Concepts:** incident mitigation, mid-Sprint change, severity/reach, Sprint Goal, cross-functional coordination.

**Strong reasoning path:** Verify and contain harm first. Bring Engineering and Operations together; communicate to affected teams. Check whether mitigation or full repair is needed now. Collaborate on Sprint scope and make displaced work visible. Preserve quality and evidence.

**Trade-offs:** rapid restoration versus risky patch; current goal versus customer harm.

**Possible recommendation:** If the bug materially blocks current orders, interrupt for bounded mitigation and verified repair. Renegotiate Sprint scope; if the goal becomes obsolete, the PO considers cancellation.

**Metrics/evidence:** affected merchants/orders, acceptance and completion, error rate, recovery time, recurrence, neighboring marketplace effects.

**Interviewer follow-ups:** What if only one small merchant is affected? What belongs in the Retrospective?

### Beginner 3 — Feature shipped, customers do not use it

**Prompt:** The team delivered an AI failure-summary feature on time, but eligible customers rarely use it.

**Clarifying questions:** Are users exposed and instrumentation correct? Do they encounter the relevant job? Did they try and abandon? Which segments? What alternatives do they use?

**Concepts:** delivery versus outcome, adoption funnel, discovery, hypothesis, backlog adaptation.

**Strong reasoning path:** Do not blame marketing immediately. Separate opportunity, awareness, trial, completion, correctness, and repeated value. Observe tasks and compare segments. The problem, solution, usability, trust, or targeting assumption may be wrong.

**Trade-offs:** improve, reposition, or remove; more investment versus opportunity cost.

**Possible recommendation:** Run a narrow diagnosis using task eligibility, behavior, and user interviews. Fix a clear friction only if supported; otherwise stop expansion and revisit the problem hypothesis.

**Metrics/evidence:** eligible-task use, completion, repeat use, correct diagnosis, total effort, harmful guidance, qualitative reasons.

**Interviewer follow-ups:** When would you sunset it? What if users praise it in interviews but behavior stays low?

### Intermediate 1 — Urgent enterprise request mid-Sprint

**Prompt:** One large enterprise asks for unattended AI test repair before a renewal meeting next week. The current Sprint Goal is safer human review.

**Clarifying questions:** What outcome drives renewal? Is this a production need, demo request, or roadmap signal? What actions and assets would automation touch? Is there broader evidence? What can be shown safely next week?

**Concepts:** stakeholder pressure, Sprint Goal, discovery, risk and reversibility, opportunity cost.

**Strong reasoning path:** Clarify the underlying customer job and commercial deadline. Do not equate account size with general priority. Ask Engineering and security about failure consequences. Look for a lower-risk demonstration or workflow that preserves the current goal.

**Trade-offs:** revenue risk and learning versus safety, disruption, and roadmap capture.

**Possible recommendation:** Keep the safer-review Sprint Goal, offer a controlled prototype or discovery session for the renewal conversation, and order unattended actions only after evidence and safety criteria. Change course only if verified company risk and feasible mitigation outweigh current value.

**Metrics/evidence:** renewal decision drivers, review delay, repair correctness, harmful changes, eligible accounts, permission failures.

**Interviewer follow-ups:** What if the request comes from 40% of revenue? Who makes the decision?

### Intermediate 2 — Sprint Goal repeatedly missed

**Prompt:** The same team misses its Sprint Goal for the third Sprint. Leaders want stricter commitments.

**Clarifying questions:** Are the goals coherent and measurable? What work became Done? What patterns recur—scope, incidents, dependencies, skills, decisions, or capacity? Did point scales or DoD change?

**Concepts:** empiricism, predictability, systems diagnosis, Review, Retrospective, WIP.

**Strong reasoning path:** Inspect three Sprints as a system. Separate goal quality, planning forecast, flow, quality, and interruptions. Find the constraint and one controllable change. Stricter promises do not create capacity.

**Trade-offs:** ambitious goals versus credible focus; reserved incident capacity versus feature scope.

**Possible recommendation:** Choose a narrower goal, limit concurrent work, surface dependencies before Planning, and reserve evidence-based support capacity. Check the next two Sprints rather than manipulate velocity.

**Metrics/evidence:** goal success, work item age, WIP, cycle-time distribution, interrupt load, blocked time, escaped defects.

**Interviewer follow-ups:** When is team capability actually the issue? How do you communicate this to leadership?

### Intermediate 3 — Backlog constantly changing

**Prompt:** Engineering says Product changes the backlog so often that the team wastes work.

**Clarifying questions:** Product Backlog order or Sprint Backlog scope? How often, why, and how late? Which work was discarded? Was the Product Goal stable? Were changes driven by evidence or preferences?

**Concepts:** adaptable Product Backlog, Sprint protection, discovery, refinement, change cost.

**Strong reasoning path:** A changing Product Backlog is normal; uncontrolled current-work changes are different. Review examples, quantify rework, and own avoidable ambiguity. Preserve outcome direction, involve Engineering earlier, and make the reason and opportunity cost of changes transparent.

**Trade-offs:** responsiveness versus focus; early discovery effort versus later rework.

**Possible recommendation:** Establish a clear Sprint change rule around goal risk, strengthen weekly refinement of near-term items, record major assumptions, and inspect rework and useful learning.

**Metrics/evidence:** scope changes after start, discarded work, blocked age, decision latency, Sprint Goal result, causes of change.

**Interviewer follow-ups:** Would you freeze requirements? What if customer evidence genuinely changes every week?

### Intermediate 4 — Engineering requests two Sprints for technical debt

**Prompt:** Engineering wants two full Sprints to replace an internal service before adding more agent autonomy.

**Clarifying questions:** Which failures or future changes does the service affect? What incident, security, or delivery evidence exists? Is replacement the smallest option? What happens if delayed? What product work waits?

**Concepts:** technical debt, autonomy risk, enabling work, slicing, Product Goal.

**Strong reasoning path:** Translate debt into customer and business consequences. Ask for alternatives: isolate risky actions, add verification, replace one path, or stage migration. Compare the cost of delay on both product and debt.

**Trade-offs:** visible feature progress versus safety and future adaptability; full replacement versus incremental risk reduction.

**Possible recommendation:** If the service creates a verified unsafe boundary or blocks validation, set a product-relevant reliability goal and deliver the smallest usable migration/guardrail slice first. Do not approve a blanket rewrite without evidence and checkpoints.

**Metrics/evidence:** related incidents, change failure, delivery time in affected area, security evaluation, rollback success, autonomy error severity.

**Interviewer follow-ups:** How do you make this visible to customers? What if no incident has happened yet?

### Pressure 1 — Velocity falls 30%

**Prompt:** An executive asks why team velocity fell 30% and demands it return next Sprint.

**Clarifying questions:** Same team, point scale, Sprint length, capacity, work type, and DoD? Was there leave, onboarding, incidents, or unusually uncertain work? Were the Sprint Goal and outcomes affected?

**Concepts:** velocity misuse, forecast versus KPI, Goodhart's law, flow and outcome metrics.

**Strong reasoning path:** Validate comparability before interpreting. Explain that points are subjective and local. Investigate system causes and actual customer impact. Refuse the false equivalence without dismissing the executive's need for predictability.

**Trade-offs:** simple reporting versus valid evidence; short-term point output versus quality and value.

**Possible recommendation:** Report Sprint Goal, usable Increments, quality, cycle-time range, interrupt load, and product outcome. Use velocity only as internal historical context; remove any target that rewards point inflation.

**Metrics/evidence:** capacity, goal success, throughput by comparable work class, cycle time, escaped defects, product outcome.

**Interviewer follow-ups:** Give the executive one number. What if cycle time also worsened?

### Pressure 2 — Country teams demand different marketplace priorities

**Prompt:** Three country teams request different merchant, driver, and buyer improvements. Central Engineering can support one major initiative this quarter.

**Clarifying questions:** What company outcome and constraints apply? Are the mechanisms comparable across cities? How severe, reachable, and time-sensitive is each problem? Can platform capability and local operations be separated?

**Concepts:** strategy, segmentation, shared platform, local marketplace dynamics, dependencies, stakeholder conflict.

**Strong reasoning path:** Do not average incompatible markets or reward political pressure. Define a shared outcome, normalize evidence carefully, and identify whether one platform capability unlocks several local responses. Include Operations and Analytics, not only Engineering.

**Trade-offs:** local fit versus scalable platform investment; largest market versus greatest marginal impact; speed versus evidence.

**Possible recommendation:** Choose the initiative with the strongest verified problem, strategic fit, reusable capability, and cost of delay; offer bounded local operational tests elsewhere. Publish the decision rule and next review point.

**Metrics/evidence:** segmented completion, cancellation, preparation/assignment time, contribution, affected users, dependency unlock, experiment spillovers.

**Interviewer follow-ups:** What if the smallest country has the most severe harm? How do you prevent central bias?

### Pressure 3 — Serious defect one day before release

**Prompt:** QA finds that an AI-generated test can silently remove a payment assertion one day before a public release. Marketing has announced the date.

**Clarifying questions:** Is the flaw in the product, generated output, or test workflow? Which users and actions are affected? Can the risky path be disabled independently? Has harm occurred? What does the DoD or release criterion require?

**Concepts:** quality, DoD, release decision, safety boundary, scope reduction, stakeholder pressure.

**Strong reasoning path:** Establish severity and reproducibility. A calendar does not make unsafe work Done. Consider disabling generation for this action, requiring review, reducing release scope, or delaying. Preserve evidence and communicate decision and customer impact.

**Trade-offs:** date credibility versus product trust and financial risk; narrow disablement versus full delay.

**Possible recommendation:** Block the unsafe path and release only if the remaining Increment independently meets DoD and user promises. Otherwise delay, explain the concrete risk, repair and verify. Later inspect why meaningful assertion preservation was missed.

**Metrics/evidence:** affected action classes, detection accuracy, harmful proposals applied, review effectiveness, regression result, post-release incidents.

**Interviewer follow-ups:** The CEO says ship anyway—what do you say? What changes at Review versus Retro?

## 19. Context practice: Katalon and ShopeeFood — P0

These are **HYPOTHETICAL / INTERVIEW EXERCISES**, not claims about either company's internal process, product roadmap, or interview questions.

### 19.1 Katalon-like B2B SaaS, developer tooling, and testing scenarios

| Situation | Product reasoning | Agile delivery implication |
|---|---|---|
| One enterprise requests an AI feature mid-Sprint | Clarify its job, evidence, deadline, reach, and safety risk | Protect the Sprint Goal; use a prototype or backlog reorder unless verified harm justifies interruption |
| Generated tests are inconsistent | Segment error types and evaluate meaningful assertions, not only pass rate | Narrow scope, strengthen acceptance criteria and DoD, and deliver an inspectable Increment |
| QA workflow research contradicts the roadmap | Treat the roadmap as a hypothesis; compare observed jobs with assumed demand | Reorder Product Backlog and adapt future goals rather than finish low-value scope because it was planned |
| An agent/MCP integration reveals security work | Define authorization, data exposure, action scope, and failure recovery | Technical/security work may be part of value and DoD, not an optional afterthought |
| Engineering wants debt work before greater autonomy | Link debt to unsafe actions, incidents, change difficulty, or verification gaps | Set a bounded product-relevant reliability goal and inspect progress instead of approving an unbounded rewrite |
| AI safety evaluation fails before release | Identify failed behavior, severity, affected users, and possible isolation | Do not lower DoD silently; remove risky scope, repair and verify, or delay |
| Product Director asks why a feature slipped | Explain what was learned, which goal/outcome changed, new forecast, and options | Do not hide behind story points; show dependency, quality, scope, and decision evidence |

**One complete loop — HYPOTHETICAL:**

```text
Observe QA engineers reviewing generated changes
→ problem: uncertain changes make review slow and risky
→ Product Goal: trustworthy review before applying changes
→ order evidence view, permissions, conflict handling, then broader automation
→ Sprint Goal: inspect and safely reject one proposed change
→ build and test a small usable Increment
→ Review: users understand the difference but miss requirement provenance
→ evidence: correct decisions improve only when source evidence is visible
→ adapt Product Backlog: provenance before more autonomous actions
```

### 19.2 ShopeeFood-like high-scale marketplace scenarios

| Situation | Product reasoning | Cross-functional delivery implication |
|---|---|---|
| Driver cancellation spikes mid-Sprint | Verify time, city, route, merchant, order type, and immediate harm | Product and Engineering need Analytics and Operations evidence; mitigate severe harm before normal roadmap work |
| Promo experiment creates imbalance | Trace buyer demand into merchant load, driver waiting, completion, and economics | Adapt eligibility or stop rule; Marketing and Operations may own essential actions outside software |
| Merchant app prevents order acceptance | Measure reach and workaround; distinguish app fault, connectivity, menu state, and merchant behavior | Incident response may interrupt the Sprint; support and city teams help contain impact |
| Experiment requires product plus operations work | Define both interventions and ownership before calling it ready | A shipped switch without trained operations or merchant communication is not the complete experiment |
| KPI changes unexpectedly after rollout | Check definitions, exposure, segments, counterfactual, and second-order effects | Roll back, limit, or continue conditionally; update backlog from observed mechanism |
| Country/city teams request different priorities | Compare local severity and strategic fit; avoid misleading averages | Central platform work, local configuration, and operations can have different cadences and owners |

Marketplace work often coordinates **Product, Engineering, Analytics, Operations, Marketing, and merchant/driver teams**. Scrum events can make evidence and decisions visible. They do not substitute for product strategy, marketplace diagnosis, or economic judgment.

## 20. PRJ226: strict truth boundary — P0

### 20.1 Evidence audit

| Statement | Status | Safe use |
|---|---|---|
| PRJ226 is the candidate's main side project | **SELF-REPORT** in the repository evidence ledger | May call it a side project |
| PRJ226 was primarily a solo project | **SELF-REPORT** in the current task | May explain why formal team Scrum was not used |
| PRJ226 did not formally use Agile or Scrum | **SELF-REPORT** in the current task | Must not claim formal Scrum experience from it |
| It had a Scrum Team, Product Owner, Scrum Master, Sprints, events, story points, or velocity | **UNSUPPORTED / contradicted by current self-report** | Do not claim |
| The candidate broke work into increments, validated changes, reprioritized from evidence, or used review gates | **PERSONAL EVIDENCE REQUIRED** | Add only after one concrete real example is supplied |
| Users, customer outcomes, architecture, deployed agents, MCP, metrics, or successful results | **PERSONAL EVIDENCE REQUIRED** | Do not infer from the project name or this exercise |

### 20.2 Layer A — honest interview answers

The safe base answer is:

> “PRJ226 was primarily a solo side project, and I did not formally run Agile or Scrum. I would not claim a Scrum Team, Sprints, or ceremonies that did not exist. I understand the professional framework, and I can explain how I would apply it in a cross-functional team.”

Do **not** add “I worked iteratively,” “I validated each increment,” or “I reprioritized from evidence” until a real incident supports it.

#### “Have you worked in Agile?”

> “I haven't worked in a formal Scrum environment through PRJ226, so I would not claim that experience. It was primarily a solo side project. My understanding is that Agile is about small value increments, feedback, collaboration, and adaptation. In a Scrum team I would connect the Product Goal, ordered backlog, Sprint Goal, usable Increment, and learning.”

If another job supplies real Agile experience, use that separately after verifying the actual team practices.

#### “What Agile methodology did your project use?”

> “PRJ226 did not formally use an Agile methodology. I managed a solo project, so Scrum accountabilities and team events would be misleading labels. I can describe my actual way of working once I select a concrete example, and I can separately explain how Scrum could structure a team version.”

#### “Tell me about a Sprint you worked on.”

> “I don't have a truthful PRJ226 Sprint example because the project did not use formal Sprints. I would rather be clear about that. I can discuss a real scoped work period if I establish the facts, but I would not rename it a Sprint.”

**PERSONAL EVIDENCE REQUIRED:** a real project period, objective, work, change, result, and learning.

#### “How did you prioritize your backlog?”

> “I did not maintain a formal Scrum Product Backlog for PRJ226. Before claiming an informal method, I would need to give a real decision between competing work. In a Scrum team, I would order the Product Backlog by goal alignment, customer evidence, value, risk, dependencies, effort, and opportunity cost.”

#### “How did you deal with changing requirements?”

> “I would need a concrete PRJ226 example before claiming how I handled change. Professionally, I would clarify the new evidence and urgency, check the current goal, involve Engineering in cost and risk, and make any displaced work explicit.”

#### “How did you work with engineers?”

> “PRJ226 was primarily solo, so it is not evidence of collaboration with an Engineering team. I would use a separate verified work example if I have one. My team approach would be to bring problem context and priorities, ask engineers to challenge feasibility and risk, and collaborate on the smallest useful scope.”

#### “What happened when work slipped?”

> “I need a real incident before describing a PRJ226 slip. I would not invent a cause or result. In a Scrum setting I would separate the Sprint Goal from ticket completion, inspect the product at Review, improve the working system at the Retrospective, and reorder unfinished work.”

#### “How would you apply Scrum to PRJ226?”

> “I would treat this as a thought experiment, not project history. I would first define a Product Goal and users, then create one ordered Product Backlog. A cross-functional Scrum Team would choose a focused Sprint Goal, produce a usable Increment meeting a shared DoD, inspect it with stakeholders, and adapt.”

### 20.3 Layer B — HYPOTHETICAL / INTERVIEW EXERCISE only

> **This section did not happen historically. It must never be retold as PRJ226 experience.** Product behavior below is invented for learning because PRJ226 capabilities are not established by repository artifacts.

**Hypothetical Product Goal:** Help a user retrieve useful project knowledge with less manual context management while preserving provenance and control.

**Possible ordered Product Backlog:**

1. Define one target user's knowledge-retrieval job and baseline.
2. Retrieve bounded project knowledge.
3. Show source provenance with each answer.
4. Prevent mutation of authoritative state without explicit authorization.
5. Handle missing, conflicting, or stale sources.
6. Abstract a provider only if evidence shows that flexibility is valuable.
7. Evaluate task success, unsupported claims, latency, and user effort.

**Hypothetical Sprint Goal:** “Allow the user to retrieve grounded project knowledge without permitting the model to mutate authoritative state.”

**Possible selected items:** bounded read access, source display, denial of write attempts, missing-source behavior, and an evaluation set.

**Possible user story — COMMON PRACTICE:** “As a project contributor, I want each answer linked to its project source so that I can check it before using it.”

**Possible acceptance criteria:** answer identifies the source; user can open the referenced passage; unavailable evidence is stated; an attempted write is denied; conflicting sources are surfaced rather than silently merged.

**Possible Definition of Done:** implementation reviewed; relevant automated, permission, and integration checks pass; unauthorized writes are blocked; required operational logging and documentation are complete; the Increment works with existing integrated behavior. This is one invented DoD, not a universal standard.

**Possible Sprint Review learning:** Stakeholders can check sources but cannot tell which source is authoritative when files conflict. Adapt the Product Backlog by ordering conflict visibility and authority rules above provider abstraction.

**Possible Retrospective learning:** Permission assumptions appeared too late. Add an early threat-and-access discussion during refinement and check whether it reduces late rework next Sprint.

```text
Hypothetical Product Goal
→ ordered Product Backlog
→ focused Sprint Goal
→ selected work + delivery plan
→ usable Increment meeting DoD
→ Sprint Review product learning
→ Retrospective process learning
→ adapted backlog and working agreement
```

## 21. Decision-centered teaching case studies — P1

All five are **SYNTHESIZED HYPOTHETICAL TEACHING CASES**, not real published company outcomes. Company names are deliberately omitted. They apply principles from the cited sources without inventing evidence.

### Case study 1 — B2B SaaS: the requested dashboard

- **Initial situation:** Account teams request a large executive dashboard after renewal conversations.
- **Uncertainty/problem:** The team does not know which decision executives cannot make or whether current data is trusted.
- **Operating approach:** The product trio observes review meetings and prototypes a small risk summary while delivery continues on reliability work.
- **Feedback:** Executives rarely need more charts; they need to identify accounts with unresolved configuration failures.
- **Adaptation:** Reorder the backlog around one actionable failure view and data-quality checks; defer the dashboard suite.
- **Result:** A small usable Increment tests the decision workflow. No invented adoption or revenue result is claimed.
- **PM lesson:** Collaboration and small increments protect the team from scaling an unsupported request.

### Case study 2 — Developer tool: plugin architecture or one integration

- **Initial situation:** A team wants a universal plugin architecture before supporting a requested CI provider.
- **Uncertainty/problem:** It is unclear whether customers need many providers or one reliable integrated path.
- **Operating approach:** Define a Product Goal around successful CI diagnosis, build the thinnest integrated provider slice, and record extension assumptions.
- **Feedback:** Authentication and permission differences—not connector code—create most setup failure.
- **Adaptation:** Prioritize guided permissions and observable errors; delay general abstraction until a second provider tests the common design.
- **Result:** The team learns the real constraint without committing to a broad architecture. No company performance claim is made.
- **PM lesson:** Simplicity means maximizing unnecessary work not done, not avoiding sound design.

### Case study 3 — Consumer marketplace: lunch cancellation spike

- **Initial situation:** Buyer cancellations rise during lunch, and the growth team requests more driver incentives.
- **Uncertainty/problem:** Cancellation can arise from assignment, restaurant preparation, ETA promises, price, or app faults.
- **Operating approach:** Product, Analytics, and Operations segment the funnel; Engineering improves missing timestamps while local teams inspect affected merchants.
- **Feedback:** Drivers are assigned, but long pickup waits at a small merchant group make quoted ETAs unreliable.
- **Adaptation:** Test merchant load controls and readiness accuracy before adding broad supply incentives.
- **Result:** The team has a mechanism-specific intervention and guardrails; no invented commercial improvement is claimed.
- **PM lesson:** Agile events support coordination, but systems diagnosis selects the useful change.

### Case study 4 — AI product: autonomy after trust

- **Initial situation:** Leadership wants an assistant to apply generated changes automatically to improve completion speed.
- **Uncertainty/problem:** Generated changes sometimes alter meaningful assertions, and reviewers cannot see source evidence.
- **Operating approach:** Deliver a review-first Increment with diff, provenance, rejection, permission checks, and outcome evaluation.
- **Feedback:** Reviewers safely approve simple convention changes but reject ambiguous requirement changes.
- **Adaptation:** Automate only a narrow, reversible action class with strong verification; keep risky changes reviewable.
- **Result:** Autonomy becomes evidence-based and segmented. No fabricated accuracy or time-saving metric is claimed.
- **PM lesson:** Agile adaptation can reduce scope while increasing product value and safety.

### Case study 5 — Failed Agile implementation: ceremonies without empiricism

- **Initial situation:** An organization renames managers Product Owners, schedules Daily Scrums, and requires velocity to rise every Sprint.
- **Uncertainty/problem:** Roadmap scope stays fixed, stakeholders skip Reviews, teams hide quality work, and points inflate.
- **Operating approach:** Work is pushed through mini-waterfall Sprints: specification, coding, late testing, then carryover.
- **Feedback ignored:** Customers do not use delivered features; repeated Retrospectives produce no action because leadership judges teams by points.
- **Adaptation:** None at first—the important failure. A recovery would stop cross-team velocity targets, restore outcome-focused Product Goals, involve stakeholders in Review, protect DoD, and empower backlog decisions.
- **Result:** The first approach is Agile in vocabulary only. The recovery remains a proposed teaching response, not a reported outcome.
- **PM lesson:** Events without transparency, inspection, empowerment, and adaptation create ritual, not agility.

## 22. Common Agile myths — P0

### Myth 1 — Agile equals Scrum

- **Why wrong:** Agile is a philosophy; Scrum is one framework that can support it.
- **Better model:** Choose a delivery approach that preserves value, feedback, and adaptation.
- **Short example:** A support team can use Kanban flow without Sprints and still work consistently with Agile values.

### Myth 2 — Agile means no planning

- **Why wrong:** Scrum includes Product Goal, Product Backlog, Sprint Goal, and Sprint Planning.
- **Better model:** Plan continuously at the level current evidence supports.
- **Short example:** Keep a product direction while revising feature sequence after user evidence.

### Myth 3 — Agile means no documentation

- **Why wrong:** The Manifesto values working software more; it does not say documents have no value.
- **Better model:** Create documentation needed for shared understanding, quality, operation, and risk.
- **Short example:** Permission rules and an API contract can be essential to a Done integration.

### Myth 4 — Requirements can change anytime without cost

- **Why wrong:** Change creates rework, delay, and opportunity cost; Scrum protects the Sprint Goal.
- **Better model:** Respond deliberately, clarify urgency, and expose displaced work.
- **Short example:** Reorder a normal request for next Sprint; interrupt for verified severe harm.

### Myth 5 — Agile simply means move fast

- **Why wrong:** Speed without quality or useful feedback can deliver harm faster.
- **Better model:** Shorten learning cycles while preserving sustainable pace and technical excellence.
- **Short example:** Release a narrow verified review flow before risky automatic actions.

### Myth 6 — Agile is the Daily Stand-up

- **Why wrong:** Agile is values and principles; the Daily Scrum is one event in Scrum.
- **Better model:** Use the Daily Scrum for Developers to inspect progress toward the Sprint Goal and adapt their plan.
- **Short example:** Discuss a new blocker and change the day's plan, not report to the PM.

### Myth 7 — A Sprint is mini-waterfall

- **Why wrong:** Sequential analysis, coding, and testing that produce no usable Increment defeats the learning loop.
- **Better model:** Create a small end-to-end Done Increment; discovery and testing can occur throughout.
- **Short example:** Complete one permission-safe failure view rather than analyze ten views, code ten, then test late.

### Myth 8 — Product Owner is a project manager

- **Why wrong:** The PO is accountable for product value and backlog management, not assigning tasks and tracking utilization.
- **Better model:** Product sets goal and order; Developers self-manage delivery.
- **Short example:** The PO explains why failure diagnosis matters; Developers design the technical plan.

### Myth 9 — Velocity equals productivity

- **Why wrong:** Velocity uses local subjective estimates and can change without value or real output changing.
- **Better model:** Use it cautiously for one team's forecast and inspect flow, quality, goals, and outcomes.
- **Short example:** Doubling point values doubles reported velocity while nothing else changes.

### Myth 10 — More story points means a better team

- **Why wrong:** Point scales and work contexts differ; targets invite inflation and easier work.
- **Better model:** Compare a team with its goals, customer value, quality, and improvement evidence.
- **Short example:** A lower-point security fix can protect more value than many small features.

### Myth 11 — Every backlog item must be a user story

- **Why wrong:** Scrum does not require user stories, and not all useful work fits the format.
- **Better model:** Describe work in the form that makes value, scope, and verification clear.
- **Short example:** “Investigate duplicate payment mechanism” is a valid learning item.

### Myth 12 — Sprint Review is only a demo

- **Why wrong:** It is a working session to inspect outcome and changed context and decide what to do next.
- **Better model:** Use product evidence and stakeholder collaboration to adapt the Product Backlog.
- **Short example:** Low usage causes the team to pause expansion and investigate the workflow.

### Myth 13 — Retrospective is a blame meeting

- **Why wrong:** Its purpose is improving quality and effectiveness, not finding a person to punish.
- **Better model:** Inspect contributing conditions and choose a controllable system improvement.
- **Short example:** Add earlier dependency review instead of blaming the engineer blocked by an API.

### Myth 14 — Definition of Done equals acceptance criteria

- **Why wrong:** Acceptance criteria concern one item's expected behavior; DoD is the Increment's shared quality state.
- **Better model:** Use both when helpful and keep their scopes distinct.
- **Short example:** “Reject changes nothing” is a criterion; integrated tests and required review belong to the DoD.

## 23. Beginner mental map — P0

```text
AGILE
├── Values and Principles
│   ├── customer value and frequent delivery
│   ├── people and collaboration
│   ├── responsiveness and simplicity
│   └── sustainable pace and technical quality
├── Empiricism
│   ├── Transparency
│   ├── Inspection
│   └── Adaptation
├── Scrum
│   ├── Accountabilities
│   │   ├── Product Owner
│   │   ├── Developers
│   │   └── Scrum Master
│   ├── Events
│   │   ├── Sprint
│   │   ├── Sprint Planning
│   │   ├── Daily Scrum
│   │   ├── Sprint Review
│   │   └── Sprint Retrospective
│   ├── Artifacts
│   │   ├── Product Backlog
│   │   ├── Sprint Backlog
│   │   └── Increment
│   └── Commitments
│       ├── Product Goal
│       ├── Sprint Goal
│       └── Definition of Done
├── Product Discovery
│   └── right problem and promising solution
├── Product Delivery
│   └── build, verify, ship, operate, improve
├── Backlog and Prioritization
│   └── value, evidence, risk, effort, dependency, opportunity cost
├── Quality
│   └── acceptance criteria and Definition of Done
├── Learning and Feedback
│   └── Review product; retrospect on working system
├── Metrics
│   └── flow and delivery evidence
└── Product Outcomes
    └── customer and business value with guardrails
```

Central reflex:

> **Problem → Hypothesis → Small Increment → Feedback → Evidence → Adapt.**

## 24. Audio Overview: one Agile product story — P0

Imagine a testing-product team hearing the same request: “Give us faster AI test generation.” The team could plan a large generator, assign months of work, and celebrate when it ships. But faster generation is a proposed solution, not yet the customer problem.

The team observes QA engineers during failed-test work. It learns that generation takes five minutes, but reviewing uncertain changes and finding source evidence takes much longer. Some suggestions even weaken important assertions. Now the team has a better problem: reviewers cannot judge a proposed change quickly and safely.

The Product Owner connects that evidence to a Product Goal: help QA teams make trustworthy release decisions. The Product Backlog contains many possibilities—faster generation, source provenance, a diff view, permission checks, failure grouping, and broader automation. The Product Owner orders source evidence and safe review above unattended action because they address the observed constraint and reduce risk.

At Sprint Planning, the whole Scrum Team creates one Sprint Goal: let a QA engineer inspect and safely reject one AI-proposed change. Developers select a realistic slice and decide how to build it. The Sprint Backlog includes the goal, selected items, and their technical plan.

During the Sprint, the Daily Scrum is not a report to the PM. Developers inspect whether they are moving toward the goal. When conflict handling is harder than expected, they collaborate with the Product Owner and reduce a secondary filter without endangering the goal. Quality does not decrease.

The resulting Increment shows the original and proposed change, links the requirement source, blocks unauthorized application, and leaves the test unchanged after rejection. It meets this product's Definition of Done. Coding alone would not have been enough.

At Sprint Review, the team and stakeholders use the working result. Reviewers understand simple changes, but a conflicting source makes them hesitate. That is product learning. The Product Backlog adapts: source-conflict visibility moves ahead of faster generation.

At the Retrospective, the Scrum Team examines how it worked. Permission questions appeared late, so it adds an early access-risk discussion to refinement. That is process learning. Review inspected the product and next direction; Retrospective inspected quality and effectiveness.

The story is Agile because evidence changed the decision and a small usable Increment created the next learning—not because the team attended meetings. The reflex is: problem, priority, small Increment, build, inspect, learn, adapt.

## 25. P0 flashcards — 25 cards

### 1. Agile versus Scrum

**Agile** is a philosophy of value, collaboration, feedback, and adaptation. **Scrum** is one lightweight framework that can support it.

### 2. Scrum versus Kanban

Scrum uses a small self-managing team, goals, and fixed-length Sprints. Kanban optimizes value flow by defining/visualizing workflow, controlling WIP, managing items, and improving flow.

### 3. Why Agile exists

Complex product work cannot be predicted perfectly. Small increments and feedback limit exposure to wrong assumptions.

### 4. Empiricism

Make work visible, inspect observed results, and adapt: **transparency → inspection → adaptation**.

### 5. Product Owner

Accountable in Scrum for maximizing product value and effective Product Backlog management.

### 6. Developers

Create a usable Increment, plan and adapt Sprint work, follow DoD, and decide how delivery is done.

### 7. Scrum Master

Accountable for establishing Scrum and enabling Scrum Team effectiveness; not a task administrator.

### 8. PM versus Product Owner

PO is an official Scrum accountability. PM often covers broader strategy, market, discovery, and outcomes. The roles may overlap or be split.

### 9. Product Backlog

Emergent, ordered source of work needed to improve the product; its commitment is the Product Goal.

### 10. Sprint Backlog

Developers' current plan: Sprint Goal, selected Product Backlog items, and delivery plan.

### 11. Increment

A usable, integrated, verified step toward the Product Goal that meets the DoD.

### 12. Product Goal versus Sprint Goal

Product Goal is the longer-term target; Sprint Goal is the single objective for one Sprint.

### 13. Acceptance criteria versus DoD

Criteria clarify one item's behavior; DoD is the shared quality state required for the Increment.

### 14. Sprint Review versus Retrospective

Review inspects product outcome and next direction with stakeholders. Retrospective inspects the Scrum Team's way of working to improve quality/effectiveness.

### 15. Daily Scrum

A 15-minute Developers' event to inspect progress toward the Sprint Goal and adapt the plan—not a manager status meeting.

### 16. Backlog refinement

Ongoing clarification and decomposition of Product Backlog items; an official Scrum activity, not a formal Scrum event.

### 17. User story status

A common conversation format, not a mandatory Scrum requirement and not the same as the customer problem.

### 18. Story points versus time

Points are a team's relative sizing convention. Five points do not mean five days.

### 19. Velocity versus customer value

Velocity may support one team's forecasting; it is not a customer outcome or cross-team productivity score.

### 20. Mid-Sprint change

Clarify urgency and harm, protect the Sprint Goal, involve Developers, and expose opportunity cost. Agile does not mean accept everything.

### 21. Sprint cancellation

Only the Product Owner can cancel, and it may be considered when the Sprint Goal becomes obsolete.

### 22. Technical debt

Internal deficiencies that add risk or extra effort to future change; prioritize their product consequences, not the label.

### 23. Discovery versus delivery

Discovery decides what is worth building; delivery builds, ships, operates, and improves it. They can overlap.

### 24. Delivery metric versus outcome

Flow or completion evidence shows how work moved. Product outcomes show whether customer/business value changed.

### 25. Honest PRJ226 mapping

PRJ226 was self-reported as primarily solo and not formal Scrum. Never rename work periods, roles, or meetings as Scrum; keep team application hypothetical.

## 26. Conceptual quiz — 20 questions

Answer without looking back.

1. Why can a detailed long-term plan be risky in complex product development?
2. What does “left over right” in the Agile Manifesto mean, and what does it not mean?
3. How can documentation support rather than oppose Agile delivery?
4. Why are Agile, Scrum, and Kanban not synonyms?
5. What three empirical pillars make Scrum's inspection useful?
6. How does the Product Owner maximize value without assigning Developers' tasks?
7. Why might a Product Manager and Product Owner be the same person in one company but separate in another?
8. How do Product Goal, Product Backlog, and Sprint Goal connect?
9. Why is the Sprint Backlog described as a plan by and for Developers?
10. What makes an Increment more than finished code?
11. Why can Sprint Review change future product direction?
12. Why is a Retrospective not the right place for stakeholder feature feedback?
13. Why is refinement important even though it is not a formal Scrum event?
14. Why is a user story not the same as a customer problem?
15. How do acceptance criteria and DoD answer different questions?
16. Why can five story points not be converted universally into five days?
17. Why can higher velocity coexist with lower customer value?
18. How can technical debt reduce product responsiveness?
19. Why should unfinished work not move automatically to the next Sprint?
20. How can discovery and delivery inform each other continuously?

### Conceptual answer cues

1. Uncertain needs and technology make early assumptions fragile. 2. Both sides matter; prioritize the left when in tension. 3. Use necessary, current documentation for understanding and quality. 4. Philosophy, Sprint framework, and flow strategy have different scopes. 5. Transparency, inspection, adaptation. 6. Order by value and provide context while Developers select and plan delivery. 7. Scrum defines accountability, not every company job design. 8. Long-term target shapes emergent work; one Sprint goal advances it. 9. Developers own and update the delivery plan. 10. Usable, integrated, verified, and meeting DoD. 11. Stakeholders inspect outcome and changed context. 12. Retro improves the Scrum Team's working system. 13. Near-term work needs sufficient shared understanding. 14. A story expresses a possible capability. 15. Item behavior versus Increment-wide quality. 16. Points are local and relative. 17. Points can change or fund unused/harmful output. 18. Debt adds risk, incidents, and change effort. 19. Value and order may have changed. 20. Feasibility informs options; Increments create customer evidence.

## 27. Scenario quiz — 10 questions

Try the decision before reading the cues.

1. A sales leader asks for a feature mid-Sprint and says only “the customer is important.” What do you clarify before changing work?
2. Developers finish every selected item, but the items do not produce a usable user flow. Did the Sprint necessarily succeed?
3. A production bug affects 0.2% of users but can expose private data. How should severity and reach influence priority?
4. Velocity drops after the team strengthens its DoD. What comparisons prevent a wrong conclusion?
5. A PO orders a feature first, but Developers reveal an unplanned security dependency. What should happen?
6. Sprint Goals are missed because support incidents consume 25% of capacity. What system options would you test?
7. Users ask for a dashboard, but observation shows they cannot trust the source data. What belongs earlier in the Product Backlog?
8. Engineering asks for a rewrite but cannot connect it to incidents, risk, or future change. How do you move the discussion forward?
9. A promo raises placed orders but also merchant rejection and driver wait. Is the Sprint or experiment successful?
10. An interviewer asks for a PRJ226 Sprint story. How do you answer without weakening your candidacy or inventing experience?

### Scenario answer cues

1. Underlying job, deadline/harm, evidence, reach, Sprint Goal impact, cost, and displaced work. 2. No; inspect Sprint Goal, Increment, DoD, and intended value. 3. Low reach does not erase severe consequence; contain and assess likelihood/exposure. 4. Capacity, same point scale, goal, quality, escaped defects, flow, and outcome. 5. Collaborate, make risk visible, and renegotiate scope/order while preserving quality and goal where possible. 6. Reserve evidence-based capacity, reduce WIP/scope, improve incident root causes, and inspect trends. 7. Data quality/provenance and a smaller decision-support slice. 8. Ask for affected area, recurring cost/risk, delay consequence, smallest reduction, and evidence. 9. Shipping or orders alone are insufficient; assess completion, all sides, economics, and causal comparison. 10. Say PRJ226 did not use formal Sprints, offer a real scoped incident only after facts are established, then explain a hypothetical Scrum application separately.

## 28. Speakable interview English — P0

- “I'd first clarify whether this change affects the Sprint Goal.”
- “I’d separate an urgent production issue from a new feature request.”
- “The backlog should reflect current priorities, but changing current work has an opportunity cost.”
- “I’d ask what new evidence makes this urgent now.”
- “I’d make the displaced work and revised forecast visible.”
- “An estimate is a forecast, not a guarantee.”
- “Five story points do not mean five days.”
- “I wouldn't treat velocity as a customer outcome.”
- “A lower velocity is a signal to investigate, not proof of lower productivity.”
- “I’d compare severity, reach, risk, learning value, and cost of delay.”
- “I want Engineering to challenge my assumptions about effort and technical risk.”
- “The main trade-off is responsiveness versus disrupting focused work.”
- “Sprint Review inspects the product and next direction.”
- “The Retrospective improves how the Scrum Team works.”
- “Coding complete does not automatically mean Done.”
- “This criterion is item-specific; the DoD is the shared Increment quality bar.”
- “I’d separate finishing tickets from achieving the Sprint Goal.”
- “I would reorder unfinished work instead of carrying it over automatically.”
- “This technical work matters if it reduces customer risk or preserves future delivery speed.”
- “I’d look for the smallest end-to-end slice that creates useful evidence.”
- “Discovery asks whether we should build it; delivery asks whether we can build and sustain it.”
- “Agile welcomes useful learning, not uncontrolled change.”
- “I haven't used formal Scrum in that project, so I wouldn't claim that experience.”
- “PRJ226 was primarily solo; I can separately explain how I would apply Scrum in a team.”
- “That example is hypothetical and not part of my project history.”

## 29. Sources and evidence boundaries

### P0 authoritative sources

- [Manifesto for Agile Software Development](https://agilemanifesto.org/) — four values and the important “left more than right” nuance.
- [Principles behind the Agile Manifesto](https://agilemanifesto.org/principles) — twelve principles grouped in this note for interview use.
- [Official Scrum Guide, November 2020](https://scrumguides.org/scrum-guide.html) and [official download page](https://scrumguides.org/download) — current Scrum definition, theory, values, accountabilities, events, artifacts, commitments, Sprint change, and cancellation.
- [The Kanban Guide, May 2025](https://kanbanguides.org/the-kanban-guide/2025.5/pdf/kanban-guide.v2025.5.en.pdf) — flow strategy, workflow visualization, WIP control, active management, improvement, and minimum flow metrics.

### Reputable interpretation sources

- [Scrum.org: Product Backlog Refinement](https://www.scrum.org/resources/product-backlog-refinement) — refinement as an ongoing activity rather than a prescribed event.
- [Scrum.org: Story points across teams](https://www.scrum.org/resources/blog/deciphering-enigma-story-points-across-teams) — limits of subjective points and cross-team comparison.
- [Atlassian: User stories](https://www.atlassian.com/agile/project-management/user-stories) — user-focused story format and conversation practice.
- [Atlassian: Scrum artifacts](https://www.atlassian.com/agile/scrum/artifacts/) — burndown as a common tool, not an official Scrum artifact.
- [Product Talk: discovery and delivery](https://www.producttalk.org/adopting-continuous-product-discovery/) — discovery as deciding what to build and delivery as building/shipping; Dual-Track is labeled common practice here.
- [Martin Fowler: Technical Debt](https://martinfowler.com/bliki/TechnicalDebt.html) — debt metaphor and the extra future change effort called interest.
- [Scrum.org: Product Owner interview questions for 2026](https://www.scrum.org/resources/blog/product-owner-interview-questions-2026) and [Product and Value interview questions](https://www.scrum.org/resources/interview-questions-about-product-and-value) — used to check that the synthesized bank covers value, goals, evidence, backlog decisions, stakeholders, and cross-functional work rather than ceremony trivia.

### Scope and truth boundary

This note teaches official Scrum from the Scrum Guide and labels complementary practices separately. The interview questions, company-context scenarios, case bank, case studies, numerical values, product behaviors, and PRJ226 team design are educational syntheses—not reported company or candidate outcomes.

Repository evidence verifies only broad PRJ226 self-report. Formal Scrum experience, delivery events, detailed capabilities, users, metrics, and outcomes remain unsupported unless the candidate supplies new facts. Preserve that boundary in every spoken answer.
