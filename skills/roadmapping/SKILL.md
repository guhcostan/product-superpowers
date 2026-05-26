---
name: roadmapping
description: Use when creating or updating a product roadmap, defining OKRs, or communicating product direction to stakeholders.
---

# Roadmapping

Create and maintain outcome-based product roadmaps using Now/Next/Later format. Define OKRs that connect work to business outcomes.

**Announce at start:** "I'm using the roadmapping skill to [create/update] the product roadmap."

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Define product vision and strategic themes** — What direction are we heading?
2. **Define OKRs** — Objectives with 3-5 Key Results each
3. **Map initiatives to outcomes** — What work drives which outcomes?
4. **Position in Now/Next/Later** — Time-horizon buckets with confidence levels
5. **Identify dependencies** — What must happen before what?
6. **Define communication plan** — Who needs to know what, when?
7. **Define review cadence** — How often does this get updated?
8. **Save and present** — Document for sharing

## Step 1: Define Product Vision and Strategic Themes

### Product Vision

The aspirational future state you're working toward. Long-term, inspirational, stable.

**Format:**
```
[Product name] helps [target user] achieve [key benefit] by [unique approach].
```

**Examples:**
- Airbnb: "Belong anywhere."
- Slack: "Make work life simpler, more pleasant, and more productive."
- Stripe: "Increase the GDP of the internet."

### Strategic Themes

3-5 broad areas of investment that support the vision. Themes persist across multiple quarters.

| Theme | What it means | Why it matters |
|-------|--------------|----------------|
| User Activation | Help new users reach their first "aha moment" faster | Activation is the biggest lever for retention |
| Collaboration | Make it effortless for teams to work together | Team accounts have 3x higher LTV |
| Platform Reliability | Improve uptime, performance, and error handling | Trust is eroding with current 99.5% uptime |

## Step 2: Define OKRs

### Objective

A qualitative, inspirational goal. "Where do we want to go?"

- Written as a single sentence
- Aspirational but achievable
- Time-bound (typically quarterly)

**Examples:**
- "Become the easiest-to-use project management tool for small teams"
- "Make our API the preferred integration platform for e-commerce"
- "Create a product that users love to tell their friends about"

### Key Results

3-5 quantitative, measurable outcomes that show progress toward the Objective.

**Format:**
```
[Improve/Move/Change] [metric] from [baseline] to [target] by [timeframe]
```

**Examples:**
- "Increase new user activation rate from 40% to 65% by end of Q3"
- "Reduce median time-to-first-project from 12 minutes to 3 minutes"
- "Achieve NPS of 50+ (currently 32) by end of Q4"
- "Grow weekly active teams from 500 to 1,200 by end of Q3"

### OKR Best Practices

- KRs must be outcomes, not outputs ("reduce churn to 2%" not "ship retention emails")
- 3-5 KRs per Objective (more dilutes focus)
- 60-70% achievement is the sweet spot (100% means they were too easy)
- Separate committed OKRs (must deliver) from aspirational OKRs (stretch goals)
- Every team's OKRs should connect to company-level OKRs

### Alternatives

- **North Star Metric** — Single metric that captures core value. Use as a complement to OKRs.
- **KPIs** — Broader performance indicators for ongoing health monitoring.

## Step 3: Map Initiatives to Outcomes

For each initiative in your roadmap, answer: which outcome does this drive?

| Initiative | Drives which KR(s)? | Confidence |
|------------|---------------------|------------|
| Redesigned onboarding flow | KR1: Activation rate | High (backed by user testing) |
| Team invite improvements | KR4: Weekly active teams | Medium |
| Performance optimization | KR3: NPS improvement | Low (indirect relationship) |

Initiatives that don't connect to any outcome should be questioned. Every significant piece of work should trace back to a strategic goal.

## Step 4: Now/Next/Later

Use relative time buckets instead of fixed dates:

### Now
- Actively working on or starting this month/quarter
- High confidence in scope and outcome
- Features are specified, designs are done
- Dependencies are resolved

### Next
- Up next in the queue (next quarter or two)
- Medium confidence — scope is clear but details may shift
- Some discovery may still be needed
- Priority order matters

### Later
- Future initiatives (2-4 quarters out or beyond)
- Low confidence — broad strokes, subject to change
- Discovery not yet done
- Order is rough; things will shift

### Example Roadmap

| Now | Next | Later |
|-----|------|-------|
| Redesigned onboarding flow | Team collaboration features | Mobile app |
| Performance optimization (P95 < 2s) | Advanced analytics dashboard | AI-powered recommendations |
| SSO integration (Enterprise) | Public API v2 | Internationalization |
| Bug fix sprint (top 20 issues) | Dark mode | Marketplace / integrations |

