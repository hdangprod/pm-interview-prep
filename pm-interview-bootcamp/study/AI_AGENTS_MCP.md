# AI, agents and MCP for a PM

[Study home](README.md) · [Katalon cases](../katalon/CASES.md) · [Quick review](../QUICK_REVIEW.md)

**Start here:** AI can interpret messy input. Tools let software act. An agent chooses next steps. MCP helps connect the application to tools and context. None guarantees a useful or correct result.

Read in three short visits: **1–2 foundations**, **3–4 agents and MCP**, **5–7 judgment**. New to MCP? [Jump to the worked example](#4-mcp-connects-the-parts).

## 1. AI, ML and LLMs

**What is it?** AI is the broad field of systems performing tasks associated with intelligence. Machine learning (ML) learns patterns from data. A large language model (LLM) is an ML model trained to predict and generate token sequences, often used for language and code.

**Why a PM cares:** Pick capabilities for a job. You do not need an LLM for every prediction or rule.

**Mental model:** Task → required capability → simplest suitable approach.

**Example:** Food-delivery ETA can use predictive ML plus operational inputs. Explaining a messy QA failure report may benefit from an LLM. Checking whether a required field is empty needs a rule.

**Common mistake:** “It uses AI, so it understands the business and is correct.”

**Interview application:** Explain the uncertainty and what the system must reliably produce.

**Check yourself:**

- Why might ETA prediction and failure explanation use different methods?
- What task would you keep deterministic?

## 2. Tokens, context, prompting and grounding

### Tokens and context

**What is it?** Tokens are chunks of text or other encoded input. The context window is the bounded material a model can use in an interaction; it is not unlimited recall.

**Why a PM cares:** Relevant input competes for space and adds processing cost. Important facts can be omitted, buried or outdated.

**Mental model:** Context is the working desk. More paper does not guarantee better decisions.

**Example:** Test generation needs the requirement, project conventions, useful examples and environment constraints. The entire repository may add noise.

**Common mistake:** Assuming a long conversation means every detail will be used reliably.

**Interview application:** Identify the minimum relevant context and how to detect missing information.

**Check yourself:**

- What must the model know for this specific test?
- What should happen when the requirement is missing?

### Prompting

**What is it?** Instructions and examples communicating the goal, constraints, relevant input and desired output.

**Why a PM cares:** Clear boundaries reduce ambiguity, but prompts are not permission enforcement.

**Mental model:** Brief the task → supply evidence → set boundaries → check output.

**Example:** “Draft tests for this requirement using this project's conventions. Mark missing information. Do not invent expected behavior.”

**Common mistake:** Improving prompt wording before discovering that the feature solves the wrong problem.

**Interview application:** Explain what you would change in the input and how you would compare results.

**Check yourself:**

- What ambiguity does your prompt remove?
- What must be enforced outside the prompt?

### Hallucination and RAG

**What is it?** A hallucination is plausible output unsupported by facts or supplied evidence. Retrieval-augmented generation (RAG) retrieves relevant material and provides it as context before generation.

**Why a PM cares:** A fluent answer can invent an API or requirement. Grounding can help, but retrieval can miss or return stale material.

**Mental model:** Retrieve evidence → provide it → answer against it → verify.

**Example:** Retrieve current testing conventions before drafting a test. Check that the cited convention supports the generated choice.

**Common mistake:** Treating RAG as retraining the model or a guarantee against hallucination.

**Interview application:** Separate retrieval quality from answer quality. Handle missing and conflicting evidence explicitly.

**Check yourself:**

- Could correct retrieval still produce a wrong answer?
- How would you handle outdated project documentation?

RAG's retrieval-and-context role is described in [Google's RAG overview](https://cloud.google.com/vertex-ai/generative-ai/docs/rag-engine/rag-overview). Examples here are hypothetical.

## 3. Tools, agents and memory

### Tool calling

**What is it?** The model proposes a named operation with arguments; the application validates and executes the allowed call, then returns a result.

**Why a PM cares:** Actions can change real systems. The model saying “done” is not proof of execution.

**Mental model:** Proposed action → policy/argument check → execution → observed result.

**Example:** Read a test result by ID. Updating that test needs the right project, permissions and conflict handling.

**Common mistake:** Assuming a valid tool name means safe arguments, or blindly retrying a write after a timeout.

**Interview application:** Describe failure handling and how the user knows whether an action completed.

**Check yourself:**

- What happens with the right tool but wrong project ID?
- How would you avoid duplicate changes after a retry?

### Agent, chatbot and workflow

**What is it?** A chatbot is a conversational interface; it can be backed by an agent. A deterministic workflow follows predefined steps. An LLM-based agent chooses steps/tools in response to observations.

**Why a PM cares:** Flexible action selection brings extra cost and failure opportunities.

**Mental model:** Goal → inspect context → choose action → call tool → observe → continue, ask, or stop.

**Example:** A fixed process always runs a regression suite and sends its report. An agent investigating an unfamiliar failure may choose whether to inspect logs, data or recent changes.

**Common mistake:** Calling every multi-step script an agent or assuming chat cannot take actions.

**Interview application:** Justify why variable next steps are necessary. Bound retries, runtime and scope.

**Check yourself:**

- Where does this system actually choose its next step?
- Could a known sequence solve the problem more reliably?
- What stops an unproductive loop?

The distinction between predefined workflows and adaptive agents follows [Anthropic's agent design guidance](https://www.anthropic.com/engineering/building-effective-agents). Product labels vary.

### Memory versus working context

**What is it?** Memory is information stored across interactions. It must be selected and brought into context to affect a later model call.

**Why a PM cares:** Stored information may be wrong, stale or inappropriate for another project.

**Mental model:** Storage → relevant retrieval → current context → decision.

**Example:** Save an approved convention for Project A without silently applying it to Project B. Let users inspect, correct or remove preferences.

**Common mistake:** Remembering every prior model statement as a verified fact.

**Interview application:** Identify what deserves persistence, whose information it is and when it expires.

**Check yourself:**

- What should be remembered or forgotten?
- How does the user correct a bad memory?

## 4. MCP connects the parts

**What is it?** Model Context Protocol standardizes exchanging tools and context between an AI application and other systems.

**Why a PM cares:** A common interface can reduce custom integration work and bring capabilities into existing workflows.

**Mental model:**

- **Host:** The AI application the user interacts with.
- **Client:** Its connection component.
- **Server:** A program exposing tools, resources or prompt templates.
- **Underlying system:** The project, service or data those capabilities access.

The server may run locally or remotely. It need not contain an LLM. An agent can use tools without MCP. [Official architecture](https://modelcontextprotocol.io/docs/learn/architecture)

### A concrete testing example

Imagine asking a connected assistant: “Explain why test T-42 failed.”

1. The host has an MCP client connected to the testing server.
2. The application discovers available tools and their inputs.
3. It requests the relevant result through an allowed tool.
4. The server retrieves the result from the testing system.
5. The application uses that evidence to explain the failure or request context.

Asking to update the test adds a write decision with separate permission, verification and recovery needs.

Katalon documents external assistants accessing testing artifacts through its [True Platform MCP server](https://docs.katalon.com/katalon-platform/testops-mcp-server). T-42 and this sequence are teaching examples, not a specific tool name or Dang's work.

**Common mistake:** “MCP is the agent's brain,” “MCP replaces every API,” or “MCP makes actions safe.” Adapters may still call APIs; policies must control access and actions.

**Interview application:** Explain one user benefit, trace one read/write boundary, and name a failure. Skip transport internals unless asked.

**Check yourself:**

- Which part reasons, and which exposes capabilities?
- Why does connecting a server not justify unrestricted access?
- What is the product value beyond adding an acronym?

## 5. Control autonomy according to risk

**What is it?** Autonomy is how much action the system takes without intervention. Human-in-the-loop means meaningful involvement at selected decisions.

**Why a PM cares:** Both mistakes and excessive approvals can make a feature unusable.

**Mental model:** Error likelihood × impact × exposure, considered alongside verifiability and reversibility.

- **Permissions:** Limit projects, data, tools and operations to the task.
- **Reversibility:** Can a change be undone, and does undo remove its consequences? Exposed data cannot simply be “unseen.”
- **Approval:** Show the exact action and affected scope when risk or uncertainty warrants it.
- **Observability:** Record inputs, tool calls, results and errors so actions can be checked. Protect sensitive log content.
- **Recovery:** Stop, report partial progress, and offer a safe next action on failure.

**Example:** Automatically inspect authorized logs; draft a change; require approval for risky shared configuration updates. Choose boundaries from the environment. Even read-only access can expose sensitive data.

**Common mistake:** “Humans approve everything, so it is safe.” People may rubber-stamp confusing requests. Retrieved documents may contain malicious instructions; treat them as data, not new authority.

**Interview application:** Name an action to automate, an action to gate, and evidence needed to expand autonomy.

**Check yourself:**

- Can the reviewer make an informed decision?
- What happens if the user is unavailable?
- What risk remains after rollback?

These are design choices, not universal Katalon permission defaults.

## 6. Evaluate the user's job

**What is it?** Check whether outputs/actions are correct, safe enough for their purpose, and useful.

**Why a PM cares:** Better model scores may not improve adoption or outcomes.

**Mental model:** Representative tasks → current-workflow baseline → correctness checks → user outcome → guarded rollout.

**Example:** Compare total time to an accepted, meaningful test, including edits, review and retries. Inspect whether assertions catch relevant defects and avoid false alarms. Include ambiguous requirements and missing context.

Separate:

- **Output quality:** Correctness, grounding and suitability.
- **Action quality:** Right tool, arguments, permissions and completion.
- **User value:** Task success, effort, trust and eligible repeat use.
- **Operational cost:** Cost and latency per successful task.

**Common mistake:** Equating tests that execute with tests that protect the product. Edits are not automatically errors; an error-free run does not prove useful coverage.

**Interview application:** Propose a small evaluation set and comparison. Explain costly failures, a stop criterion and why the measures reflect the job. Monitor after launch.

**Check yourself:**

- What failure would an average score hide?
- What outcome can improve while retention stays unchanged?
- How would you avoid measuring only successful users?

## 7. Cost, latency, quality — and saying no

**What is it?** Quality competes with response time and resources. More context, tool calls and retries can add cost and delay.

**Why a PM cares:** Good output arriving late or needing excessive review can lose to the existing workflow.

**Mental model:** Successful-job cost includes generation, tools, retries and human effort.

**Example:** Use a rule for a known file format; reserve flexible reasoning for ambiguous diagnosis. Compare the whole workflow rather than one model call.

**When not to use AI:** Exact rules suffice; errors cannot be checked affordably; available context cannot support the task; or there is no meaningful user benefit.

**When not to use an agent:** Steps are stable; a single model call suffices; tool failures cannot be recovered safely; or autonomy adds little.

**Common mistake:** Defaulting to a stronger model or more agents.

**Interview application:** “I’d use an agent only if choosing the next step is part of the problem.”

**Check yourself:**

- What is the simplest credible baseline?
- Where does autonomy create measurable value?
- What would make you remove AI from the feature?

## Practice

Explain MCP in 45 seconds. Then take [K-P02](../katalon/CASES.md#pressure-test) or say “Teach me AI agents from where I am” using the [Gemini prompt](../gemini/COACH_PROMPT.md).

[Next: testing](TESTING_FOR_PM.md) · [Company research](../katalon/research.md)

Primary references checked September 10, 2026. Learn the mental model, not release trivia.
