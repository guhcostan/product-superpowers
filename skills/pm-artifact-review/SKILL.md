---
name: pm-artifact-review
description: Use when completing PM artifacts (PRDs, user stories, roadmaps) or before sharing with stakeholders to verify quality and completeness
---

# PM Artifact Review

Dispatch a PM reviewer subagent to catch gaps and quality issues in PM artifacts before they reach engineering, stakeholders, or leadership. The reviewer gets precisely crafted context — never your session history.

**Core principle:** Review PM artifacts before they cascade into commitments. A flawed PRD costs 10x more to fix after engineering starts.

**Announce at start:** "I'm using the pm-artifact-review skill to review [artifact type]."

## When to Request Review

**Mandatory:**
- After completing a PRD (before user story breakdown)
- After completing user stories (before sprint planning)
- After completing a roadmap (before stakeholder presentation)
- After completing a discovery doc (before PRD)

**Optional but valuable:**
- When the artifact is strategically critical
- When multiple stakeholders will commit resources based on it
- When you want a fresh perspective before an executive review

## The Process

### Step 1: Identify What to Review

Ready to review:
- PRD: Check against Amazon PR/FAQ format, discovery findings, and PM quality standards
- User Stories: Check INVEST criteria, acceptance criteria format, edge case coverage
- Roadmap: Check outcome-based structure, Now/Next/Later format, OKR alignment
- Discovery Doc: Check completeness of opportunity assessment, research evidence, JTBD mapping

### Step 2: Dispatch PM Reviewer Subagent

Use the template at `pm-artifact-review/artifact-reviewer-prompt.md`.

Fill these placeholders:
- `{DESCRIPTION}` — Brief summary of the artifact (e.g., "PRD for onboarding redesign")
- `{PLAN_OR_REQUIREMENTS}` — What it should address (discovery doc path, or requirements list)
- `{ARTIFACT_CONTENT_OR_PATH}` — Full path to the artifact file

### Step 3: Act on Feedback

- Fix Critical issues immediately — these block progress
- Fix Important issues before proceeding to next step
- Note Minor issues for later polish
- If the reviewer found gaps in the underlying spec/discovery, go back and fix those first

## Two-Stage Review

The reviewer checks two dimensions:

**Stage 1 — Spec Compliance**
Does the artifact follow the required format and cover all required sections?

**Stage 2 — PM Quality**
Is the thinking sound? Are there gaps in problem clarity, metrics, scope, user centricity, or executability?

Always complete Stage 1 before Stage 2. A perfectly written artifact (Stage 2) that misses required sections (Stage 1) still fails review.

## Example

```
You: "PRD complete. Let me review before breaking into stories."

[Review discovery doc to ensure it's current]
[Dispatch PM reviewer subagent]
  DESCRIPTION: PRD for new onboarding flow — aims to improve activation from 40% to 65%
  PLAN_OR_REQUIREMENTS: docs/product-superpowers/discovery/2026-05-20-onboarding.md
  ARTIFACT_CONTENT_OR_PATH: docs/product-superpowers/prds/2026-05-22-onboarding.md

[Subagent returns]:

  Strengths:
  - Strong press release with clear customer benefit
  - Metrics are specific and time-bound

  Issues:
  Critical: (none)
  Important:
  1. Missing FAQ internal question about support team training
  2. Out-of-scope section doesn't mention mobile (will engineering assume it's in scope?)
  3. No accessibility requirements specified
  Minor:
  1. Customer quote could be more specific to target persona

  Assessment: Ready with fixes

You: [Fix Important issues]
You: [Invoke user-story-writing skill]
```

## Red Flags

**Never:**
- Skip review because "it's a simple feature"
- Proceed with unfixed Critical issues
- Forward unreviewed artifacts to stakeholders
- Ignore Important issues — they compound
- Argue with valid PM quality feedback

**If reviewer wrong:**
- Push back with evidence (research data, user quotes, strategy documents)
- Show how the artifact addresses the concern
- Request clarification on what specifically is missing

## Integration with Workflow

**Discovery → PRD pipeline:**
- Review discovery doc before writing PRD
- Review PRD before breaking into stories
- Review stories before sprint planning

**Roadmap work:**
- Review roadmap before presenting to stakeholders

**Strategic artifacts:**
- Review competitive analysis before strategy decisions
- Review strategy doc before roadmap alignment

## Common Mistakes

**Skipping review**: "The PRD is solid, let's just start writing stories"
**Reality**: You're too close to the work. Fresh eyes catch what you missed.

**Review-only at the end**: Reviewing a full PRD + stories + roadmap at once
**Reality**: Review at each stage. Fixing early saves rework.

**Vague review prompt**: "Review this PRD" with no context
**Reality**: Provide the discovery doc, format requirements, and quality standards.

**Ignoring reviewer**: Noting issues but not fixing them
**Reality**: Every ignored Important issue will resurface as a stakeholder or engineering complaint.
