---
name: product-analytics
description: Use when defining product metrics, designing experiments, analyzing feature adoption, or setting up measurement frameworks.
---

# Product Analytics

Define metrics that matter. Design experiments that produce valid insights. Measure feature adoption and business impact. Make data-informed product decisions.

**Announce at start:** "I'm using the product-analytics skill to [purpose]."

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Define the North Star metric** — What single metric captures your product's core value?
2. **Map the user lifecycle (AARRR)** — Where are the biggest opportunities?
3. **Define feature adoption framework** — How will you measure if features succeed?
4. **Design experiments (A/B tests)** — If testing, follow the full process
5. **Set up measurement before building** — Instrument before development
6. **Define kill criteria** — When to deprecate features that don't work

## Step 1: Define the North Star Metric

The single metric that captures the core value your product delivers — a leading indicator of long-term success that expresses value to users, not just revenue.

| Company | North Star Metric | Core Value |
|---------|-------------------|------------|
| Spotify | Time spent listening | Music discovery and enjoyment |
| Airbnb | Nights booked | Travel accommodations |
| Slack | Messages sent per team | Team communication |
| Figma | Weekly active editors | Collaborative design |
| Stripe | Payment volume processed | Payment infrastructure |

**How to define yours:** Identify the core action that delivers value. Determine how frequently users must take it for ongoing value. Ensure it's measurable and hard to game.

**Input metrics** (what teams influence to move the North Star): e.g., activation rate → onboarding team, retention rate → core experience team, collaboration invites → growth team, time-to-value → performance team.

## Step 2: Map the User Lifecycle (AARRR)

| Stage | Question | Key Metrics |
|-------|----------|-------------|
| **Acquisition** | How do users find you? | Traffic sources, conversion by channel, CAC |
| **Activation** | Do they have a great first experience? | Sign-up rate, onboarding completion, time to "aha moment" |
| **Retention** | Do they come back? | DAU/MAU, churn rate, D1/D7/D30 retention |
| **Referral** | Do they tell others? | NPS, viral coefficient, referral sign-ups |
| **Revenue** | How do you make money? | ARPU, LTV, MRR/ARR, conversion to paid |

**Diagnosis:** Find the bottleneck stage → form a hypothesis → design an intervention → measure impact.

| Pattern | Likely Issue | Focus |
|---------|-------------|-------|
| High acquisition, low activation | Onboarding broken or expectations mismatch | Activation |
| High activation, low retention | Core value not sticky enough | Retention |
| High retention, low referral | Product good but not remarkable | Delight |
| High everything, low revenue | Monetization strategy needs work | Pricing |

## Step 3: Feature Adoption Measurement

**Adoption funnel:** Exposed → Engaged → Activated → Retained → Power User

| Stage | Definition | Metric |
|-------|-----------|--------|
| **Exposed** | Saw the feature exists | % of target users who viewed it |
| **Engaged** | Interacted once | % who clicked/opened/tried |
| **Activated** | Got value from first use | % who completed the key action |
| **Retained** | Came back | % who used it again within N days |
| **Power User** | Core workflow habit | % using at least X times/week |

| Metric | Definition | Target |
|--------|-----------|--------|
| **Adoption Rate** | % of target users who use the feature | Depends on feature type |
| **Time to Adopt** | How long after exposure until first use | < 7 days for promoted features |
| **Feature Retention** | % of first-time users who return | > 40% at D7 is healthy |
| **Feature Stickiness** | DAU/MAU for the feature | > 20% is sticky |
| **Cannibalization** | Does new feature reduce usage of existing ones? | Monitor for displacement |

Always segment adopters by persona, account age, plan/tier, region, and device/platform.

## Step 4: Design A/B Tests

**Process:**
1. **Form a hypothesis:** "If we change [X] to [Y], we will see [Z impact] because [rationale]"
2. **Define primary metric:** ONE metric that determines winner/loser
3. **Define guardrail metrics:** Metrics that must NOT degrade (e.g., revenue per user ≤ 2% drop)
4. **Calculate sample size:** Based on baseline rate, minimum detectable effect, 80% power, 95% significance
5. **Randomize and run:** Random split, pre-calculated duration (1–4 weeks). Do NOT peek early.
6. **Analyze:** Check statistical significance (p < 0.05), practical significance, guardrails, segment results
7. **Decide:** Ship winner, iterate if inconclusive, discard if negative

**Pitfalls:**

| Pitfall | Prevention |
|---------|-----------|
| **Peeking** (stopping early) | Pre-commit to duration, don't look until over |
| **Too many variants** | Test 2–3 max |
| **Too many metrics** (p-hacking) | Pre-register one primary metric |
| **Novelty effect** | Run at least 2–4 weeks |
| **Small sample** | Calculate required size upfront |
| **Ignoring segments** | Always segment results |
| **No guardrail metrics** | Always define what must not degrade |

**When NOT to A/B test:** Sample too small for significance, bug fix/infra change (just ship), compliance requirement, very small user segment, experiment cost exceeds learning value, can't measure outcome reliably.

## Step 5: Instrument Before Building

**Before launch, define for every feature:**

| Artifact | Contents |
|----------|----------|
| **Success metrics** | Metric, definition, events, target (e.g., adoption rate = `feature_engaged` / total users > 30%) |
| **Events to track** | Event name, when fired, properties, example values |
| **User properties** | Property name, type, example (e.g., `plan_tier`: String, `team_size`: Integer) |

**Before launch, verify:** all events fire correctly in staging, event properties populated, data flows to your analytics tool, dashboard is built with test data, key metrics are queryable.

## Step 6: Kill Criteria

| Timeline | Metric | Threshold | Action |
|----------|--------|-----------|--------|
| 30 days | Adoption rate | < 20% of target users | Investigate discoverability or value |
| 60 days | Feature retention | < 25% return | Consider redesign or deprecation |
| 90 days | Adoption rate | < 10% of target users | Deprecate |
| Ongoing | Support tickets | > 20% of total | Evaluate cost vs. benefit |

## Key Principles

- **Metrics should drive decisions** — If a metric doesn't change what you do, stop tracking it.
- **Measure outcomes, not outputs** — "30% adopted" not "we shipped 3 features."
- **Instrument before building** — You can't retroactively add tracking.
- **Segment everything** — Averages lie. Always look at segments.
- **One primary metric per experiment** — Multiple metrics = multiple comparison problem.
- **Define kill criteria before launch** — Don't let zombie features accumulate.
- **Qualitative + quantitative** — Data tells you WHAT. User research tells you WHY.
- **North Star is a compass** — Guide decisions, not just measure past performance.

## Common Mistakes

- Tracking vanity metrics (page views, downloads) instead of actionable metrics (activation, retention)
- No defined success metrics before shipping; instrumentation as an afterthought
- A/B testing everything (some things should just ship)
- Ignoring practical significance (statistically significant but too small to matter)
- Over-optimizing for one metric at expense of others; not segmenting results
- Keeping features alive because removing them is awkward (use kill criteria)

## Key References

- "Lean Analytics" by Alistair Croll and Benjamin Yoskovitz
- "Hacking Growth" by Sean Ellis and Morgan Brown
- Amplitude's "The North Star Playbook"
- Dave McClure's AARRR framework (500 Startups)
- Reforge's experimentation and growth programs
