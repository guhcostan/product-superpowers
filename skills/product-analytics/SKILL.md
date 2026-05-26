---
name: product-analytics
description: Use when defining product metrics, designing experiments, analyzing feature adoption, or setting up measurement frameworks. Covers North Star, AARRR, feature adoption, and A/B testing.
---

# Product Analytics

Define metrics that matter. Design experiments that produce valid insights. Measure feature adoption and business impact. Make data-informed product decisions.

**Announce at start:** "I'm using the product-analytics skill to [purpose]."

## Skill Type

**Flexible** — Adapt frameworks to your analytics tooling and data maturity. Core principles are non-negotiable.

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Define the North Star metric** — What single metric captures your product's core value?
2. **Map the user lifecycle (AARRR)** — Where are the biggest opportunities?
3. **Define feature adoption framework** — How will you measure if features succeed?
4. **Design experiments (A/B tests)** — If testing, follow the full process
5. **Set up measurement before building** — Instrument before development
6. **Define kill criteria** — When to deprecate features that don't work

## Step 1: Define the North Star Metric

The North Star is the single metric that best captures the core value your product delivers to customers. It is the leading indicator of long-term business success.

### Characteristics of a Good North Star

- **Expresses value to users** — Not just business revenue
- **Leading indicator** — Predicts future outcomes, doesn't just report past ones
- **Actionable** — Teams can influence it directly
- **Measurable** — Quantifiable and trackable
- **Simple to communicate** — Everyone in the company understands it

### Examples

| Company | North Star Metric | Why |
|---------|-------------------|-----|
| Spotify | Time spent listening | Core value = music discovery and enjoyment |
| Airbnb | Nights booked | Core value = travel accommodations |
| Slack | Messages sent per team | Core value = team communication |
| WhatsApp | Messages sent | Core value = communication |
| Figma | Weekly active editors | Core value = collaborative design |
| Stripe | Payment volume processed | Core value = payment infrastructure |
| Netflix | Hours streamed | Core value = entertainment |
| Notion | Weekly active blocks created | Core value = knowledge work |

### How to Define Yours

1. **What is the core action that delivers value to users?**
   - When a user does [X], they received value from your product
   - Example: "When a user sends a message in Slack, they communicated with their team"

2. **How frequently must users take this action to get ongoing value?**
   - Is it daily? Weekly? Monthly?
   - Example: "Teams need to send messages daily to replace email"

3. **Can you measure this consistently?**
   - Is the data available? Is it reliable? Is it hard to game?
   - Example: "Messages sent is automatically tracked and hard to artificially inflate"

### North Star Inputs

Break the North Star into input metrics that teams can influence:

```
North Star: Weekly Active Editors
  ↑
  ├── New user activation rate → Onboarding team
  ├── Editor retention rate → Core experience team
  ├── Collaboration invites sent → Growth team
  └── Time to first edit → Performance team
```

## Step 2: Map the User Lifecycle (AARRR)

AARRR Pirate Metrics (coined by Dave McClure, 500 Startups) track users through 5 stages:

### The AARRR Funnel

| Stage | Question | Key Metrics |
|-------|----------|-------------|
| **Acquisition** | How do users find you? | Traffic sources, conversion by channel, CAC, SEO rankings |
| **Activation** | Do they have a great first experience? | Sign-up rate, onboarding completion, first key action taken, time to "aha moment" |
| **Retention** | Do they come back? | DAU/MAU ratio, churn rate, N-day retention (D1, D7, D30), session frequency |
| **Referral** | Do they tell others? | NPS, viral coefficient (k-factor), referral sign-ups, social shares |
| **Revenue** | How do you make money? | ARPU, LTV, MRR/ARR, conversion to paid, expansion revenue, CAC payback period |

### Using AARRR for Diagnosis

1. **Find the bottleneck**: Which stage has the biggest drop-off?
2. **Form a hypothesis**: Why are users dropping off here?
3. **Design an intervention**: What change could improve this?
4. **Measure the impact**: Did the metric improve?

### Common Patterns

