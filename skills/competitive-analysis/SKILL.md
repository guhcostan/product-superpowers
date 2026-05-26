---
name: competitive-analysis
description: Use when analyzing competitors, understanding competitive landscape, conducting SWOT analysis, or positioning your product against alternatives.
---

# Competitive Analysis

Analyze the competitive landscape systematically. Identify direct and indirect competitors, map their strengths and weaknesses, and produce actionable insights for product strategy.

**Announce at start:** "I'm using the competitive-analysis skill to analyze [market/competitor]."

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Define the competitive landscape** — Direct, indirect, substitutes, potential entrants
2. **Gather data** — Product, pricing, positioning, reviews, funding, market signals
3. **Build feature comparison matrix** — Side-by-side capability analysis
4. **Apply SWOT analysis** — Strengths, weaknesses, opportunities, threats with cited evidence
5. **Apply strategic frameworks** — Porter's Five Forces, Strategic Group Map, or Wardley Map as needed
6. **Identify whitespace and threats** — Where are we uniquely strong? Where are we vulnerable?
7. **Extract insights and recommendations** — What should we DO differently?
8. **Save and maintain** — Document findings, schedule next review

## Step 1: Define the Competitive Landscape

| Category | Definition | Example (if you're Notion) |
|----------|-----------|---------------------------|
| **Direct Competitors** | Same problem, same solution, same target | Confluence, Coda, Craft |
| **Indirect Competitors** | Same problem, different solution | Google Docs + Sheets + Trello combined |
| **Substitutes** | Different approach to same need | Email + spreadsheets + shared drives |
| **Potential Entrants** | Adjacent companies that could enter | Microsoft building a Notion clone in Teams |

Select 3–7 competitors for deep analysis: market leaders, fast-growing challengers, adjacent threats, and aspirational peers.

## Step 2: Gather Data

| Dimension | Data Sources | Look For |
|-----------|-------------|----------|
| **Product** | Website, demos, trials, reviews | Key features, UX quality, differentiation |
| **Pricing** | Pricing page, mystery shopping | Price points, packaging, discount patterns |
| **Positioning** | Homepage, blog, PR, exec interviews | Target audience, key messages, brand personality |
| **Reviews** | G2, Capterra, Reddit, App Store | What users love, what frustrates them |
| **Business Health** | Crunchbase, news, hiring pace | Funding, growth trajectory, layoffs |
| **Team & Tech** | LinkedIn, job postings, engineering blogs | Talent, tech stack, open roles reveal priorities |

For each competitor answer: What do they do best? What are they bad at? Who are they really for? What do their users complain about most? How do they make money? What are they investing in?

## Step 3: Build Feature Comparison Matrix

| Feature / Capability | Us | Competitor A | Competitor B | Competitor C |
|---------------------|----|-------------|-------------|-------------|
| **Core Capabilities** | | | | |
| Feature 1 | ✅ | ✅ | ✅ | ❌ |
| Feature 2 | ✅ | ✅ | ❌ | ✅ |
| **Differentiators** | | | | |
| Our Key Feature | ✅ | ❌ | ❌ | ❌ |
| **Deficiencies** | | | | |
| Their Key Feature | ❌ | ✅ | ✅ | ❌ |

✅ = Full support, ⚠️ = Partial, ❌ = Not supported, 🚧 = Beta/announced

Analyze the matrix for: table stakes (must-haves), differentiators (protect and invest), deficiencies (close critical gaps), whitespace (no one has — innovation opportunity).

## Step 4: SWOT Analysis (with cited evidence)

| Category | Focus | Key Questions |
|----------|-------|---------------|
| **Strengths** (Internal) | What we do better | What do we do best? What unique resources do we have? What do customers praise? |
| **Weaknesses** (Internal) | Where we're behind | What do competitors do better? What do customers complain about? What should we avoid? |
| **Opportunities** (External) | Trends to exploit | What market trends can we leverage? What competitor weaknesses to exploit? What adjacent markets? |
| **Threats** (External) | Risks to watch | What competitor moves could hurt us? What market/regulatory shifts? Platform risk? |

Every cell must have cited evidence. Be honest about weaknesses — sugarcoating helps no one.

## Step 5: Apply Strategic Frameworks

Choose one or more based on your needs:

### Porter's Five Forces

| Force | Assess |
|-------|--------|
| Threat of new entrants | Barriers: capital requirements, network effects, regulation, brand |
| Supplier power | Dependence on key suppliers/platforms |
| Buyer power | Switching costs, buyer concentration, price sensitivity |
| Threat of substitutes | Alternative approaches to the same need |
| Industry rivalry | Number of competitors, growth rate, differentiation |

### Strategic Group Map

Plot competitors on two market-relevant dimensions (e.g., price vs. features, breadth vs. depth, self-serve vs. high-touch) to identify clusters and whitespace.

### Wardley Map

Map your value chain by evolution stage: Genesis (unique, innovate here) → Custom Built (emerging, build for advantage) → Product (common, buy don't build) → Commodity (ubiquitous, use services). Focus innovation on the left side; outsource components moving right.

## Step 6: Identify Whitespace and Threats

**Whitespace Opportunities:** features no one has that users request, segments no one serves, use cases no one addresses well, unserved price points or geographies.

**Threats to Monitor:** competitors closing your differentiation gap, entering your core segments, or undercutting pricing; platform risk (Apple/Google/Microsoft building your feature); open-source alternatives; new entrants with different approaches.

## Step 7: Extract Insights and Recommendations

Save to: `docs/product-superpowers/competitive-analysis/YYYY-MM-DD-<market>.md`

```markdown
# Competitive Analysis — [Market] — [Date]

## Executive Summary (3–5 key findings)
## Competitive Landscape
## Feature Comparison Matrix
## SWOT Analysis
## Strategic Insights
  - Start doing: [actions based on competitor weakness or market opportunity]
  - Stop doing: [activities where competitors have made us irrelevant]
  - Continue doing: [what's working, protect it]
  - Watch: [trends, competitors, market shifts to monitor]
## Next Review (quarterly or triggered by market event)
```

## Step 8: Maintenance Cadence

| Trigger | Action |
|---------|--------|
| **Quarterly** | Full competitive landscape review |
| **Competitor launches major feature** | Spot analysis |
| **Competitor raises funding / changes pricing** | Assess trajectory and threat level |
| **New competitor enters** | Add to landscape, assess threat |
| **Major win or loss to competitor** | Win/loss analysis interview |

## Key Principles

- **Evidence over intuition** — Every claim about a competitor should be sourced.
- **Honesty over comfort** — Acknowledge where competitors are better than you.
- **Action over observation** — Analysis that doesn't change decisions is wasted effort.
- **Customer perspective** — What matters is what customers think, not what you think.
- **Continuous, not periodic** — Landscape shifts constantly. Monitor continuously.
- **Respect competitors** — Dismissing them blinds you to real threats.

## Common Mistakes

- Competitor obsession (copying features instead of solving user problems)
- Confirmation bias (only seeing data that confirms you're better)
- Analysis paralysis (researching forever, never acting)
- Ignoring indirect competitors and substitutes (they hurt you differently)
- Focusing only on features (pricing, positioning, brand, distribution matter too)
- Dismissing smaller competitors (today's startup is tomorrow's threat)
- Not updating the analysis (a year-old analysis is worse than none)

## Key References

- Porter's Five Forces (Michael Porter, "Competitive Strategy")
- "7 Powers" by Hamilton Helmer (foundations of business strategy)
- "Playing to Win" by A.G. Lafley and Roger Martin
- "Obviously Awesome" by April Dunford (product positioning)
- "Blue Ocean Strategy" by W. Chan Kim and Renée Mauborgne
- Simon Wardley's Wardley Mapping
