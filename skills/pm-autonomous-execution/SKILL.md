---
name: pm-autonomous-execution
description: Use when executing PM plans with independent tasks — dispatches subagent per task with review between each
---

# PM Autonomous Execution

Execute a PM plan by dispatching a fresh subagent per task, with review after each output. Covers discovery, PRDs, user stories, prioritization, and launch plans.

**Core principle:** Fresh subagent per task + review after each = high-quality PM artifacts with minimal context pollution.

**Announce at start:** "I'm using the pm-autonomous-execution skill to execute this plan."

<HARD-GATE>
Do NOT invoke this skill unless you have a written PM plan with defined tasks and acceptance criteria. If no plan exists, invoke the relevant planning skill first.
</HARD-GATE>

## When to Use

**Use when:**
- You have a written plan with 3+ PM tasks (discovery, PRD, stories, etc.)
- Each task produces a self-contained artifact
- Tasks follow a sequence but don't require continuous conversation
- You want agentic execution with quality gates between tasks

**Don't use when:**
- Scope or tasks aren't defined yet
- Work requires continuous user conversation
- Tasks are tightly coupled (output of A is incomplete without B finishing it)
- This is exploratory — you're figuring out the plan as you go

## The Process

```
Read plan → For each task:
  1. Dispatch implementer subagent (produces PM artifact)
  2. Dispatch PM reviewer subagent (reviews quality)
  3. Fix issues → re-review → approve
  4. Mark complete → next task
Present final summary
```

## Step 1: Load Plan

Read the plan file once. Extract all tasks with full text, context, and acceptance criteria. Create TodoWrite with all tasks. Do NOT make subagents read the plan file — provide the text directly.

## Step 2: Execute Each Task

For each task in sequence:

1. **Dispatch implementer subagent** using the template in `pm-autonomous-execution/pm-implementer-prompt.md`. Provide: full task text, scene-setting context, and source documents.

2. **Implementer produces the PM artifact** (PRD, stories, roadmap, etc.). Reports status: DONE, DONE_WITH_CONCERNS, BLOCKED, or NEEDS_CONTEXT. If BLOCKED or NEEDS_CONTEXT, resolve and re-dispatch.

3. **Dispatch PM reviewer subagent** using `pm-artifact-review`. Review against task requirements. Categorize issues.

4. **Implementer fixes issues.** Re-review after fixes.

5. **Mark task complete** once reviewer approves.

## Step 3: Complete

Present summary of all artifacts produced, open issues, and next steps.

## PM Plan Template

```markdown
# [Initiative] — PM Execution Plan

**Goal:** [One sentence outcome]

## Task 1: Product Discovery
**Deliverable:** Discovery doc (JTBD, opportunity assessment, validation)
**Source:** [User interviews, analytics, support tickets]
**Output:** docs/product-superpowers/discovery/YYYY-MM-DD-topic.md

## Task 2: PRD
**Deliverable:** PRD in Amazon PR/FAQ format
**Source:** Task 1 output (discovery doc)
**Output:** docs/product-superpowers/prds/YYYY-MM-DD-feature.md

## Task 3: User Stories
**Deliverable:** INVEST-validated stories with Gherkin ACs
**Source:** Task 2 output (PRD)
**Output:** docs/product-superpowers/stories/YYYY-MM-DD-feature-stories.md

## Task 4: Launch Plan
**Deliverable:** Launch checklist, beta plan, rollout strategy
**Source:** Task 3 output (stories)
**Output:** docs/product-superpowers/launch-plans/YYYY-MM-DD-feature.md
```

## Handling Implementer Status

**DONE:** Proceed to PM review.
**DONE_WITH_CONCERNS:** Read concerns. If minor, proceed to review. If significant, resolve before review.
**NEEDS_CONTEXT:** Provide missing context and re-dispatch.
**BLOCKED:** Assess: context problem → provide more; task too hard → re-dispatch with better model; task too large → split; plan wrong → escalate to user.

## Model Selection

- **Mechanical tasks** (formatting stories, filling PRD sections): fast/cheap model
- **Analysis tasks** (competitive analysis, JTBD mapping): standard model
- **Strategy tasks** (trade-off decisions, PMF assessment): most capable model

## Red Flags

**Never:**
- Skip review between tasks (review gates exist for a reason)
- Proceed with unfixed Critical or Important issues
- Dispatch multiple implementers in parallel (sequential tasks)
- Make subagent read plan file (provide full text)
- Accept "close enough" on review
- Skip review loops (reviewer found issues → fix → review again)

## Integration

**Required skills:**
- `pm-artifact-review` — Review each task's output
- `pm-subagent-orchestration` — Dispatch parallel tasks within a task if applicable

**Can follow:**
- `stakeholder-management` — Present completed plan to stakeholders
- `launch-planning` — Execute launch after plan completion
