---
name: prioritization
description: Use when prioritizing or scoring features, user stories, or initiatives against each other.
---

# Prioritization

Score and order product backlog items, feature requests, or strategic initiatives using proven prioritization frameworks. Choose the right framework for the context, apply it systematically, and produce a scored, ordered output with documented rationale.

**Announce at start:** "I'm using the prioritization skill to prioritize [what you're prioritizing]."

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Gather all items to prioritize** — Features, stories, bugs, tech debt, strategic bets
2. **Understand the context** — What decision is being made? What constraints exist?
3. **Choose the right framework** — One or more based on context
4. **Apply the framework** — Score every item with documented rationale
5. **Order and analyze** — Produce an ordered list with insights
6. **Identify quick wins and big bets** — Call out patterns
7. **Present for review** — Get approval before committing

## Choosing the Right Framework

| Framework | Best For | When to Use |
|-----------|----------|-------------|
| **RICE** (recommended) | Feature prioritization, roadmap decisions | You have estimates for reach, confidence, and effort. Need a balanced score. |
| **ICE** | Quick prioritization, growth experiments | You need fast gut-feel scoring. Early-stage, high uncertainty. |
| **MoSCoW** | Release scoping, MVP definition | You need to make hard trade-offs for a specific timebox. |
| **Kano** | Feature discovery, user satisfaction | You need to understand which features are basics vs. delighters. |
| **Value vs. Effort** | Portfolio-level decisions, visual communication | You want a 2x2 visual. Communicating to executives. |
| **Story Mapping** | Release planning, user journey focus | You need to find a natural slicing line across a user journey. |

You can combine frameworks. Example: Use RICE to score, then MoSCoW for the top items against a release deadline.

## RICE Scoring

Developed by Intercom. The most comprehensive framework.

```
RICE Score = (Reach × Impact × Confidence) / Effort
```

### Factor Definitions

**Reach:** How many users or customers will this affect in a given time period?
- Be specific: "5,000 users per month" not "lots"
- For internal tools, count the people who will use it
- For new markets, estimate the addressable users

**Impact:** How much will this move the needle for those users?
- 3 = Massive impact (step-change improvement)
- 2 = High impact (significant improvement)
- 1 = Medium impact (noticeable improvement)
- 0.5 = Low impact (marginal improvement)
- 0.25 = Minimal impact (barely noticeable)

**Confidence:** How sure are you about your reach, impact, and effort estimates?
- 100% = High confidence (backed by data, experiments, or strong evidence)
- 80% = Medium confidence (informed by research, some data)
- 50% = Low confidence (gut feel, limited evidence)
- 20% = Moonshot (wild guess, high uncertainty)

**Effort:** Total resources needed.
- Measure in person-months, person-weeks, or story points
- Include engineering, design, QA, and any other teams
- Be consistent across all items being compared

### Scoring Process

For each item, produce a table:

| Item | Reach | Impact | Confidence | Effort | RICE Score | Notes |
|------|-------|--------|------------|--------|------------|-------|
| Feature A | 5,000 users/mo | 3 (massive) | 80% | 2 person-months | 6,000 | Backed by beta feedback |
| Feature B | 10,000 users/mo | 1 (medium) | 100% | 0.5 person-months | 20,000 | Quick win — high confidence from analytics |

### Red Flags in RICE

- All items scored with 100% confidence (unrealistic)
- Reach is always "all users" (be precise)
- Effort estimates from engineering are missing (PM guessing effort = low confidence)
- Scoring to make a pre-determined answer win (confirmation bias)

## ICE Scoring

Simpler than RICE. Good for rapid, gut-feel prioritization (growth experiments, early-stage).

```
ICE Score = (Impact + Confidence + Ease) / 3
```

Each factor scored 1-10:
- **Impact**: How much will this move the needle? (1 = minimal, 10 = massive)
- **Confidence**: How sure are you? (1 = wild guess, 10 = backed by data)
- **Ease**: How easy is it to build? (1 = extremely hard, 10 = trivial)

ICE is fast but less rigorous than RICE. Use for initial filtering, then apply RICE to top candidates for deeper analysis.

## MoSCoW Method

For release scope decisions. Categorize every item into one of four buckets:

- **M**ust have — Critical, non-negotiable for this release. Without these, the release has no value.
  - Guard: "If we shipped without this, would we delay the release?" If no, it's not Must Have.
- **S**hould have — Important but not critical. Can be worked around if not ready.
  - Guard: "If we shipped without this, would users be frustrated but still use the product?" If yes, Should Have.
