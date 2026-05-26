---
name: product-strategy
description: Use when defining or refining product vision, mission, strategic trade-offs, build-vs-buy decisions, or product-market fit assessment.
---

# Product Strategy

Define product vision, mission, and strategic trade-offs. Assess product-market fit and make build-vs-buy decisions.

**Announce at start:** "I'm using the product-strategy skill to [purpose]."

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Articulate vision and mission** — Where are we going? Why do we exist?
2. **Assess current state** — Where are we now? What's working? What isn't?
3. **Analyze strategic options** — What paths are available?
4. **Evaluate trade-offs** — Build vs. buy? Sustaining vs. disruptive?
5. **Assess product-market fit** — Are we serving a real need for a real market?
6. **Define strategic choices** — Where will we play? How will we win?
7. **Document and get alignment** — Write the strategy document, get stakeholder buy-in

## Step 1: Articulate Vision and Mission

### Product Vision

The aspirational future state you're working toward. Long-term (years), inspirational, and relatively stable. It describes the WORLD you want to create.

**Characteristics:**
- Inspirational and ambitious
- Customer-centric (not about you)
- Stable over years (not tied to specific technology or trends)
- Memorable (can be repeated by anyone on the team)

**Format:**
```
A world where [describe the future state you're creating].
```

**Examples:**
- Airbnb: "Belong anywhere."
- Tesla: "Accelerate the world's transition to sustainable energy."
- LinkedIn: "Create economic opportunity for every member of the global workforce."
- Google (original): "Organize the world's information and make it universally accessible and useful."

### Product Mission

What you do to pursue the vision. More concrete, but still strategic. Answers: what do we do, for whom, and why?

**Format:**
```
[Product name] helps [target customer] achieve [key benefit] by [unique approach].
```

**Examples:**
- Slack: "Make work life simpler, more pleasant, and more productive."
- Stripe: "Increase the GDP of the internet."
- Notion: "Make it possible for everyone in the world to customize their own software tools."

### Strategy = Vision + Choices

Strategy is NOT the vision. Strategy is the set of choices you make about where to play and how to win, given your vision and the current market reality.

```
Vision (where we're going)
    → Strategy (how we'll get there — our choices)
        → Roadmap (what we'll do now/next/later)
            → Execution (shipping value)
```

## Step 2: Assess Current State

Honest assessment of where the product stands today:

### Health Indicators

| Dimension | Questions to Ask | Red Flags |
|-----------|-----------------|-----------|
| **User satisfaction** | NPS? Retention? User complaints/support volume? | NPS < 0, churn increasing, support overwhelmed |
| **Growth** | Organic acquisition? Word of mouth? Paid CAC sustainable? | Growth flat or declining, CAC > LTV |
| **Revenue** | MRR/ARR growth? LTV? Expansion revenue? | Revenue growth slowing, churn eating growth |
| **Market position** | Market share? Win/loss rate? Competitive threats? | Losing deals to competitors, price pressure |
| **Team** | Morale? Velocity? Technical debt? | Burnout, slow shipping, bug regression |
| **Differentiation** | What can only we do? Is that gap widening or narrowing? | Competitors copying features, commoditization |

## Step 3: Analyze Strategic Options

Common strategic paths:

### Growth Strategies (Ansoff Matrix)

| | Existing Markets | New Markets |
|---|---|---|
| **Existing Products** | **Market Penetration**: Get more of existing market | **Market Development**: Enter new geos/segments |
| **New Products** | **Product Development**: New features for current users | **Diversification**: New products for new markets |

### Generic Strategies (Porter)

| Strategy | Description | Requirements | Risks |
|----------|-------------|-------------|-------|
| **Cost Leadership** | Be the lowest-cost provider | Scale, efficiency, process optimization | Price wars, margin erosion |
| **Differentiation** | Be uniquely valuable in ways customers will pay for | Innovation, brand, design, customer experience | Competitors copy, differentiation erodes |
| **Focus** | Serve a specific niche exceptionally well | Deep domain expertise, tailored solution | Niche too small, niche commoditized |

## Step 4: Evaluate Trade-Offs

### Build vs. Buy Decision Framework

| Consideration | Build | Buy / Integrate |
|--------------|-------|-----------------|
| **Core to your differentiation?** | Yes → Build. This is what makes you unique. | No → Buy. Don't build what isn't your secret sauce. |
| **Mature solutions exist?** | No → Build. You get to define the category. | Yes → Buy. Don't reinvent the wheel. |
| **Internal expertise available?** | Yes → Build. You have the talent. | No → Buy. Building without expertise = long timeline, poor quality. |
| **Time to market critical?** | No → Build. You have time to do it right. | Yes → Buy. Speed matters more than perfection. |
| **Total cost of ownership** | Build if long-term TCO is lower. | Buy if short-term speed + maintenance is cheaper. |

### Sustaining vs. Disruptive Innovation (Christensen)

| | Sustaining Innovation | Disruptive Innovation |
|---|---|---|
| **Target** | Your best, most demanding customers | Overlooked segments or non-consumers |
| **What it does** | Makes good products better | Makes inaccessible products accessible |
| **Incumbent response** | Motivated to invest and protect | Motivated to ignore (low margins, wrong customers) |
| **Risk to you** | Competitors are investing here too | If you're the incumbent, you'll be tempted to ignore it |