| Pattern | Likely Issue | Focus Area |
|---------|-------------|-----------|
| High acquisition, low activation | Onboarding is broken, product doesn't match expectations | Activation |
| High activation, low retention | Core product value isn't sticky enough | Retention |
| High retention, low referral | Product is good but not remarkable | Referral/Delight |
| High everything, low revenue | Monetization strategy needs work | Revenue/Pricing |

### Beyond AARRR

- **Awareness** — Added before Acquisition (AAARRR). How do potential users learn you exist?
- **Resurrection** — Win-back campaigns for churned users
- **Expansion** — Upsell, cross-sell, seat expansion within existing accounts

## Step 3: Feature Adoption Measurement

### Feature Adoption Funnel

```
Exposed → Engaged → Activated → Retained → Power User
```

| Stage | Definition | Metric |
|-------|-----------|--------|
| **Exposed** | Saw the feature exists | % of target users who viewed the feature |
| **Engaged** | Interacted with it once | % who clicked/opened/tried the feature |
| **Activated** | Got value from first use | % who completed the key action |
| **Retained** | Came back and used it again | % who used it again within N days |
| **Power User** | Uses it frequently as core workflow | % who use it at least X times per week |

### Key Feature Metrics

| Metric | Definition | Target |
|--------|-----------|--------|
| **Adoption Rate** | % of target users who use the feature | Set based on feature type (core vs. nice-to-have) |
| **Time to Adopt** | How long after exposure until first use | Should be < 7 days for promoted features |
| **Feature Retention** | % of first-time users who use it again | > 40% at D7 is healthy |
| **Feature Stickiness** | DAU/MAU for the specific feature | > 20% is sticky |
| **Cannibalization** | Does new feature reduce usage of existing features? | Monitor for unintended displacement |
| **Support Impact** | Tickets related to this feature | Compare to baseline |

### Segmenting Feature Adoption

Always segment adopters by:
- **User persona** (does this feature resonate with the intended audience?)
- **Account age** (do new users adopt differently than existing users?)
- **Plan/tier** (free vs. paid adoption patterns)
- **Region/language** (any geo-specific issues?)
- **Device/platform** (mobile vs. desktop differences)

## Step 4: Design A/B Tests

### The A/B Testing Process

1. **Form a hypothesis**: 
   - Format: "If we change [X] to [Y], we will see [Z impact] because [rationale]"
   - Example: "If we move the signup button above the fold, we will increase signup rate by 10% because users don't scroll to find the current CTA."

2. **Define primary metric**:
   - ONE metric that determines winner/loser
   - Must be measurable and sensitive enough to detect the expected effect

3. **Define guardrail metrics**:
   - Metrics that must NOT degrade
   - Example: "Revenue per user must not decrease by more than 2%"

4. **Calculate sample size**:
   - Based on: baseline conversion rate, minimum detectable effect, desired statistical power (typically 80%), significance level (typically 95%)
   - Use a sample size calculator

5. **Randomize and run**:
   - Random split between control (A) and treatment (B)
   - Run for the pre-calculated duration (typically 1-4 weeks)
   - DO NOT PEEK at results early (increases false positive rate)

6. **Analyze results**:
   - Check statistical significance (p < 0.05)
   - Check practical significance (is the effect big enough to matter?)
   - Check guardrail metrics
   - Segment results (did effect vary by user type?)

7. **Decide**:
   - Ship the winner
   - Iterate on the design if inconclusive
   - Discard if negative or neutral

### A/B Testing Pitfalls

| Pitfall | Why It's a Problem | Prevention |
|---------|-------------------|-----------|
| **Peeking** | Stopping early when results look significant inflates false positive rate | Pre-commit to duration, don't look until it's over |
| **Too many variants** | Requires much larger sample size per variant | Test 2-3 variants max |
| **Too many metrics** | Multiple comparisons increase false positives (p-hacking) | Pre-register one primary metric |
| **Novelty effect** | Users initially engage with anything new | Run tests at least 2-4 weeks |
| **Small sample** | Underpowered test can't detect real effects | Calculate required sample size upfront |
| **Ignoring segments** | Averages can hide opposite effects in different groups | Always segment results |
| **No guardrail metrics** | You might optimize for one metric while destroying another | Always define guardrails |
| **Causation vs. correlation** | Metric movement doesn't prove your change caused it | Use randomized controlled experiments |