- **C**ould have — Nice to have. Low cost of delay.
  - Guard: "Would most users not even notice if this was missing?" If yes, Could Have.
- **W**on't have — Explicitly out of scope for this release.
  - Guard: This is NOT "we'll do it later." This is "we made a conscious decision not to do this now."

**MoSCoW Rules:**
- Must Have items should be ≤ 60% of total effort
- If everything is Must Have, nothing is
- Won't Have is not a failure — it's a strategic choice

## Kano Model

Classify features by how they affect customer satisfaction:

| Category | Description | User Reaction | Strategy |
|----------|-------------|---------------|----------|
| **Basic (Must-be)** | Expected. Absence = dissatisfaction. | "Of course it does that." | Must include. Don't overinvest. |
| **Performance** | More is better. Linear satisfaction. | "The faster the better." | Invest to differentiate. |
| **Excitement (Delighters)** | Unexpected. Absence = neutral. | "Wow, I didn't know I needed that!" | Innovate here for competitive edge. |
| **Indifferent** | Users don't care either way. | "Meh." | Avoid building. |
| **Reverse** | Some users like, others dislike. | "I hate this." (some users) | Understand segments. |

**Using Kano for Prioritization:**
1. List all potential features
2. Classify each into one category based on user research
3. Prioritize: Basic (must have) → Performance (invest) → Excitement (differentiate)
4. Cut Indifferent and segment Reverse features

## Value vs. Effort Matrix

Plot items on a 2x2 grid:

```
High Value  │  Quick Wins    │  Big Bets
            │  (Do first)    │  (Plan carefully)
            │                │
Low Value   │  Fill-ins      │  Time Sinks
            │  (If time)     │  (Don't do)
            └────────────────┴─────────────
            Low Effort          High Effort
```

**Action per quadrant:**
- **Quick Wins (High Value, Low Effort):** Do these immediately. Highest ROI.
- **Big Bets (High Value, High Effort):** Plan and sequence. Break into smaller deliverables.
- **Fill-ins (Low Value, Low Effort):** Do if there's spare capacity. Don't prioritize over Quick Wins or Big Bets.
- **Time Sinks (Low Value, High Effort):** Don't do. Explicitly deprioritize.

## Story Mapping

For release and sprint planning. From Jeff Patton's methodology.

**Process:**
1. List user activities left-to-right in chronological order (the backbone)
2. Under each activity, list user stories in priority order (top = critical, bottom = nice-to-have)
3. Draw a slicing line across the map to identify what goes in each release
4. Each horizontal slice is a coherent release

```
Activities:  Browse     →   Search    →   Compare   →   Purchase  →   Track
             ─────────────────────────────────────────────────────────────
             Product grid   Search bar   Side-by-side  Checkout     Order status
             Filter by cat  Autocomplete  Price history  Payment      Notifications
             ───────────── Slicing Line (MVP) ─────────────────────────
             Sort by price  Filters       Reviews       Save cart    Returns
             Ratings        Recent        Wishlist      Gift wrap    Reorder
```

## Presenting Results

After scoring, present:

1. **Framework used and why**
2. **Top items with scores and rationale**
3. **Bottom items that should be deprioritized**
4. **Quick wins identified**
5. **Big bets requiring further planning**
6. **Any ties or judgment calls to discuss**

Save to: `docs/product-superpowers/prioritization/YYYY-MM-DD-<context>.md`

## Key Principles

- **Score with evidence, not emotion** — Every score should have a rationale. "Gut feel" is valid only if labeled as low confidence.
- **Effort must come from engineering** — PM should not estimate effort alone.
- **Confidence matters** — A high-scoring item with low confidence is riskier than a medium-scoring item with high confidence.
- **Reprioritize continuously** — New information should change the order.
- **Make trade-offs explicit** — "If we do X, we don't do Y (or we delay Z)."
- **Don't over-prioritize** — If everything is P1, nothing is. 30-40% of items should be P1 or Must Have at most.

## Red Flags

- Scoring items to get a pre-determined answer ("I already know what we should build")
- All items scored with the same confidence (not thinking critically)
- Effort estimates from PM alone (need engineering input)
- No items below the line (everything can't be top priority)
- Using one framework for everything (RICE doesn't work for release scoping)

## Key References

- RICE framework by Sean McBride (Intercom)
- ICE framework by Sean Ellis (GrowthHackers)
- MoSCoW method by Dai Clegg
- Kano model by Noriaki Kano
- "User Story Mapping" by Jeff Patton
