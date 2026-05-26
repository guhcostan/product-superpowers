---
name: continuous-discovery
description: Use when setting up or improving a continuous product discovery practice with weekly customer interviews.
---

# Continuous Discovery

Establish and maintain a continuous product discovery practice. Based on Teresa Torres' "Continuous Discovery Habits." Discovery is not a phase — it's ongoing.

**Announce at start:** "I'm using the continuous-discovery skill to [purpose]."

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

| Output (what you build) | Outcome (what changes) |
|------------------------|------------------------|
| "Build a new onboarding flow" | "Increase new user activation from 40% to 65%" |
| "Add a sharing feature" | "Increase weekly active teams from 500 to 1,200" |
| "Redesign the dashboard" | "Reduce time-to-first-insight from 12 min to 3 min" |

Choose a leading indicator within your team's influence, measurable, and with room for improvement — not a lagging revenue metric. Examples: "Reduce churn for small teams," "Increase feature adoption among enterprise accounts."

## Step 2: Set Up Interview Cadence

**Minimum:** 1 customer interview per week, 30–45 min, rotating among the product trio. Automate recruitment via in-app prompts, email, or sales introductions.

**Interview structure** (follow "The Mom Test"):
- **Opening:** You're learning, not selling. "Tell me about your role and what you do day to day."
- **Exploration:** Focus on specific past instances: "Tell me about the last time you [did X]?" "Walk me through step by step." "What have you tried before? What worked? What didn't?"
- **Probing:** "Why is that important?" "What would happen if you couldn't do that?"
- **Closing:** "Who else should we talk to?" "Can we reach out again as we learn more?"

**Anti-patterns:** No hypotheticals ("Would you use X?"), no pitching, no leading questions. Ask about specific past behavior; listen for problems, not feature requests.

**After every interview:** Debrief within 24 hours, tag key quotes, add opportunities to the OST, note assumptions to test.

## Step 3: Build the Opportunity Solution Tree (OST)

The OST maps: **Outcome → Opportunities → Solutions → Experiments**. One outcome at top, branching into opportunities (user needs surfaced by research), each branching into 3–5 candidate solutions, each tested via the smallest meaningful experiment.

**Building the OST:**
1. Start with the outcome at top
2. Map opportunities from interviews, analytics, support tickets, sales feedback, competitive analysis. Phrase as user needs: ✅ "Users don't know what to do after signup" / ❌ "We need a guided tour"
3. Generate 3–5 solutions per opportunity (don't evaluate yet; include the trio; go for quantity)
4. Design the smallest experiment to test the riskiest assumption for each promising solution

**Rules:** Opportunities must trace to research, not imagination. Solutions are hypotheses, not commitments. Experiments are smaller than MVPs. One solution can address multiple opportunities.

## Step 4: Identify and Test Assumptions

| Category | Question | Risk |
|----------|----------|------|
| **Desirability** | Will users want this? | You build something nobody wants |
| **Viability** | Can the business support this? | You build something that loses money |
| **Feasibility** | Can we build this? | Engineering can't deliver |
| **Usability** | Can users figure it out? | Users can't navigate it |
| **Ethical** | Should we build this? | Harms users or society |

**Process:** List assumptions → identify riskiest (if wrong, solution fails) → design smallest experiment → define success and kill criteria → run → decide: invest, pivot, or kill.

| Experiment | Effort | What It Tests | Example |
|------------|--------|--------------|---------|
| Thought experiment | Minutes | Logic and reasoning | "If users need X, why aren't they asking in support?" |
| Existing data analysis | Hours | Current behavior | "How many users already try to do X on their own?" |
| Landing page test | Days | Demand/interest | Page describing solution, measure click-through |
| Wizard of Oz / Concierge | Days–Weeks | Value proposition | Manually simulate the feature for a few users |
| Prototype test | 1–2 weeks | Usability + desirability | Clickable prototype with 5–10 users |
| A/B test | Weeks | Behavior at scale | Randomized experiment with real users |

**Before any experiment**, document: solution tested, riskiest assumption, experiment design, sample size, duration, success criteria, kill criteria, and cost.

## Step 5: Set Up the Product Trio

| Role | Discovery Responsibilities |
|------|--------------------------|
| **PM** | Leads outcome definition, facilitates decisions, owns the OST |
| **Designer** | Leads user research, prototypes solutions, designs experiments |
| **Engineer** | Assesses feasibility, suggests technical solutions, builds experiment code |

| Activity | Frequency | Duration |
|----------|-----------|----------|
| Customer interviews | Weekly (min 1) | 30–45 min |
| Interview debrief | After each | 15 min |
| OST review | Weekly/bi-weekly | 30–60 min |
| Assumption testing review | Weekly | 15–30 min |
| Synthesis session | Monthly | 2 hours |

At least one trio member attends every interview. This creates shared understanding, avoids secondhand insights, and leads to better solutions.

## Step 6: Define the Learning Loop

```
Interview → Insights → OST Update → Prioritize Opportunity → Test Solution → Learn → Interview...
```

- Maintain a searchable living document of insights, tagged by opportunity/persona/theme
- Review the OST before every roadmap or prioritization session; share interview highlights with the broader team
- Discovery must change decisions: kill bad ideas, pivot flawed solutions, reprioritize opportunities. If it never changes your roadmap, you're doing validation theater.

## Step 7: Save and Maintain

Save the OST to `docs/product-superpowers/continuous-discovery/ost-<outcome>.md` with:
- Outcome (metric, baseline, target)
- Opportunities table (source, evidence strength, priority)
- Solutions being explored (stage, next step)
- Active experiments and key insights (last 4 weeks)

Update after every interview (new opportunities/evidence), weekly (experiment progress), monthly (full trio review and reprioritization).

## Key Principles

- **Discovery is continuous** — Not a phase. Runs alongside delivery.
- **Outcome over output** — The OST starts with a metric, not a feature.
- **Smallest experiment possible** — Test the riskiest assumption with least effort.
- **Interview weekly, always** — Not talking to users every week = guessing.
- **Trio in discovery** — PM + Designer + Engineer together, not PM alone.
- **Opportunities from research** — Every OST opportunity must trace back to evidence.
- **Discovery should change decisions** — If it doesn't, you're not doing it right.

## Common Mistakes

- Solution-first OST (starting with solutions, working backward to justify them)
- Discovery as a scheduled phase ("discovery in Q1, build in Q2–Q4")
- PM-only discovery (engineers and designers not participating)
- Over-researching (analysis paralysis) or under-researching (one interview and "we know enough")
- Confirmation bias, no clear outcome, not killing bad ideas, static OST never updated

## Key References

- "Continuous Discovery Habits" by Teresa Torres (primary source)
- Product Talk (producttalk.org)
- "The Mom Test" by Rob Fitzpatrick (customer interviews)
- "Inspired" and "Empowered" by Marty Cagan
- "Lean UX" by Jeff Gothelf and Josh Seiden
