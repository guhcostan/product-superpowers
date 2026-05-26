---
name: writing-prd
description: Use when you have an approved discovery document and need to write a Product Requirements Document before implementation begins.
---

# Writing a Product Requirements Document (PRD)

Write a PRD based on approved discovery findings. The PRD translates problem understanding into clear product requirements that engineering, design, and stakeholders can align on.

**Default format: Amazon PR/FAQ (Working Backwards).** This format forces clarity on customer benefit and differentiation before any solution details.

**Announce at start:** "I'm using the writing-prd skill to create the Product Requirements Document."

<HARD-GATE>
Do NOT invoke this skill unless discovery is complete and approved. If discovery has not been done, invoke product-discovery first.
</HARD-GATE>

**Save PRDs to:** `docs/product-superpowers/prds/YYYY-MM-DD-<feature-name>.md`

## When to Use Which Format

| Format | Best For | Origin |
|--------|----------|--------|
| **Amazon PR/FAQ** (recommended) | New features, new products, major initiatives | Amazon |
| **SVPG Product Brief** | Lightweight, outcome-focused, rapid iteration | Marty Cagan/SVPG |
| **Shreyas Doshi Framework** | Strategic decisions, trade-off clarity, decision logs | Shreyas Doshi |

Ask the user which format they prefer, defaulting to Amazon PR/FAQ.

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Review discovery doc** — Ensure findings are current and complete
2. **Write the Press Release** — Customer-facing, 1-page announcement of the finished product
3. **Write the FAQ — External** — Questions customers would ask
4. **Write the FAQ — Internal** — Questions from stakeholders, engineering, leadership
5. **Add Success Metrics** — How will we know if this succeeded?
6. **Add Assumptions, Constraints, and Dependencies**
7. **Add Open Questions** — What still needs investigation
8. **Spec self-review** — Scan for placeholders, contradictions, ambiguity, scope creep
9. **User reviews and approves** — Wait for explicit approval before proceeding to user stories

## The Amazon PR/FAQ Process

### Part 1: The Press Release

Write a 1-page press release announcing the finished product. Write it as if the product exists today.

**Rules:**
- Customer-focused language. No jargon. No internal project names.
- One page maximum. If it takes more, you don't understand the product well enough.
- Write in past/present tense as if it already launched.
- Include a customer quote (fictional, but realistic).

**Structure:**

```
[Headline] — One sentence that captures the customer benefit

[Subhead] — 2-3 sentences expanding on who this is for and the primary benefit

[Summary Paragraph] — The what, who, where, when, and why in plain language

[Problem Paragraph] — The customer problem today. Why current solutions fall short.

[Solution Paragraph] — How this product solves the problem. Key capabilities.

[Customer Quote] — A fictional quote from a real user persona describing the impact

[How to Get Started] — How customers access/use this. Call to action.
```

### Part 2: FAQ — External (Customer Questions)

Anticipate and answer questions customers will have. Write from their perspective.

**Common questions to address:**
- What exactly does this do?
- How is it different from [competitor/alternative]?
- How much does it cost?
- Is my data secure?
- How do I get started?
- What if I need help?
- Does it work with [existing tool/ecosystem]?
- What happens to my existing [workflow/data]?
- Is there a free trial?
- When will it be available?

### Part 3: FAQ — Internal (Stakeholder Questions)

Anticipate and answer questions from engineering, design, leadership, sales, support, legal.

**Engineering/Design:**
- What are the technical constraints or dependencies?
- What existing systems/services does this integrate with?
- Are there new infrastructure or third-party costs?
- What's the expected scale (users, data volume, requests)?
- What are the non-functional requirements (performance, security, accessibility)?

**Leadership:**
- How does this align with company strategy?
- What's the business impact (revenue, retention, acquisition)?
- What's the estimated investment (team size, timeline)?
- What are the key risks?
- Why now? What's the cost of delay?

**Sales/Marketing:**
- How do we position this against competitors?
- What's the target customer profile?
- What's the pricing model?
- What sales enablement is needed?

**Support:**
- What's the expected support burden?
- What documentation/training is needed?
- What are common failure modes?

**Legal/Compliance:**
- Are there regulatory requirements?
- Data residency, privacy, GDPR considerations?
- Terms of service or policy changes needed?

### Part 4: Success Metrics

Define how you will measure success. Use the format:

