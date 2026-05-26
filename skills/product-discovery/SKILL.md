---
name: product-discovery
description: Use before any product work — new features, product ideas, or behavior changes. Use before writing PRDs or user stories.
---

# Product Discovery

Help turn product ideas into validated opportunities through structured discovery. Understand the problem deeply before thinking about solutions.

Start by exploring the current product context, then conduct discovery through JTBD mapping, user research, and opportunity assessment. Once discovery is complete, present findings and get approval before moving to PRD.

<HARD-GATE>
Do NOT invoke any PRD-writing skill, write any user story, or take any product-commitment action until you have completed discovery and the user has approved the findings. This applies to EVERY feature regardless of perceived simplicity.
</HARD-GATE>

## Anti-Pattern: "This Is Obvious, We Already Know the Problem"

Every product initiative goes through discovery. A login button, a settings page, a minor UX tweak — all of them. "Obvious" features are where unexamined assumptions cause the most wasted engineering effort. The discovery can be short (a few minutes for truly simple features), but you MUST present findings and get approval.

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Explore current context** — Check existing product docs, analytics, user feedback, recent changes, competitive landscape
2. **Define the desired outcome** — What business or user metric are we trying to move? Frame as an outcome, not an output.
3. **Map Jobs-to-be-Done** — What job is the user hiring this product/feature to do? Functional, emotional, and social dimensions.
4. **Conduct user research** — Interview users following The Mom Test principles. Uncover needs, pain points, and desires — don't validate your existing ideas.
5. **Complete Opportunity Assessment** — Answer all 10 SVPG questions
6. **Validate the problem** — Use lightweight validation techniques before committing to building
7. **Present findings** — Problem statement, evidence, opportunity size, key risks
8. **Save discovery doc** — Write to `docs/product-superpowers/discovery/YYYY-MM-DD-<topic>.md`
9. **User reviews and approves** — Wait for explicit approval before proceeding to PRD

## The Process

### Step 1: Explore Current Context

Before asking the user anything, gather what already exists:
- Review any existing product docs, PRDs, or discovery docs in the project
- Check analytics data (if available): what are users doing? Where do they drop off?
- Review recent user feedback, support tickets, NPS comments
- Check competitive landscape for this problem space
- Understand the current product architecture and technical constraints

### Step 2: Define the Desired Outcome

Reframe the request as an outcome, not an output.

| Instead of (output) | Ask (outcome) |
|---------------------|---------------|
| "Build a dark mode" | "Are users struggling with eye strain or battery life?" |
| "Add a share button" | "Are users trying to collaborate or spread awareness?" |
| "Build a dashboard" | "What decisions do users need to make with this data?" |

Use the format: **"Improve [metric] from [baseline] to [target] by [timeframe]"**

Example: "Increase new user activation rate from 40% to 65% by Q3."

### Step 3: Map Jobs-to-be-Done

For each user segment, identify the Job-to-be-Done:

**Job Statement Format:**
```
When [situation],
I want to [motivation],
so I can [expected outcome].
```

Map the Forces of Progress for each job:

| Force | Question |
|-------|----------|
| **Push** (pain of current state) | What's frustrating about how they do it today? |
| **Pull** (attraction of new solution) | What makes the new way compelling? |
| **Anxiety** (worries about new solution) | What concerns do they have about switching? |
| **Habit** (allegiance to current behavior) | What keeps them using the current approach? |

**Job Mapping** — Break the job into steps:
```
Define → Locate → Prepare → Confirm → Execute → Monitor → Modify → Conclude
```

**JTBD Interview Questions:**
- "Tell me about the last time you [did the activity]?"
- "What was going on in your life that led you to look for a solution?"
- "What did you try before using our product (or a competitor)?"
- "What made you decide to finally switch?"

### Step 4: Conduct User Research (The Mom Test)

Talk to users. Follow Rob Fitzpatrick's principles:

- **Don't pitch your solution.** Ask about their problems and current behavior.
- **Talk about their life, not your idea.** "Tell me about how you currently handle X."
- **Ask about specific past instances, not generic opinions.** "When was the last time...?" not "Would you ever...?"
- **Listen for commitments, not compliments.** "That's interesting" is not validation.
- **Avoid premature zoom-in.** Don't focus on one solution before understanding the broad problem space.

