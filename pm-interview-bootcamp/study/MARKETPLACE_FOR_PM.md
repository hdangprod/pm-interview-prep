# Food-delivery marketplace thinking

[Study home](README.md) · [ShopeeFood cases](../shopeefood/CASES.md) · [Quick review](../QUICK_REVIEW.md)

**Start here:** a completed order requires a buyer who wants it, a merchant who can prepare it, and a driver who can deliver it. The platform coordinates them within time, price and capacity constraints.

Shortcuts: [Order-decline diagnosis](#diagnose-an-order-decline) · [Numbers](#5-orders-gmv-and-economics) · [Causal chains](#6-first--and-second-order-effects)

All numerical examples are fictional. No internal ShopeeFood rates, costs or matching policies are assumed.

## 1. Liquidity is local and time-sensitive

**What is it?** Matching demand with suitable selection and fulfillment capacity at an acceptable price and time.

**Why a PM cares:** Plenty of drivers citywide does not help if none can reach a lunch area quickly.

**Mental model:** Right meal + preparation capacity + nearby delivery capacity + right moment.

**Example:** Orders rise around offices at noon while drivers and merchants are busy elsewhere. More traffic can worsen the mismatch.

**Common mistake:** Counting registered drivers as immediately available supply.

**Interview application:** Ask where, when and for whom the system is constrained.

**Check yourself:**

- Why could nearby neighborhoods have different ETAs?
- What makes a driver available for this order?

## 2. Buyer: demand depends on the promised experience

**What is it?** The path from opening the service to receiving a meal and deciding whether to return.

**Why a PM cares:** Traffic creates opportunities; selection, total price and reliability determine whether they become durable demand.

**Mental model:** Visit → find meal → evaluate price/ETA → order → receive → return.

**Example:** Traffic stays steady but delivery fees rise in a segment. Conversion may fall. Alternatively, checkout could be broken; the metric alone cannot tell you.

- **Traffic:** Visits or eligible sessions; define which.
- **Conversion:** A defined action divided by eligible opportunities.
- **Frequency:** Orders per buyer in a period.
- **Retention:** A defined cohort returning to order later.
- **Selection/menu quality:** Suitable available meals, clear items, accurate prices and stock.
- **Promotions:** Change value; may subsidize orders that would happen anyway.
- **ETA/cancellation:** Set and deliver a promise; failures can affect future use.

**Common mistake:** Treating conversion, frequency and retention as interchangeable.

**Interview application:** Locate the funnel break, compare segments, and consider price, selection, reliability and product faults.

**Check yourself:**

- Can conversion rise while orders fall?
- Can a promotion lift frequency without lasting retention?

## 3. Merchant: selection must be fulfillable

**What is it?** The merchant turns orders into prepared meals.

**Why a PM cares:** Appearing online does not prove a restaurant can fulfill extra demand.

**Mental model:** Available menu → accept → prepare → hand off.

**Example:** A promotion exceeds kitchen capacity. Preparation slows, drivers queue, food waits, and buyers cancel.

- **Availability:** Open status and item stock.
- **Acceptance:** Can and will the merchant fulfill the order?
- **Preparation time:** Time and variability until pickup readiness.
- **Menu quality:** Accurate options reduce confusion and rework.
- **Economics:** Receipts after discounts and fees must cover food, packaging, labor and other costs.
- **Capacity:** Kitchen throughput is limited; extra orders can displace other business.

**Common mistake:** Forcing acceptance up without solving stock or overload problems.

**Interview application:** Separate information problems from operational bottlenecks. Ask who owns the change.

**Check yourself:**

- When might fewer accepted orders improve outcomes?
- Can a merchant receive more orders and earn less?

## 4. Driver: productive capacity, not just people

**What is it?** Drivers spend time accepting, reaching pickup, waiting, delivering and finding the next job.

**Why a PM cares:** Longer cycles reduce orders per available hour even with unchanged driver counts.

**Mental model:** Effective capacity depends on available time and the full order cycle.

**Example:** Kitchen wait rises from 5 to 15 minutes. The same drivers spend less time completing deliveries.

- **Supply:** Available drivers in the relevant location/time.
- **Acceptance:** Depends on earnings, distance, waits and alternatives.
- **Utilization:** Productive/busy time relative to a stated available-time definition.
- **Idle time:** May mean weak demand, poor matching or useful buffer capacity.
- **Pickup wait/distance:** Consume time and operating costs.
- **Earnings:** Consider earnings per online hour and expenses, not just per order.
- **Incentives:** Can attract or move supply, but cost money and shift shortages.

**Common mistake:** Maximizing utilization at all times, leaving no buffer for a surge.

**Interview application:** Explain how an intervention changes the driver's cycle and willingness to accept.

**Check yourself:**

- Why could higher pay per order still mean lower hourly earnings?
- Could incentives in one district harm another?

## 5. Orders, GMV and economics

**What is it?** Measures of activity, transaction value and what the platform retains.

**Why a PM cares:** Volume can hide losses or fragile service.

**Mental model:**

- Completed orders = placed orders × completion rate.
- With consistent counting: placed orders = eligible sessions × orders per session.
- If at most one order is attributed to each session, orders per session also equals session conversion.
- GMV ≈ relevant order count × average order value, with consistent status/refund definitions.
- Platform revenue may include commissions and fees; specify what counts.
- Contribution = defined revenue minus included variable costs. It excludes some fixed costs; it is not company profit.

**Example:** 1,000 placed orders × 90% completion = 900 completed orders. At a defined average food value of 100,000 VND, completed-order GMV is 90 million VND. This does not establish platform revenue.

A separate hypothetical order yields 25,000 VND revenue and incurs 27,000 VND included variable costs: contribution is −2,000 VND. More volume at that margin worsens near-term contribution unless something else changes.

**Common mistake:** Treating GMV as revenue, omitting the promotion payer, or calling every promoted order incremental.

**Interview application:** Ask about incentives, refunds, payment/delivery/support costs and the counterfactual. Do not invent commission rates.

**Check yourself:**

- Which definitions must match before multiplying?
- What could justify temporarily negative contribution?
- How would you distinguish new demand from subsidized existing demand?

## 6. First- and second-order effects

**What is it?** First-order effects are direct changes; second-order effects follow as the system and people respond.

**Why a PM cares:** A feature can improve its target metric and worsen overall service.

**Mental model:** Intervention → response → bottleneck/behavior change → later outcomes.

**Possible chains to investigate:**

- Promotion → demand rises → kitchen/driver shortage → ETA rises → cancellations → weaker future trust.
- Faster preparation → less pickup wait → more deliveries per driver hour → better capacity and possibly shorter ETA.
- Larger radius → more selection → longer trips → lower capacity → service deterioration.
- Higher incentive → supply moves to target area → nearby area loses drivers → shortage shifts.

These are hypotheses, not inevitable outcomes. Check spare capacity, response size, geography and time.

**Common mistake:** Stopping at “orders increase,” or assuming every side must improve equally.

**Interview application:** Name the beneficiary, who bears the cost, whether the trade-off is acceptable, and how to observe harm.

**Check yourself:**

- Where could the benefit reverse?
- Which stakeholder behavior could change?
- What happens after an incentive ends?

## Diagnose an order decline

**What changed → when → where → which segment → which mechanism?**

1. **Define and verify:** Placed or completed orders? Which comparison period? Check events, reporting and known outages.
2. **Locate:** Traffic, ordering, acceptance, matching, completion or repeat behavior? Request rates and counts.
3. **Segment:** City, zone, time, new/returning buyers, merchant type, distance, app version or promotion exposure.
4. **Explain:** Rank a few mechanisms using timing/evidence; request the next data that could change the ranking.
5. **Act:** Choose a feasible product or operations intervention, owner and limited scope.
6. **Evaluate:** Measure the outcome plus reliability/economic guardrails; state when to change course.

Do not collect every metric before acting. A major outage may need mitigation while diagnosis continues. Matching and preparation can overlap; do not add overlapping times twice.

**Common mistake:** “Orders fell; add discounts.” Establish whether demand or fulfillment is constrained.

**Check yourself:**

- Could placed orders stay steady while completed orders fall?
- What comparison separates seasonality from a new problem?

## Experiment without ignoring shared capacity

**What is it?** A comparison helping separate intervention effects from other changes.

**Why a PM cares:** Buyers in different groups may share drivers and merchants.

**Mental model:** Intervention → exposed users/resources → spillovers → measured difference.

**Example:** A promotion fills kitchens and slows delivery for the control group too. A user-level comparison may misstate full-rollout impact.

Consider geographic clusters or alternating time periods when appropriate. Balance comparable areas/times and account for movement, seasonality and carryover. No design removes every issue.

**Common mistake:** Claiming causality from one city's before/after result.

**Interview application:** Name the main confounder and one practical mitigation.

**Check yourself:**

- Could the control group be affected?
- Does the test show short-term activity or lasting behavior?

## Connect to ShopeeFood

The [research](../shopeefood/research.md) grounds the three-sided model in program and operational sources. Internal metrics, costs and exact BAC format remain unknown.

[Practice S-D01](../shopeefood/CASES.md#intermediate) · [Gemini prompt](../gemini/COACH_PROMPT.md)