### When NOT to A/B Test

- Sample size too small for statistical significance
- Change is a bug fix or infrastructure improvement (just ship it)
- Change is a compliance/legal requirement
- Feature is for a very small user segment
- The cost of building the experiment exceeds the value of the learning
- You can't measure the outcome reliably

## Step 5: Instrument Before Building

### Tracking Plan Template

For every feature, define tracking before development:

```markdown
# Tracking Plan — [Feature Name]

## Success Metrics
| Metric | Definition | Event(s) | Target |
|--------|-----------|----------|--------|
| Adoption rate | % of users who use feature within 30 days | `feature_engaged` / total users | > 30% |
| Feature retention | % who use again within 7 days of first use | `feature_engaged` with 7-day gap | > 40% |

## Events to Track
| Event Name | When Fired | Properties | Example Value |
|------------|-----------|------------|---------------|
| `onboarding_started` | User begins onboarding flow | `source`, `plan_tier` | `source: "invite_email"` |
| `onboarding_step_completed` | User completes a step | `step_name`, `step_number`, `time_spent_s` | `step_name: "team_setup"` |
| `onboarding_completed` | User finishes onboarding | `total_time_s`, `steps_completed`, `skipped` | `total_time_s: 180` |

## User Properties
| Property | Type | Example |
|----------|------|---------|
| `account_created_at` | Date | `2026-05-20T10:30:00Z` |
| `plan_tier` | String | `pro` |
| `team_size` | Integer | `12` |
```

### Before Launch, Verify

- [ ] All events fire correctly in staging
- [ ] Event properties are populated correctly
- [ ] Data flows to your analytics tool (Mixpanel, Amplitude, PostHog, etc.)
- [ ] Dashboard is built and populated with test data
- [ ] Key metrics are queryable and match expectations

## Step 6: Kill Criteria

Define in advance when to deprecate a feature:

| Timeline | Metric | Threshold | Action |
|----------|--------|-----------|--------|
| 30 days | Adoption rate | < 20% of target users | Investigate. Is it discoverability or value? |
| 60 days | Feature retention | < 25% of first-time users return | Consider redesign or deprecation |
| 90 days | Adoption rate | < 10% of target users | Deprecate |
| Ongoing | Support tickets | > 20% of total tickets | Evaluate cost vs. benefit |

## Key Principles

- **Metrics should drive decisions** — If a metric doesn't change what you do, stop tracking it.
- **Measure outcomes, not outputs** — "30% of users adopted" not "we shipped 3 features."
- **Instrument before building** — You can't retroactively add tracking to shipped code.
- **Segment everything** — Averages lie. Always look at segments.
- **One primary metric per experiment** — Multiple metrics = multiple comparison problem.
- **Define kill criteria before launch** — Don't let zombie features accumulate.
- **Qualitative + quantitative** — Data tells you WHAT. User research tells you WHY.
- **North Star is a compass, not a report card** — It guides decisions, not just measures past performance.

## Common Pitfalls

- Tracking vanity metrics (page views, downloads) instead of actionable metrics (activation, retention)
- No defined success metrics before shipping ("we'll figure out if it worked later")
- Instrumentation as an afterthought ("we'll add tracking after launch")
- A/B testing everything (some things should just ship)
- Ignoring practical significance (statistically significant but too small to matter)
- Over-optimizing for one metric at the expense of others
- Not segmenting results (hiding opposite effects in different user groups)
- Keeping features alive because removing them is awkward (kill criteria exist for this)

## Key References

- "Lean Analytics" by Alistair Croll and Benjamin Yoskovitz
- "Hacking Growth" by Sean Ellis and Morgan Brown
- Amplitude's "The North Star Playbook"
- Dave McClure's AARRR framework (500 Startups)
- Reforge's experimentation and growth programs