Research methods to consider:
- User interviews (1:1 conversations)
- Contextual inquiry (observe users in their environment)
- Surveys (for quantitative validation)
- Analytics review (what are users actually doing?)
- Support ticket analysis (what are common pain points?)

### Step 5: Opportunity Assessment (SVPG)

Answer all 10 questions:

1. **Exactly what problem will this solve?** (value proposition)
2. **For whom do we solve that problem?** (target market/persona)
3. **How big is the opportunity?** (market size, affected users, revenue potential)
4. **How will we measure success?** (specific metrics and targets)
5. **What alternatives are out there now?** (competitive landscape, substitutes)
6. **Why are we best suited to pursue this?** (our differentiator, unfair advantage)
7. **Why now?** (market timing, urgency, window of opportunity)
8. **How will we get this to market?** (go-to-market strategy, channels)
9. **What factors are critical to success?** (key solution requirements, must-have capabilities)
10. **Given the above, is it worth pursuing?** (go/no-go recommendation)

### Step 6: Validate the Problem

Before committing to building, validate using lightweight techniques:

| Technique | What it is | Best for |
|-----------|------------|----------|
| **Problem interviews** | Talk to potential users about the problem (no solution shown) | Understanding if the problem is real |
| **Landing page test** | Create a page describing the solution, measure interest | Gauging demand before building |
| **Wizard of Oz test** | Simulate a working product manually behind the scenes | Testing value prop without engineering |
| **Concierge MVP** | Manually deliver the service to early customers | Learning what users really need |
| **Smoke test** | "Buy now" button or ad that measures intent | Validating willingness to pay/act |
| **Value Proposition Canvas** | Map customer jobs/pains/gains to your solution | Systematic problem-solution fit check |

### Step 7: Present Findings

Present the discovery summary:

1. **Problem Statement** — One sentence: what problem, for whom, why it matters
2. **Evidence** — What data, interviews, or research supports this is a real problem
3. **Opportunity Size** — How many users affected, revenue impact, strategic importance
4. **Key Risks** — Biggest uncertainties and how to resolve them
5. **Recommendation** — Pursue / Investigate Further / Deprioritize

### Step 8: Save Discovery Document

Write the validated discovery to `docs/product-superpowers/discovery/YYYY-MM-DD-<topic>.md`

Document structure:
```markdown
# [Topic] — Product Discovery

**Date:** YYYY-MM-DD
**Status:** Approved / Needs More Research / Deprioritized

## Problem Statement
...

## Desired Outcome
...

## Jobs-to-be-Done
...

## Research Findings
...

## Opportunity Assessment
...

## Validation Results
...

## Recommendation
...

## Open Questions
...
```

### Step 9: User Review Gate

After saving the discovery doc:

> "Discovery complete and saved to `docs/product-superpowers/discovery/<filename>.md`. Please review the findings and let me know if you approve moving to PRD, need more research, or want to deprioritize."

Wait for the user's response. If they request more research, do it. If they approve, move to PRD. If they deprioritize, archive.

## Key Principles

- **Problem before solution** — Don't think about what to build until you understand what to solve
- **Evidence over intuition** — Every claim should be backed by data, research, or cited examples
- **Outcome over output** — Frame everything as a metric to move, not a feature to ship
- **User voice over internal opinion** — Your opinion matters less than what users actually do and say
- **Lightweight is allowed** — For simple features, discovery can be brief. But it must still be done.

## Red Flags — STOP and Return to Discovery

- Writing PRD before discovery is complete
- Solution-first thinking ("we should build X" without understanding the problem)
- Confirmation bias (only seeking evidence that supports your idea)
- Skipping user research because "we already know"
- Over-relying on one method (only analytics, only surveys, etc.)
- Not including engineers or designers in discovery
- Treating discovery as a phase with a fixed end date (it's continuous)

## Transition to PRD

Once discovery is approved, invoke the **writing-prd** skill to create the Product Requirements Document. Do NOT invoke any other skill.

## Key References

- Marty Cagan, "Inspired" and "Empowered" (SVPG)
- Teresa Torres, "Continuous Discovery Habits"
- Rob Fitzpatrick, "The Mom Test"
- Clayton Christensen, "Competing Against Luck" (JTBD)
- Strategyzer, "Value Proposition Design"
