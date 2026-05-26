---
name: stakeholder-management
description: Use when you need to update stakeholders, write executive summaries, manage cross-functional relationships, or resolve conflicts with engineering and design.
---

# Stakeholder Management

Manage product stakeholder relationships effectively. Write clear status updates, prepare executive summaries, communicate across functions, and resolve conflicts constructively.

**Announce at start:** "I'm using the stakeholder-management skill to [purpose]."

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Identify stakeholders and their needs** — Who cares about what?
2. **Draft the communication** — Status update, executive summary, or presentation
3. **Review for stakeholder language** — Is it in their language? Focused on what they care about?
4. **Include risks and asks** — Don't just report. Ask for what you need.
5. **Present and follow up** — Close the loop

## Step 1: Identify Stakeholders and Their Needs

### Stakeholder Map

| Stakeholder Group | What They Care About | How to Communicate | Cadence |
|-------------------|---------------------|-------------------|---------|
| **Executive/VP** | Strategic alignment, ROI, key risks, resource decisions | Concise executive summary | Monthly or per milestone |
| **Engineering Lead** | Technical feasibility, dependencies, clarity of requirements | Detailed plan + trade-off discussions | Weekly or per sprint |
| **Design Lead** | User experience, consistency, design system alignment | Design reviews + user research findings | Weekly |
| **Marketing** | Launch timing, competitive positioning, messaging | Feature briefs + launch timelines | Per feature/launch |
| **Sales** | Customer commitments, competitive differentiators, availability | Enablement materials + roadmap highlights | Monthly |
| **Customer Success** | Feature changes, known issues, training needs | Release notes + support documentation | Per release |
| **Legal/Compliance** | Regulatory requirements, privacy, terms updates | Formal reviews of changes | Per significant change |
| **Peer PMs** | Dependencies, shared resources, learnings | Informal syncs + roadmap alignment | Bi-weekly |

## Step 2: The 3-Part Status Update

Use this format for regular stakeholder updates. It scales from a Slack message to a full document.

### Part 1: Headline

One sentence. The most important thing to know.

**Examples:**
- "Feature X is on track for launch next week. Beta feedback has been positive."
- "We've discovered a blocking issue in Feature Y. Now targeting a 2-week delay."
- "Q3 OKRs are all on track. Activation rate improved from 40% to 52% so far this quarter."

### Part 2: Key Accomplishments

3-5 bullet points of what was accomplished since the last update.

```
This period:
• Shipped onboarding redesign to 25% of new users — early data shows +15% activation
• Completed 12 user interviews for the collaboration feature discovery
• Resolved the performance regression (P95 latency back to 1.8s)
• Signed off on design specs for the dashboard v2
```

### Part 3: Key Risks, Blockers, and Asks

What's at risk? What do you need help with? What decisions need to be made?

```
Risks & Blockers:
• [BLOCKER] API team timeline slipped by 1 week — need to re-plan sprint scope
• [RISK] Analytics contractor leaves end of month — need to prioritize knowledge transfer
• [NEEDS DECISION] Mobile-first or desktop-first for the dashboard? Need alignment by Friday

Asks:
• Engineering: Need 2 engineers for the API integration spike next sprint
• Leadership: Please review and approve the Q4 roadmap draft by EOW
```

### Status Update Template

```markdown
# [Product/Feature] Status Update — [Date]

**Headline:** [One sentence — what's the most important thing to know?]

## Accomplishments
- [Accomplishment 1]
- [Accomplishment 2]
- [Accomplishment 3]

## Metrics
| Metric | Current | Target | Trend |
|--------|---------|--------|-------|
| ... | ... | ... | ↑/↓/→ |

## Risks & Blockers
- [Risk/blocker with impact and mitigation]

## Next Priorities
- [What's happening next]

## Asks
- [What do you need from the reader?]
```

## Step 3: Executive Summaries

When communicating to executives, use the SCRA framework:

**S**ituation — Context. What's the landscape?

**C**omplication — What changed? What's the problem or opportunity?

**R**esolution — What are we doing about it? (Present options, recommend one)

**A**sk — What do we need from you? (Decision, resources, air cover)

### Example

```
Situation:
Our user activation rate has been stuck at 40% for the past 3 quarters.
This is below our target of 65% and the primary reason retention is flat.

Complication:
Research with 20 users revealed that new users are overwhelmed by
the empty dashboard — they don't know what to do first. Competitors
all provide guided setup, which we lack.

Resolution:
I'm proposing a 6-week onboarding redesign sprint. We have 3 paths:
A) Full redesign (8 weeks, highest impact)
B) Quick-start templates only (3 weeks, medium impact) ← recommended
C) In-app tips only (1 week, lowest impact)

Ask:
Approve path B and allocate 1 designer and 2 engineers for 6 weeks
starting next sprint. I need your decision by Friday to hit Q3 targets.
```