**As a PM, ask yourself:**
- Are we only listening to our best customers? (They'll ask for sustaining innovations.)
- Is there a low-end or new-market disruption that could threaten us?
- Should we create a separate unit to pursue a disruptive opportunity?
- When competitors launch something "worse but cheaper/more accessible," are you dismissing it?

## Step 5: Assess Product-Market Fit

### The Sean Ellis Test

Survey your users:
> "How would you feel if you could no longer use [product]?"

- Very disappointed
- Somewhat disappointed
- Not disappointed (it isn't that useful)
- N/A — I no longer use [product]

**Threshold**: If 40% or more say "very disappointed," you have product-market fit.

### Rahul Vohra's PMF Engine

If you have PMF:
1. Segment by "very disappointed" responses — who are these people?
2. Identify what they love (the "high-expectation customers")
3. Double down on what makes those users love you
4. Don't try to please everyone — focus on your enthusiasts

### Signs of Product-Market Fit

| Sign | What to Look For |
|------|-----------------|
| **Organic growth** | Word of mouth, viral coefficient > 1, people finding you without marketing |
| **Low churn / high retention** | Users who sign up stay. Cohort retention curves flatten. |
| **Increasing usage** | Users use the product more over time, not less |
| **Users would be upset** | If you shut down, users would genuinely care |
| **Shorter sales cycles** | Less convincing needed. Prospects come to you. |
| **Customer praise** | Support tickets include praise, not just problems |
| **You can't keep up** | Demand outpaces your ability to serve it |

### If You DON'T Have PMF

1. Talk to users who churned. Why did they leave?
2. Talk to users who stayed. What keeps them?
3. Identify the smallest segment where you DO have strong fit
4. Narrow your focus to that segment
5. Iterate the product until you're indispensable to them
6. Expand from that beachhead

## Step 6: Define Strategic Choices

### Strategy on One Page

```markdown
# Product Strategy — [Product Name] — [Date]

## Vision
[Where are we going? 3-5 year aspirational state.]

## Mission
[What do we do, for whom, and why?]

## Current State Assessment
[Honest assessment of where we are. Strengths. Weaknesses. Market position.]

## Strategic Choices

### Where We Will Play
- Target market: [Who specifically?]
- Key segments: [Which customer segments?]
- Geography: [Where?]
- Use cases: [What problems are we solving?]

### Where We Will NOT Play
- [Explicitly excluded segments, markets, or use cases]

### How We Will Win
- Our differentiation: [What can only we do?]
- Our moat: [What protects us from competitors?]
- Our business model: [How do we capture value?]

### Key Bets and Assumptions
- [What must be true for this strategy to work?]
- [What are we uncertain about?]

### Key Risks
- [What could cause this strategy to fail?]
- [How will we mitigate those risks?]

## Strategic Trade-offs Made
- [Build vs. Buy decision with rationale]
- [Sustaining vs. Disruptive focus with rationale]
- [Speed vs. Quality decisions]
- [Breadth vs. Depth decisions]
```

Save to: `docs/product-superpowers/strategy/product-strategy-YYYY-MM-DD.md`

## Step 7: Get Alignment

Strategy that isn't understood or supported fails.

- **Present to leadership**: Executive summary format. Focus on choices and trade-offs.
- **Socialize with peers**: Get input from engineering, design, marketing, sales leadership.
- **Share with the team**: Everyone should understand the strategy and their role in it.
- **Reference in decisions**: Every roadmap item should connect back to strategy.
- **Revisit regularly**: Strategy is not "set and forget." Review quarterly.

## Key Principles

- **Strategy is what you say NO to** — The most important part of strategy is what you choose NOT to do.
- **Vision is stable; strategy evolves** — The destination stays the same. The path adjusts.
- **Differentiation over features** — Being better at the same things = commodity. Being different = strategy.
- **Honesty over narrative** — Acknowledge weaknesses. Face threats. Don't sugarcoat.
- **Focus over breadth** — Doing one thing exceptionally well beats doing many things adequately.
- **Strategy without execution is hallucination** — Strategy must translate to roadmap choices.

## Common Mistakes

- Confusing vision with strategy (vision = destination, strategy = path)
- Strategy as a list of features ("our strategy is to build X, Y, Z")
- No explicit trade-offs (if you're not saying no, you don't have a strategy)
- Trying to serve everyone (lack of focus = lack of strategy)
- Copying competitors' strategies (their context is different from yours)
- Strategy as an annual exercise (should be revisited quarterly at minimum)
- No connection to execution (strategy document exists but doesn't influence roadmap)

## Key References

- "Good Strategy Bad Strategy" by Richard Rumelt
- "Playing to Win" by A.G. Lafley and Roger Martin
- "7 Powers" by Hamilton Helmer
- "The Innovator's Dilemma" and "Competing Against Luck" by Clayton Christensen
- "Crossing the Chasm" by Geoffrey Moore
- "Obviously Awesome" by April Dunford (positioning)
- "Blue Ocean Strategy" by W. Chan Kim and Renée Mauborgne