### Confidence Levels

For each item, indicate confidence:
- **High**: We know what to build and why. Validated with users.
- **Medium**: General direction is clear. Some unknowns remain.
- **Low**: Hypothesis stage. Needs discovery and validation.

External roadmaps (customer-facing) should only include High and some Medium confidence items.

## Step 5: Identify Dependencies

Map what must happen before what:

```
Initiative A (onboarding redesign) → depends on → Design system v2
Initiative B (team features) → depends on → Initiative A (enables team invites)
Initiative C (API v2) → no dependencies → can start anytime
```

Flag:
- **Blocking dependencies**: Can't start without this being done
- **Enabling dependencies**: Can start, but full value requires this
- **Cross-team dependencies**: Requires another team's work

## Step 6: Communication Plan

Different stakeholders need different views:

| Stakeholder | Needs | Format | Cadence |
|-------------|-------|--------|---------|
| **Executive team** | Strategic alignment, resource decisions, key risks | Executive summary + Now/Next/Later | Monthly |
| **Engineering** | What's coming, dependency resolution, technical context | Full roadmap + sprint plans | Bi-weekly |
| **Design** | Upcoming design needs, user insights | Thematic view + discovery queue | Weekly |
| **Sales/Marketing** | Launch timing, competitive positioning, customer commitments | External roadmap (conservative) | Monthly |
| **Customer Success** | Feature changes, training needs, support impact | Feature-focused view | Per release |
| **Customers** | What's coming, why, when (roughly) | Public roadmap (high confidence only) | Quarterly |

## Step 7: Review Cadence

A roadmap is a living document. Define how often it gets reviewed:

- **Weekly**: PM review — any blockers? New information?
- **Monthly**: Team review — adjust priorities, update confidence levels
- **Quarterly**: Strategic review — major reprioritization, new OKRs
- **On-demand**: When a significant event changes priorities (competitor launch, market shift, major customer win/loss)

## Document Format

Save to: `docs/product-superpowers/roadmaps/YYYY-QN-roadmap.md`

```markdown
# Product Roadmap — [Product Name] [Time Period]

**Last Updated:** YYYY-MM-DD
**Vision:** [One sentence]
**Status:** Draft / In Review / Approved

## Strategic Themes
| Theme | Meaning | Importance |
|-------|---------|------------|
| ... | ... | ... |

## OKRs
**Objective 1:** [Qualitative goal]
- KR1: [Metric] from [baseline] to [target] by [timeframe]
- KR2: ...
- KR3: ...

## Roadmap
| Now (Q1 2026) | Next (Q2-Q3) | Later (Q4+) |
|---------------|--------------|-------------|
| Initiative A (High confidence) | Initiative D (Medium) | Initiative G (Low) |
| Initiative B (High confidence) | Initiative E (Medium) | Initiative H (Low) |
| Initiative C (Medium confidence) | Initiative F (Low) | Initiative I (Low) |

## Dependencies
...

## Risks and Mitigations
...

## Review Cadence
...
```

## Key Principles

- **Outcome over output** — The roadmap says WHAT we want to achieve, not exactly what we'll build
- **Confidence over precision** — "High confidence Q2" is better than "April 15" when you're guessing
- **Now/Next/Later over dates** — Avoid false precision. Use relative buckets.
- **Transparent uncertainty** — Be explicit about what you don't know
- **Living document** — Update at least monthly. A stale roadmap is worse than no roadmap.
- **Connect everything to outcomes** — If an initiative doesn't drive a KR, ask why it's on the roadmap

## Common Mistakes

- **Feature-based roadmaps** — Listing features with dates ("Login page by March 15"). Outcome-based is better.
- **False precision** — Committing to dates 9 months out with low confidence
- **Everything is "Now"** — If everything is a priority, nothing is
- **Roadmap as a promise** — It's a directional plan, not a contract
- **No stakeholder differentiation** — Showing the same detailed view to executives and engineers
- **Stale roadmaps** — Not updated for 6+ months but still referenced
- **Pet features** — Items on the roadmap because someone important asked, not because they drive outcomes

## Key References

- "Product Roadmaps Relaunched" by C. Todd Lombardo et al.
- "Outcomes Over Output" by Josh Seiden
- "Measure What Matters" by John Doerr (OKRs)
- "Inspired" by Marty Cagan (roadmapping chapter)
- Jeff Patton, "User Story Mapping" (slicing roadmaps)
