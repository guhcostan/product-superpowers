---
name: continuous-discovery
description: Use when setting up or improving a continuous product discovery practice with weekly customer interviews.
---

# Continuous Discovery

Establish and maintain a continuous product discovery practice. Based on Teresa Torres' framework from "Continuous Discovery Habits" and Product Talk. Discovery is not a phase — it's ongoing.

**Announce at start:** "I'm using the continuous-discovery skill to [purpose]."

## Core Principles

1. **Start with a clear outcome** — Focus on business outcomes, not feature outputs
2. **Interview weekly** — Minimum one customer interview per week, every week. Non-negotiable.
3. **Opportunity Solution Trees** — Visualize the path from outcome to experiment
4. **Assumption testing** — Identify and test the riskiest assumptions before building
5. **Product trio** — PM, designer, and engineer all participate in discovery

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Define your discovery outcome** — What metric are we trying to move?
2. **Set up interview cadence** — Weekly interviews, structured process
3. **Build the Opportunity Solution Tree** — Map outcome → opportunities → solutions → experiments
4. **Identify and test assumptions** — For each solution, what must be true?
5. **Set up the product trio** — Who participates, how, when?
6. **Define the learning loop** — How do insights flow back into product decisions?
7. **Save and maintain** — Document the OST, keep it current

## Step 1: Define Your Discovery Outcome

Discovery is focused by a clear business outcome you're trying to drive.

### Outcome vs. Output

| Output (what you build) | Outcome (what changes) |
|------------------------|------------------------|
| "Build a new onboarding flow" | "Increase new user activation rate from 40% to 65%" |
| "Add a sharing feature" | "Increase weekly active teams from 500 to 1,200" |
| "Redesign the dashboard" | "Reduce time-to-first-insight from 12 min to 3 min" |

### Choosing Your Outcome

- **Leading indicator** of business success (not a lagging revenue metric)
- **Within your team's influence** (you can affect it with product changes)
- **Measurable** (you can track it consistently)
- **Has room for improvement** (not already optimized)

Examples of good discovery outcomes:
- "Increase new user activation rate"
- "Reduce churn rate for small teams"
- "Increase feature adoption among enterprise accounts"
- "Reduce time to complete core workflow"

## Step 2: Set Up Interview Cadence

### The Weekly Interview Commitment

- **Minimum**: 1 customer interview per week
- **Who conducts them**: Rotate among the product trio (PM, designer, engineer)
- **Duration**: 30-45 minutes each
- **Recruitment**: Automate. Use in-app prompts, email outreach, sales introductions, user testing platforms

### Interview Structure (Discovery Interview, NOT Usability Test)

Follow "The Mom Test" principles:

**Opening:**
- "Thanks for talking with us. We're just trying to learn — there are no wrong answers."
- "We're going to ask about your experiences. We're not trying to sell you anything."
- "Tell me about your role and what you do day to day."

**Exploration (the bulk of the interview):**
- "Tell me about the last time you [did the activity]?" (specific past instance, not hypothetical)
- "What was going on that led you to do that?"
- "How do you currently handle [problem area]?"
- "What have you tried before? What worked? What didn't?"
- "Walk me through exactly what happened step by step."
- "How does this problem affect the rest of your work?"

**Probing for depth:**
- "You mentioned [X] — can you tell me more about that?"
- "Why is that important to you?"
- "What would happen if you couldn't do that?"
- "How did that make you feel?"

**Closing:**
- "Is there anything else you think we should know?"
- "Who else do you think we should talk to?"
- "Would you be open to us reaching out again as we learn more?"

### Interview Anti-Patterns (The Mom Test)
- ❌ "Would you use a feature that does X?" (hypothetical = useless)
- ❌ "Do you like this idea?" (people want to be nice)
- ❌ "How much would you pay for X?" (what people say ≠ what they do)
- ❌ Pitching your solution during the interview
- ❌ Leading questions that confirm your existing beliefs
- ✅ Ask about specific past behavior
- ✅ Listen for problems, not feature requests
- ✅ Dig into the context around decisions

### After Every Interview

1. **Debrief immediately** (within 24 hours): What were the key moments? What surprised us?
2. **Tag key quotes and insights** for later synthesis
3. **Add opportunities to the OST** (new pain points, needs, desires)
4. **Note assumptions that might need testing**

## Step 3: Build the Opportunity Solution Tree (OST)

The OST is a visual map connecting everything from your target outcome down to specific experiments.

