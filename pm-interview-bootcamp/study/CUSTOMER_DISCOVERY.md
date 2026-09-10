# Customer discovery

[Study home](README.md) · [Product thinking](PRODUCT_THINKING.md) · [Katalon cases](../katalon/CASES.md)

**Start here:** ask about the last real event before asking about a future feature. A request tells you what someone imagines could help; discovery tests the underlying need.

## 1. Discover behavior, not approval

**What is it?** Learning how people try to complete a job, where they struggle, and what they do instead.

**Why a PM cares:** Users may politely like an idea without changing behavior.

**Mental model:** Recent event → actions → friction → workaround → consequence.

**Example:** Instead of “Would you trust an AI test generator?”, ask “Walk me through the last test you generated. What did you change before using it?”

**Common mistake:** Leading questions, selling during an interview, or taking “I would use it” as proof of demand.

**Interview application:** Explain what you want to learn and ask neutral questions that might disprove your hypothesis.

**Check yourself:**

- Which question invites a concrete example?
- How would you discover a workaround?
- What evidence could contradict what the user says?

## 2. A short interview you can actually run

**What is it?** A focused conversation around one uncertainty.

**Why a PM cares:** Broad interviews often produce interesting facts without changing a decision.

**Mental model:** One learning goal → a recent task → artifact → consequences → recap.

**Example questions for a QA engineer:**

1. “What were you trying to finish the last time you used this?”
2. “Can you walk me through what happened?”
3. “What did you check or change, and why?”
4. “What did you do when that did not work?”
5. “What happened as a result?”

Ask permission before viewing project material. Use a non-sensitive example if necessary. Summarize your interpretation and let the person correct it.

**Common mistake:** Asking “Why did you return to the old workflow?” before establishing whether they actually did.

**Interview application:** Choose a sample that helps comparison: unsuccessful first users, successful repeat users and, when relevant, people using alternatives. A few interviews reveal mechanisms, not their population prevalence.

**Check yourself:**

- What decision will this conversation inform?
- Who is missing from your sample?
- How will you distinguish a repeated problem from one person's preference?

## 3. Personas and jobs-to-be-done

**What is it?** A persona groups users by relevant behaviors and constraints. A job describes the progress someone wants in a situation.

**Why a PM cares:** Different users can request the same feature for different reasons.

**Mental model:** “When [situation], I want [progress], so I can [outcome].”

**Example:** “Before a release, I want to tell real defects from unstable tests, so I can recommend whether shipping is safe.” A tester may need diagnostic detail; a release lead may need a defensible risk summary.

**Common mistake:** Making up a persona's age and hobbies while ignoring test skills, permissions, project size or release responsibility.

**Interview application:** Segment by a meaningful constraint, explain why it changes the need, and check the segment against evidence.

**Check yourself:**

- Is your job statement independent of a proposed feature?
- Which behavior makes two users meaningfully different?
- Who uses, approves and pays for the product?

## 4. Write a problem statement

**What is it?** A concise description of the user, situation, obstacle and consequence, supported by evidence.

**Why a PM cares:** It aligns a team around what to solve without committing prematurely to how.

**Mental model:** For [user] during [situation], [obstacle] causes [consequence]. We observed [evidence]; [uncertainty] remains.

**Example — hypothetical:** “QA engineers reviewing generated tests struggle to see whether assertions reflect the requirement. In our sample, they manually compared each assertion with the source requirement. We still need to establish how common this is.”

**Common mistake:** “Users need a better AI agent” embeds a solution and says little about the job.

**Interview application:** Separate observations from your interpretation. Do not invent percentages to make a problem sound important.

**Check yourself:**

- What exactly was observed?
- Which part is still an assumption?
- Can multiple solutions address this statement?

## 5. Map the workflow and handle contradictory evidence

**What is it?** Follow the task across people, tools, handoffs and decisions.

**Why a PM cares:** The real delay may sit outside the feature being discussed.

**Mental model:** Trigger → steps → handoffs → decision → result.

**Example:** Requirements arrive incomplete → tester clarifies → creates tests → reviews → executes → investigates failures. Faster generation may create little value if clarification or diagnosis dominates the work.

If one user wants more automation and another wants more review, compare task risk, project context and experience. Do not average their preferences into a universal requirement.

**Common mistake:** Assuming disagreement means one user is wrong, or treating a feature request as validated because several people repeat it.

**Interview application:** Explain which new comparison would resolve the disagreement. Respectfully challenge a stakeholder: “That may help this segment; I’d first check whether review is the main bottleneck.”

**Check yourself:**

- Where does work wait for another person?
- Could an improvement move the bottleneck elsewhere?
- What would make you change your original problem statement?

## Apply it to your experience

Recall one actual integration/support incident. Explain what the customer requested, what you learned, and your own action. Do not rename ordinary troubleshooting as a product experiment unless you actually ran one.

Use the [evidence ledger](../stories/evidence-ledger.md) only if helpful; no report is required. Detailed TDCX/FPT Software incidents are not available yet.

[Try K-F01 or K-C04](../katalon/CASES.md) · [Next: AI, agents and MCP](AI_AGENTS_MCP.md)
