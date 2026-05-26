# Product Superpowers

Product Superpowers is a complete product management methodology for your AI agents, built on top of a set of composable skills and initial instructions that make sure your agent uses them — from discovery through launch.

## Quickstart

Give your agent Product Superpowers: [Claude Code](#claude-code), [OpenCode](#opencode).

## How It Works

It starts from the moment you bring a new product idea or feature request. Your agent *doesn't* jump into writing a PRD. Instead, it steps back and runs discovery — understanding the problem, interviewing users (or you), mapping Jobs-to-be-Done, and validating assumptions before anything gets committed to requirements.

Once discovery is done and you've signed off, your agent writes a PRD in Amazon PR/FAQ format — a customer-focused press release plus FAQs for both customers and internal stakeholders. You review it in sections.

After the PRD is approved, your agent breaks it into user stories with INVEST criteria and Gherkin acceptance criteria, prioritized and organized into epics.

Supporting skills handle roadmapping, stakeholder communication, launch planning, analytics, competitive analysis, and continuous discovery — all triggered automatically when the context is right.

And because the skills trigger automatically, you don't need to do anything special. Your PM agent just has Product Superpowers.

## Installation

### Claude Code

Product Superpowers is available via the Superpowers marketplace:

```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install product-superpowers@superpowers-marketplace
```

Or install directly from GitHub:

```bash
/plugin install product-superpowers@git+https://github.com/your-org/product-superpowers.git
```

### OpenCode

Add to your `opencode.json` plugin array:

```json
{
  "plugin": ["product-superpowers@git+https://github.com/your-org/product-superpowers.git"]
}
```

Or follow the detailed install guide at `.opencode/INSTALL.md`.

## The Core Workflow

1. **product-discovery** — Activates before any product work. Understands the problem through JTBD, user interviews, and opportunity assessment. Validates before building.

2. **writing-prd** — Activates after discovery approval. Writes PRD in Amazon PR/FAQ format with success metrics, assumptions, constraints, and open questions.

3. **user-story-writing** — Activates after PRD approval. Breaks PRD into user stories with INVEST criteria, Gherkin acceptance criteria, and epic/story hierarchy.

4. **prioritization** — Scores and orders backlog items using RICE, ICE, MoSCoW, or Kano.

5. **roadmapping** — Maintains outcome-based roadmap with Now/Next/Later and OKRs.

6. **design-handoff** — Prepares design specs for engineering with tokens, states, accessibility, and QA checklist.

7. **stakeholder-management** — Status updates, executive summaries, managing up, conflict resolution.

8. **launch-planning** — GTM strategy, pre/during/post-launch checklists, beta management, rollout strategies.

9. **product-analytics** — North Star metric, AARRR funnel, feature adoption, A/B testing.

10. **competitive-analysis** — SWOT, Porter's Five Forces, feature comparison matrix.

11. **product-strategy** — Vision, mission, build vs buy, product-market fit assessment.

12. **continuous-discovery** — Teresa Torres framework: Opportunity Solution Trees, assumption testing, product trio.

**The agent checks for relevant skills before any PM task.** Mandatory workflows, not suggestions.

## What's Inside

### Skills Library

**Core Workflow**
- **product-discovery** — Problem understanding, JTBD, user interviews, opportunity assessment
- **writing-prd** — Amazon PR/FAQ, SVPG Product Brief, Shreyas Doshi frameworks
- **user-story-writing** — INVEST criteria, Gherkin acceptance criteria, epic breakdown

**Decision Making**
- **prioritization** — RICE, ICE, MoSCoW, Kano, Value/Effort matrix
- **roadmapping** — Outcome-based roadmaps, Now/Next/Later, OKRs

**Execution**
- **design-handoff** — Design specs, tokens, states, accessibility, design QA
- **launch-planning** — GTM strategy, launch checklists, beta, rollout
- **stakeholder-management** — Status updates, executive summaries, managing up
- **product-analytics** — North Star, AARRR, feature adoption, A/B testing

**Continuous Strategy**
- **competitive-analysis** — SWOT, Porter's Five Forces, feature comparison
- **product-strategy** — Vision, build vs buy, PMF assessment
- **continuous-discovery** — Opportunity Solution Trees, assumption testing, product trio

**Meta**
- **using-product-superpowers** — Introduction to the skills system

## Philosophy

- **Discovery before requirements** — Understand the problem before writing what to build
- **Outcomes over outputs** — Measure success by business impact, not features shipped
- **Evidence over opinions** — Validate with data and user research, not intuition
- **Systematic over ad-hoc** — Process over guessing
- **Complexity reduction** — Ruthlessly descope; YAGNI applies to product too

## Key References

Product Superpowers draws from established product management thinking:

- Marty Cagan (SVPG) — "Inspired," "Empowered," product operating model
- Teresa Torres — "Continuous Discovery Habits," Opportunity Solution Trees
- Shreyas Doshi — PM craft, strategic thinking frameworks
- Amazon — PR/FAQ Working Backwards methodology
- Clayton Christensen — Jobs-to-be-Done, Innovator's Dilemma
- John Doerr — OKRs ("Measure What Matters")
- Melissa Perri — "Escaping the Build Trap," outcome over output
- Rob Fitzpatrick — "The Mom Test," customer interview methodology
- April Dunford — "Obviously Awesome," product positioning
- Strategyzer — Business Model Canvas, Value Proposition Canvas

## License

MIT License — see LICENSE file for details.