```
                        [OUTCOME]
                      Increase activation
                            │
          ┌─────────────────┼─────────────────┐
          │                 │                 │
    [OPPORTUNITY]     [OPPORTUNITY]      [OPPORTUNITY]
    Users don't       Empty state is     Setup takes
    know what to      overwhelming       too long
    do first
          │                 │                 │
    ┌─────┴─────┐    ┌─────┴─────┐    ┌─────┴─────┐
    │           │    │           │    │           │
 [SOLUTION] [SOLUTION] [SOLUTION] [SOLUTION] [SOLUTION] [SOLUTION]
  Guided    Templates  Quick-start Sample    Import    SSO
  tour                  templates  data      wizard    setup
    │           │         │
    │           │         │
[EXPERIMENT] [EXPERIMENT] [EXPERIMENT]
 A/B test    Prototype   Concierge
 3-step vs   with 5      onboard 5
 5-step tour users       users manually
```

### Building the OST

1. **Start with the outcome at the top** — The single metric you're trying to move

2. **Map opportunities** — These come from research:
   - Customer interviews (pain points, unmet needs, desires)
   - Analytics (where do users drop off?)
   - Support tickets (what frustrates users?)
   - Sales feedback (what do prospects ask for?)
   - Competitive analysis (what are competitors solving that we're not?)

   An opportunity should be phrased as a user need, not a solution:
   - ✅ "Users don't know what to do after signup"
   - ❌ "We need a guided tour" (that's a solution, not an opportunity)

3. **Generate solutions** — For each opportunity, brainstorm 3-5 potential solutions:
   - Don't evaluate yet — go for quantity
   - Include the product trio in ideation
   - Consider: product changes, educational content, onboarding flows, UX improvements, pricing/packaging, integrations

4. **Design experiments** — For the most promising solutions:
   - Smallest thing you can do to test the riskiest assumption
   - Not a full feature — a test to learn whether the solution is worth building

### OST Rules
- **One opportunity can have multiple solutions**
- **One solution can address multiple opportunities** (draw connection lines)
- **Opportunities must come from research** — not from your imagination
- **Solutions are hypotheses** — not commitments
- **Experiments test assumptions** — they are NOT MVPs (they're smaller)

## Step 4: Identify and Test Assumptions

For each solution you're considering, identify what MUST be true for it to work. Then test the riskiest assumptions first.

### Assumption Categories

| Category | Question | Risk |
|----------|----------|------|
| **Desirability** | Will users want this? | You build something nobody wants. |
| **Viability** | Can the business support this? | You build something that loses money or can't scale operationally. |
| **Feasibility** | Can we build this? | You commit to something engineering can't deliver. |
| **Usability** | Can users figure out how to use it? | You build something users can't navigate. |
| **Ethical** | Should we build this? | You build something that harms users or society. |

### Assumption Testing Process

1. **List all assumptions** for the solution
2. **Identify the riskiest assumption** — Which one, if wrong, would make the whole solution fail?
3. **Design the smallest experiment** to test that assumption
4. **Define success criteria** — What result would increase confidence? What result would kill the idea?
5. **Run the experiment**
6. **Decide**: Invest (assumption validated), pivot (assumption wrong, adjust solution), or kill (assumption wrong, abandon solution)

### Experiment Types (Smallest to Largest)

| Experiment | Effort | What It Tests | Example |
|------------|--------|--------------|---------|
| **Thought experiment** | Minutes | Logic and reasoning | "If users need X, why aren't they asking for it in support tickets?" |
| **Existing data analysis** | Hours | Behavior from analytics | "How many users already try to do X on their own?" |
| **Landing page test** | Days | Demand/interest | Create a page describing the solution, measure click-through |
| **Wizard of Oz** | Days | Value proposition | Manually simulate the feature for a few users |
| **Concierge** | Days-Weeks | Value + willingness to pay | Manually deliver the service to early customers |
| **Prototype test** | 1-2 weeks | Usability + desirability | Clickable prototype tested with 5-10 users |
| **A/B test** | Weeks | Behavior at scale | Randomized experiment with real users |

### Before Running Any Experiment, Define

```markdown
## Experiment: [Name]

**Solution Being Tested:** [Brief description]
**Riskiest Assumption:** [What must be true?]
**Experiment Design:** [What exactly will we do?]
**Sample:** [Who, how many?]
**Duration:** [How long?]
**Success Criteria:** [What result would increase our confidence?]
**Kill Criteria:** [What result would make us abandon this solution?]
**Cost:** [Time, money, resources]
```

## Step 5: Set Up the Product Trio

The product trio (PM + Designer + Engineer) is the core discovery team.

### Trio Roles

| Role | Discovery Responsibilities |
|------|--------------------------|
| **Product Manager** | Leads outcome definition, facilitates decision-making, own's the OST |
| **Designer** | Leads user research, prototypes solutions, designs experiments |
| **Engineer** | Assesses feasibility, suggests technical solutions, builds experiment code |

### Trio Cadence

| Activity | Frequency | Duration | Purpose |
|----------|-----------|----------|---------|
| **Customer interviews** | Weekly (minimum 1) | 30-45 min | At least one trio member attends every interview |
| **Interview debrief** | After each interview | 15 min | Capture insights while fresh |
| **OST review** | Weekly or bi-weekly | 30-60 min | Update tree with new opportunities, prioritize |
| **Assumption testing review** | Weekly | 15-30 min | Review active experiments, decide next steps |
| **Synthesis session** | Monthly | 2 hours | Aggregate learnings, identify patterns across interviews |

### Why the Trio Matters

- **Engineers in interviews** = better solutions (they understand the problem, not just the spec)
- **Designers in interviews** = better empathy (they see real users struggling, not just personas)
- **Shared understanding** = faster decisions (no "telephone game" of secondhand insights)
- **Collective ownership** = better outcomes (everyone invested in solving the right problem)

## Step 6: Define the Learning Loop

Insights must flow from discovery into product decisions:

```
Interview → Insights → OST Update → Prioritize Opportunity → Test Solution → Learn → Interview → ...
```

### Knowledge Management

- Maintain a living document of key insights from interviews
- Tag insights by opportunity, persona, and theme
- Review the OST before every roadmap or prioritization session
- Share interview highlights with the broader team (not just the trio)
- Build a searchable research repository (tools: Dovetail, Notion, Airtable, or a simple shared doc)

### When Discovery Changes the Roadmap

Discovery should CHANGE decisions:
- **Kill ideas** that users don't actually need
- **Pivot solutions** that have a flawed assumption
- **Prioritize opportunities** that are more painful than expected
- **Delay features** that need more research
- **Add opportunities** that weren't visible before

If discovery never changes your roadmap, you're not doing discovery — you're doing validation theater.

## Step 7: Save and Maintain

Save the OST and supporting documentation:

```markdown
# Opportunity Solution Tree — [Outcome]

**Last Updated:** YYYY-MM-DD
**Outcome:** [Metric to move, with baseline and target]

## Opportunities
| Opportunity | Source | Evidence Strength | Priority |
|-------------|--------|------------------|----------|
| ... | Interview date, user ID, or data source | Strong/Medium/Weak | Now/Next/Later |

## Solutions Being Explored
| Solution | Opportunity Addressed | Current Stage | Next Step |
|----------|----------------------|--------------|-----------|
| ... | ... | Ideation / Testing / Building | ... |

## Active Experiments
[Details from assumption testing template above]

## Key Insights (Last 4 Weeks)
- [Insight from research]
- [Insight from research]
```

Save to: `docs/product-superpowers/continuous-discovery/ost-<outcome>.md`

Update the OST:
- **After every interview** — Add new opportunities or evidence
- **Weekly** — Review experiment progress
- **Monthly** — Full review with trio, reprioritize

## Key Principles

- **Discovery is continuous** — Not a phase you exit. It runs alongside delivery.
- **Outcome over output** — The OST starts with a metric, not a feature.
- **Smallest experiment possible** — Test the riskiest assumption with the least effort.
- **Interview weekly, always** — If you're not talking to users every week, you're guessing.
- **Trio in discovery** — PM + Designer + Engineer together. Not PM alone writing requirements.
- **Opportunities from users, not imagination** — Every opportunity on the OST must trace back to research.
- **Discovery should change decisions** — If it doesn't, you're not doing it right.

## Common Mistakes

- Solution-first OST building (starting with solutions and working backward to justify them)
- Discovery as a scheduled phase ("we'll do discovery in Q1, then build in Q2-Q4")
- PM-only discovery (engineers and designers not participating)
- Over-researching (analysis paralysis — never moving from research to action)
- Under-researching (one interview and "we know enough")
- Confirmation bias (only hearing what supports your existing ideas)
- No clear outcome (doing research without knowing what you're trying to learn)
- Not killing ideas (discovery reveals a bad idea but you build it anyway)
- OST as a static artifact (built once, never updated)

## Key References

- "Continuous Discovery Habits" by Teresa Torres (the primary source)
- Product Talk articles and courses (producttalk.org)
- Teresa Torres, "My Team of Agents" (Product Talk, May 2026)
- "The Mom Test" by Rob Fitzpatrick (customer interviews)
- "Inspired" and "Empowered" by Marty Cagan (product teams and discovery)
- "Lean UX" by Jeff Gothelf and Josh Seiden
