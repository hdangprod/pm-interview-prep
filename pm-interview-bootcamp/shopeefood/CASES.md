# ShopeeFood practice cases

[Home](../README.md) · [Marketplace notes](../study/MARKETPLACE_FOR_PM.md) · [Order-decline reflex](../study/MARKETPLACE_FOR_PM.md#diagnose-an-order-decline) · [Gemini prompt](../gemini/COACH_PROMPT.md)

Pick one prompt and answer aloud before reading a follow-up. All scenarios and numbers are hypothetical. Request additional data from Gemini and ask it to keep that data consistent. No full solutions or tracking required.

## Foundation

### S-F01 — Follow an order

Explain how a buyer, merchant and driver contribute to one completed order. Where can the journey break?

### S-F02 — More visits, fewer orders

Traffic increases, but placed orders decrease. How would you investigate?

### S-F03 — Conversion decline

Checkout conversion falls after a product change. What would you check first, and why?

### S-F04 — Longer ETA

Buyers see longer delivery estimates. How would you locate the source of the change?

### S-F05 — Merchant acceptance

Merchant order acceptance drops in one area. How would you decide whether the cause is product, operations or incentives?

## Intermediate

### S-D01 — Orders decline

Completed orders in one city fell 15% last week versus the previous week. The business team wants to launch a discount tomorrow. How would you decide what to do?

<details>
<summary>Optional interviewer follow-up</summary>

The decline is concentrated in weekday lunch hours. What is your next data request, and which decision will it inform?

</details>

### S-I01 — Cancellations rise

Order cancellations increase while placed orders stay steady. How would you diagnose the problem and choose a response?

<details>
<summary>Optional interviewer follow-up</summary>

Different stakeholders use different cancellation-rate denominators. How would you reconcile the evidence?

</details>

### S-C02 — Lunch shortage

A lunch promotion increases demand while ETA and cancellations worsen. How would you identify the constraint and respond?

<details>
<summary>Optional interviewer follow-up</summary>

Operations says more drivers will solve it. Merchants report long pickup queues. You have a limited incentive budget.

</details>

### S-C03 — Volume improves, economics worsen

A promotion raises completed orders but lowers contribution. Would you continue, modify or stop it?

<details>
<summary>Optional interviewer follow-up</summary>

Repeat use looks higher among promotion users. What must you know before crediting the promotion?

</details>

### S-I02 — Cities diverge

One city grows while another declines during the same national campaign. How would you explain the difference and decide whether to change the campaign?

## Pressure test

### S-C04 — Low merchant orders, long buyer ETA

Merchants complain about low order volume while buyers complain about long ETA. How can both be true, and what would you investigate first?

<details>
<summary>Optional interviewer follow-up</summary>

The citywide average driver count has not changed. Does that alter your reasoning?

</details>

### S-C05 — Experiment spillovers

A driver incentive improves delivery time in the test area while nearby areas worsen. How would you interpret the experiment and decide about expansion?

### S-P01 — Limited resources

You can fund only one initiative this month: improve merchant preparation estimates, increase lunch driver incentives, or reduce checkout friction. How would you choose?

<details>
<summary>Optional interviewer follow-up</summary>

Your preferred option takes longer than expected. What would you do this week?

</details>

### S-P02 — Merchant economics

A program raises merchant order volume, but participating merchants say they earn less and want to leave. What would you investigate and recommend?

### S-P03 — Buyer promise versus capacity

Business wants a larger delivery radius to improve selection. Operations warns it will hurt peak-time reliability. Recommend a way forward.

<details>
<summary>Optional interviewer follow-up</summary>

Your recommendation helps buyers but lowers driver earnings per online hour. Would you still proceed?

</details>

## Mock interview

Paste after the [Gemini coach prompt](../gemini/COACH_PROMPT.md):

> Run a ShopeeFood business assessment mock. Start with one ambiguous business problem. Release consistent hypothetical data as I request it. Ask me for a recommendation, then probe metrics, buyer/merchant/driver effects, economics, operational constraints and execution. Change one important constraint. Ask one question at a time, avoid solutions before my attempt, and give overall feedback when I say “end mock.”

This is practice design; the actual assessment duration and individual/group format are unconfirmed. If group work is confirmed, ask Gemini to simulate a colleague disagreeing and practice incorporating the strongest point.

[Previous case queue](case-bank.md) · [Company research](research.md) · [Quick review](../QUICK_REVIEW.md)