| Metric | Baseline | Target | Timeframe | Measurement Method |
|--------|----------|--------|-----------|-------------------|
| North Star impact | Current value | Target value | Time period | Tool/method |
| Adoption rate | Current % | Target % | Time period | Tool/method |
| Retention | Current % | Target % | Time period | Tool/method |

Include:
- **Primary metric**: The ONE metric that determines if this was a success
- **Secondary metrics**: Guardrail metrics that must not degrade
- **Counter metrics**: Things that might inadvertently get worse

### Part 5: Assumptions, Constraints, Dependencies

**Assumptions** — Things you expect to be true but haven't verified:
- "Users have stable internet connectivity"
- "Customer support team can handle the increased volume"
- "The underlying API will remain available at current latency"

**Constraints** — Limitations on the implementation:
- "Must work on mobile web (not just native)"
- "Cannot increase page load time by more than 200ms"
- "Budget limited to $50k for third-party services"

**Dependencies** — External elements the product relies on:
- "Requires the authentication service migration to be complete"
- "Depends on the design system v2 being available"
- "Third-party payment API must support our regions"

### Part 6: Open Questions

Items that need further investigation before or during development:
- "What is the acceptable latency for the recommendation engine?"
- "Do we need to support offline mode for this feature?"
- "How will GDPR right-to-deletion work for user-generated content?"

## Spec Self-Review

After writing the complete PRD, review it systematically:

1. **Placeholder scan**: Any "TBD", "TODO", incomplete sections, or vague requirements? Fix them.
2. **Internal consistency**: Do the press release claims match the FAQ answers? Does the solution address the problem stated?
3. **Scope check**: Is this focused enough for a single release, or does it need decomposition into phases?
4. **Ambiguity check**: Could any requirement be interpreted two different ways? If so, pick one and make it explicit.
5. **Metric check**: Is every success metric measurable? Do you know the baseline?

Fix any issues inline. No need to re-review — just fix and move on.

## SVPG Product Brief (Alternative Format)

If the user prefers a lighter format:

```markdown
# [Feature Name] — Product Brief

## Problem
What problem are we solving? For whom?

## Current State
How do users solve this today? What are the alternatives?

## Proposed Solution
High-level description of what we'll build.

## Success Criteria
How will we know if we solved the problem?

## Key Risks
What could go wrong? How will we mitigate?

## Scope
What's in? What's explicitly out?
```

## Shreyas Doshi Framework (Alternative Format)

For strategic products requiring decision clarity:

```markdown
# [Feature Name] — Product Requirements

## Problem Statement
...

## User Insights
What we know about our users that informs this decision.

## Success Metrics
...

## Key Decisions
The 3-5 most important decisions that will shape this product.

## Trade-offs
What we're explicitly choosing NOT to do, and why.
```

## User Review Gate

After the PRD self-review passes:

> "PRD written and saved to `docs/product-superpowers/prds/<filename>.md`. Please review it and let me know if you want changes before we break this into user stories."

Wait for the user's response. If they request changes, make them and re-run the self-review. Only proceed once the user approves.

## Transition to User Stories

Once the PRD is approved, invoke the **user-story-writing** skill to break the PRD into user stories with INVEST criteria and acceptance criteria. Do NOT invoke any other skill.

## Key Principles

- **Start with the customer, not the solution** — The press release forces this
- **Write for clarity, not completeness** — A shorter, clearer PRD beats an exhaustive, confusing one
- **Metrics before features** — If you can't measure success, don't build it
- **Scope is your shield** — Being explicit about what's OUT is as important as what's IN
- **PRD is a living document** — It will evolve. Capture decisions as they're made.
- **Show, don't just tell** — Include sketches, diagrams, references to make things concrete

## Common Mistakes

- Writing a PRD before discovery is done
- Over-specifying the solution (telling engineering how to implement)
- No success metrics (building without knowing what success looks like)
- No out-of-scope section (inviting scope creep)
- Treating the PRD as final and unchangeable (waterfall thinking)
- Writing in isolation (PRDs should involve engineering and design input)
- Features without use cases (every feature needs a "who does what and why")
- Ignoring non-functional requirements (accessibility, i18n, performance, security)

## Key References

- "Working Backwards" by Colin Bryar and Bill Carr (Amazon PR/FAQ)
- Marty Cagan, "Inspired" (SVPG Product Brief)
- Shreyas Doshi's PM frameworks
- ProductPlan PRD templates and glossary
