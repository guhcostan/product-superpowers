<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/banner.png">
    <img src="assets/banner.png" width="100%" alt="Product Superpowers banner">
  </picture>
</p>

<p align="center">
  <strong>Give your AI agent a PM brain.</strong>
</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> ·
  <a href="#how-it-works">How It Works</a> ·
  <a href="#skills">Skills</a> ·
  <a href="#faq">FAQ</a>
</p>

---

## What is this?

Product Superpowers is a set of 18 composable skills that give your AI agent a complete product management methodology — including subagent-powered research, review, and visual collaboration. Instead of jumping straight to writing requirements, your agent runs discovery, validates problems, writes PRDs, breaks them into stories, prioritizes, and plans launches — systematically, every time.

### The pipeline

```
Idea  →  Discovery  →  PRD  →  Stories  →  Prioritize  →  Launch
          ↕             ↕        ↕            ↕               ↕
      Roadmap   ·   Analytics  ·  Stakeholders  ·  Competitive  ·  Strategy  ·  Continuous Discovery
```

## Full PDLC coverage

Covers the complete Product Development Life Cycle — from ideation to commercialization:

| PDLC Stage | Skill |
|-----------|-------|
| 1. Ideation | `product-discovery` — JTBD, user interviews, problem validation |
| 2. Idea screening | `prioritization` — RICE, ICE, MoSCoW scoring |
| 3. Concept testing | `continuous-discovery` — assumption testing, concierge MVP |
| 4. Business analysis | `product-strategy` + `competitive-analysis` — PMF, SWOT, build vs buy |
| 5. Product design | `design-handoff` + `user-story-writing` — tokens, states, INVEST, Gherkin |
| 6. Market testing | `launch-planning` — beta programs, staged rollout |
| 7. Commercialization | `launch-planning` — GTM strategy, launch checklists |

## Why this?

| If you... | Your agent will... |
|-----------|-------------------|
| Have an idea for a feature | Run discovery first — JTBD, user interviews, opportunity assessment. Never jumps to solution. |
| Need a PRD written | Outputs Amazon PR/FAQ format — press release + external FAQ + internal FAQ. Metrics, assumptions, constraints, all included. |
| Have a PRD ready | Breaks it into INVEST-validated user stories with Gherkin acceptance criteria. Every state documented. |
| Need to prioritize | Scores with RICE, segments with MoSCoW, classifies with Kano. Outputs ordered list with rationale. |
| Are about to launch | Produces pre/during/post-launch checklists, beta plan, rollout strategy, kill criteria, and post-launch rituals. |
| Want to keep discovery alive | Sets up weekly interview cadence, Opportunity Solution Trees, and assumption testing — Teresa Torres framework. |

---

## Quick Start

### Claude Code

```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install product-superpowers@superpowers-marketplace
```

### OpenCode

Add to `opencode.json`:

```json
{ "plugin": ["product-superpowers@git+https://github.com/guhcostan/product-superpowers.git"] }
```

Verify: **"Tell me about your product superpowers"**

---

## Skills

<details>
<summary><strong>Core Workflow</strong> — the primary pipeline</summary>

| Skill | What triggers it |
|-------|-----------------|
| `product-discovery` | New idea, feature request, "build X" |
| `writing-prd` | Discovery approved, need requirements |
| `user-story-writing` | PRD approved, need development stories |

</details>

<details>
<summary><strong>Decision Making</strong> — what to build and when</summary>

| Skill | What triggers it |
|-------|-----------------|
| `prioritization` | "Prioritize", backlog grooming |
| `roadmapping` | "Roadmap", OKRs, quarterly planning |

</details>

<details>
<summary><strong>Execution</strong> — shipping with quality</summary>

| Skill | What triggers it |
|-------|-----------------|
| `design-handoff` | "Handoff", design specs for engineering |
| `launch-planning` | "Launch", "release", "GTM" |
| `stakeholder-management` | Status updates, exec summaries |
| `product-analytics` | Metrics, KPIs, A/B tests |
| `pm-feedback-synthesis` | Interviews, surveys, tickets → themes & insights |

</details>

<details>
<summary><strong>Continuous Strategy</strong> — the long game</summary>

| Skill | What triggers it |
|-------|-----------------|
| `competitive-analysis` | "Competitors", SWOT, market analysis |
| `product-strategy` | Vision, build vs buy, PMF |
| `continuous-discovery` | Discovery cadence, OSTs, assumption testing |

</details>

<details>
<summary><strong>Agentic</strong> — subagent-powered workflows</summary>

| Skill | What triggers it |
|-------|-----------------|
| `pm-parallel-research` | Multiple independent research tasks |
| `pm-artifact-review` | PRD/stories/roadmap ready for review |
| `pm-visual-workspace` | Show OSTs, story maps, roadmaps visually |
| `pm-autonomous-execution` | PM plan ready, automatic execution |

</details>

<details>
<summary><strong>Meta</strong></summary>

| Skill | What triggers it |
|-------|-----------------|
| `using-product-superpowers` | Every session — bootstrap |

</details>

---

## How It Works

1. **You say "build X"** → Agent loads `product-discovery`. Asks you JTBD questions. Maps opportunities. Validates before any requirements.

2. **You approve discovery** → Agent loads `writing-prd`. Writes a press release, customer FAQ, internal FAQ. Defines metrics and scope.

3. **You approve the PRD** → Agent loads `user-story-writing`. Breaks it into INVEST stories with Given-When-Then acceptance criteria.

4. **Parallel support skills** trigger as needed: `prioritization` when you ask what to build first, `roadmapping` when you update the plan, `launch-planning` when you're close to shipping, `product-analytics` when you define metrics.

---

## Philosophy

- **Discovery before requirements** — Understand the problem before writing what to build
- **Outcomes over outputs** — Measure success by business impact, not features shipped
- **Evidence over opinions** — Validate with data and user research
- **Systematic over ad-hoc** — Process over guessing

---

## FAQ

**Does this replace a human PM?**
No. Product Superpowers automates the systematic parts of PM work — discovery structure, PRD formatting, story breakdown. Strategic judgment, taste, and deep user empathy remain human.

**Do I have to follow the full pipeline?**
The three core skills (discovery → PRD → stories) have hard gates — they won't let you skip steps. All other skills are flexible and invoked on demand.

**Does this work with Jira, Linear, Notion?**
The skills produce structured outputs that maps naturally to any tool. Specific integrations come later.

**What PM frameworks does it use?**
Amazon PR/FAQ, SVPG Opportunity Assessment, Teresa Torres' OSTs, Shreyas Doshi's frameworks, RICE/ICE/MoSCoW/Kano prioritization, JTBD, Gherkin acceptance criteria, and more.

**Can I use this with Claude Code AND OpenCode?**
Yes. Skills work across both. See Quick Start for install instructions.

---

## References

Product Superpowers draws from: Marty Cagan (SVPG), Teresa Torres, Shreyas Doshi, Amazon PR/FAQ, Clayton Christensen (JTBD), John Doerr (OKRs), Melissa Perri, Rob Fitzpatrick (The Mom Test), April Dunford, and Strategyzer.

---

MIT · [Contribute](https://github.com/guhcostan/product-superpowers) · [Issues](https://github.com/guhcostan/product-superpowers/issues)
