---
name: pm-feedback-synthesis
description: Use when you have raw user feedback from multiple sources (interviews, surveys, tickets, reviews) and need to extract themes, patterns, and actionable insights
---

# PM Feedback Synthesis

Transform raw, unstructured user feedback from multiple sources into structured, actionable product insights. Cluster themes, extract evidence, and link findings to opportunities on your Opportunity Solution Tree.

**Core principle:** PMs have data goldmines but no time to mine them. This skill turns scattered feedback into a single source of truth.

**Announce at start:** "I'm using the pm-feedback-synthesis skill to synthesize user feedback."

## When to Use

- You have interview transcripts, survey responses, support tickets, or reviews to process
- You need to identify patterns across multiple feedback sources
- You're preparing for roadmap or prioritization decisions
- You want to update your OST with fresh evidence
- Stakeholders are asking "what are users saying?"

## The Process

### Step 1: Gather Sources

List all feedback sources available. Common sources:

| Source | Typical Format | What to Extract |
|--------|---------------|-----------------|
| User interviews | Transcripts or notes | Pain points, desires, JTBD, direct quotes |
| Support tickets | Ticket export | Recurring issues, friction points, feature requests |
| App store reviews | Review text + rating | Satisfaction drivers, churn signals, competitive mentions |
| NPS surveys | Scores + open comments | Detractor reasons, promoter praise |
| Sales call notes | CRM notes | Objections, competitive comparisons, buying triggers |
| Community/social | Reddit, Slack, Discord | Unfiltered opinions, workarounds, wishlists |
| Analytics drop-offs | Funnel data | Where users struggle (quantitative, needs qualitative pairing) |

### Step 2: Ingest and Cluster

For each source, extract and cluster:

1. **Extract meaningful statements** — Ignore generic praise/complaints. Focus on specific observations: "I couldn't find the export button" not "the UI is bad"

2. **Tag each statement** with:
   - **Theme**: Onboarding, Performance, Collaboration, Pricing, etc.
   - **Sentiment**: Pain point, Desire, Praise, Confusion, Workaround
   - **Frequency**: How many users mentioned this?
   - **Persona/segment**: Which user type?

3. **Cluster related statements** — Group statements within each theme that point to the same underlying need

### Step 3: Produce Structured Output

```markdown
# Feedback Synthesis — [Date]

## Top Themes (by frequency and impact)

### Theme 1: [Name] (N mentions, X% of users)
**What users are saying:**
- "[Direct quote]" — User persona, source
- "[Direct quote]" — User persona, source

**Root cause:** [What's actually broken or missing?]
**Opportunity:** [What job is the user trying to do?]
**Link to OST:** [Which opportunity on the tree does this connect to?]

### Theme 2: [Name]
...

## Emerging Signals (low volume but interesting)
- [Signal] — only 2-3 mentions but suggests a new pattern

## What Changed Since Last Synthesis
- [Theme X] mentions increased 3x since last month
- [Theme Y] was top-3 last time, now barely mentioned (likely fixed)

## Recommendations
1. [Actionable recommendation tied to a theme]
2. [Actionable recommendation]
3. [Question for further investigation]
```

### Step 4: Connect to Product Process

Route insights to the right skill:
- **New opportunities** → Add to `continuous-discovery` OST
- **Validation needed** → Feed into `product-discovery` interviews
- **Clear feature request** → Evaluate in `prioritization`
- **Bug/support issue** → Route to engineering queue
- **Competitive signal** → Feed into `competitive-analysis`

## When to Run This

- **Weekly**: Light pass — what's new in support tickets and NPS?
- **Monthly**: Deep synthesis — all sources, full theme clustering
- **Post-launch**: 7-day and 30-day feedback pulse
- **Pre-roadmap**: Comprehensive synthesis to inform prioritization

## Common Mistakes

**Mixing sources without weighting**: A power user's complaint ≠ every user's experience. Always note frequency and segment.

**Confirmation bias**: Only seeing themes that support your existing beliefs. Read the full dataset before forming conclusions.

**Over-aggregating**: "Users want better UX" is useless. "5 of 12 interviewees couldn't find the export function because it's hidden in a dropdown" is actionable.

**Synthesis without action**: Insights that don't connect to product decisions (OST update, roadmap change, interview topic) are wasted effort.

**Treating signals as certainties**: "3 users mentioned X" is a signal to investigate, not a mandate to build. Distinguish between evidence strength levels.

## Red Flags

**Never:**
- Synthesize without linking to sources ("users want X" — which users? where? when?)
- Present frequency without denominator ("15 users complained" — out of how many?)
- Ignore feedback that contradicts your roadmap
- Skip the "what changed" comparison from last synthesis
- Let insights sit in a doc — route them to the right skill

## Integration

**Feeds into:**
- `continuous-discovery` — New opportunities for the OST
- `product-discovery` — Hypotheses to validate
- `prioritization` — Evidence for scoring decisions
- `competitive-analysis` — Competitive signals from user mentions

**Fed by:**
- `product-discovery` — Interview transcripts to synthesize
- `launch-planning` — Post-launch feedback collection

## Key References

- Teresa Torres, "Continuous Discovery Habits" (connecting feedback to OSTs)
- "The Mom Test" by Rob Fitzpatrick (distinguishing signal from noise)
- Dovetail, Productboard, and similar research repositories