## Step 4: Managing Up

Principles for communicating with executives and leadership:

- **No surprises** — Flag risks and issues early. Bad news does NOT get better with age.
- **Speak their language** — Business impact, ROI, strategic alignment. Not feature details.
- **Be concise** — Lead with the headline. Details are for appendices.
- **Bring options, not problems** — "Here's the situation, here are 3 paths, I recommend B because..."
- **Know their priorities** — Frame your work in terms of what THEY care about.
- **Connect to strategy** — Every ask should tie back to a company goal or OKR.
- **Respect their time** — If you booked 30 minutes, use 25. Send pre-reads.

## Step 5: Cross-Functional Communication

### Engineering

- **Build trust**: Understand technical constraints. Don't overpromise to stakeholders what engineering can't deliver.
- **Be specific**: Vague requirements waste engineering time. Clear acceptance criteria = faster delivery.
- **Respect technical judgment**: Engineers know how to build. PMs know what to build. Stay in your lane.
- **Include engineering in discovery**: Engineers present in user interviews = better solutions and fewer feasibility surprises.
- **Credit the team**: When things go well, it's the team's win. When things go wrong, it's the PM's responsibility.

### Design

- **User outcomes over pixel perfection**: Ship and learn. Don't block on a 2px alignment.
- **Design rationale**: Understand WHY design made their choices before challenging them.
- **Include design in discovery**: Designers should be in user interviews, not receiving secondhand notes.
- **Speak design language**: Learn basic design principles. It builds credibility and speeds collaboration.

### Marketing/Sales

- **Give them lead time**: Marketing needs weeks to prepare launch campaigns. Don't surprise them with "we're launching tomorrow."
- **Arm them with evidence**: Customer quotes, data, competitive comparisons. Help them sell.
- **Don't overpromise**: Sales will promise what you tell them. Be conservative in external commitments.
- **Protect the roadmap**: Sales will ask for features to close deals. Have a process for evaluating these requests.

### Customer Success/Support

- **Preview features before launch**: Support should never learn about a new feature from a customer.
- **Document known issues**: Be honest about what's rough. Support can set expectations.
- **Listen to support**: They hear unfiltered customer feedback every day. Mine this for discovery insights.

## Step 6: Conflict Resolution

### Common PM Conflicts

| Conflict | Typical Positions | Resolution Approach |
|----------|------------------|-------------------|
| **Refactor vs. new features** | Engineering wants to refactor. PM wants new features. | Allocate % of capacity for tech debt. Connect refactors to user-visible outcomes. |
| **Design perfection vs. shipping** | Design wants pixel-perfect. Engineering wants to ship. | Define "good enough to ship" together. Use design QA checklist. Iterate post-launch. |
| **Timeline pressure** | PM pushes for aggressive timeline. Engineering says it'll take longer. | Scope the date, don't date the scope. What must ship by the date? What can follow? |
| **MVP scope disagreement** | Different opinions on what's "minimum" | Go back to user outcomes. What's the smallest thing that tests our riskiest assumption? |

### Resolution Framework

1. **Separate people from the problem** — Focus on the issue, not personalities.
2. **Go back to user and business outcomes** — What's best for the user? What moves our metrics?
3. **Use data, not opinions** — Customer research, analytics, experiments. "I think" is weaker than "the data shows."
4. **Make trade-offs explicit** — "If we do X, we delay Y by Z weeks. Are we okay with that?"
5. **Escalate with context** — If stuck, present options with trade-offs to leadership. Don't just drop the problem.
6. **Build trust through consistency** — Follow through on commitments. Admit mistakes. Share credit.
7. **Celebrate shared wins** — When the team succeeds, it's because everyone contributed. Say so.

## Key Principles

- **No surprises** — Flag risks early. Bad news ages poorly.
- **Bring options, not problems** — Show you've thought about solutions before asking for help.
- **Speak their language** — What matters to an executive is different from what matters to an engineer.
- **Be consistent** — Regular, predictable communication builds trust.
- **Ask for what you need** — Status updates without asks are journal entries, not stakeholder management.
- **Close the loop** — When someone gives you input, tell them what you did with it.

## Red Flags

- Status updates that are all good news (unrealistic — there are always risks)
- Surprising stakeholders with bad news at the last minute
- Asking leadership to solve problems without presenting options
- Throwing engineering under the bus for timeline slips
- Overpromising to sales what the product can't deliver
- Avoiding conflict instead of resolving it (it gets worse, not better)
- Taking credit for team wins
- Not following up after asking for input

## Key References

- "Crucial Conversations" by Kerry Patterson et al.
- "Influence Without Authority" by Allan Cohen and David Bradford
- "Articulating Design Decisions" by Tom Greever
- "EMPOWERED" by Marty Cagan (chapters on stakeholder management)
- "Radical Candor" by Kim Scott
