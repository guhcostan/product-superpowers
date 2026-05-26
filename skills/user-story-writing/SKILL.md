---
name: user-story-writing
description: Use when you have an approved PRD and need to break it into actionable user stories for development.
---

# Writing User Stories

Break an approved PRD into actionable user stories organized into epics. Each story must satisfy INVEST criteria and include Gherkin-format acceptance criteria with edge cases and error states.

**Announce at start:** "I'm using the user-story-writing skill to break the PRD into user stories."

<HARD-GATE>
Do NOT invoke this skill unless the PRD is approved. If the PRD hasn't been written, invoke writing-prd after product-discovery.
</HARD-GATE>

**Save stories to:** `docs/product-superpowers/stories/YYYY-MM-DD-<feature-name>-stories.md`

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Review the PRD** — Ensure you understand the full scope, metrics, and constraints
2. **Identify epics** — Group related functionality into epics organized by user journey or theme
3. **Write user stories for each epic** — Use the standard format with clear personas
4. **Apply INVEST to every story** — Verify each story meets all criteria
5. **Write acceptance criteria** — Gherkin format (Given-When-Then) for each story
6. **Cover edge cases and error states** — Explicitly document all states
7. **Define Definition of Ready** — What must be true before a story enters a sprint
8. **Prioritize and sequence** — Order stories within and across epics
9. **Save and present for review** — Write to docs, get user approval

## The Process

### Step 1: Review the PRD

Re-read the approved PRD. Note:
- All features and their descriptions
- Success metrics
- Non-functional requirements
- Constraints and dependencies
- What's explicitly out of scope
- User personas mentioned

### Step 2: Identify Epics

Group related user stories into epics. An epic represents a large body of work that delivers a coherent user outcome.

**Epic guidelines:**
- Named after a user outcome, not a technical component
- Contains 3-10 user stories
- Can span multiple sprints but should have a clear finish line
- Each epic should be independently valuable if possible

**Example epic structure:**
```
Epic: New User Onboarding
  └── Story: Sign up with email
  └── Story: Sign up with Google SSO
  └── Story: Complete profile setup
  └── Story: Guided product tour
  └── Story: Skip onboarding entirely

Epic: Core Dashboard
  └── Story: View key metrics at a glance
  └── Story: Filter dashboard by date range
  └── Story: Export dashboard as PDF
  └── Story: Customize dashboard layout
```

### Step 3: Write User Stories

Use the standard format:

```
As a [specific user persona]
I want to [goal or desire]
So that [reason or benefit]
```

**Persona-driven, not role-driven:**
- Good: "As a first-time project manager setting up their team..."
- Bad: "As a user..."

**Goal-focused, not feature-focused:**
- Good: "I want to invite team members by email so that everyone can access the project"
- Bad: "I want an invite button"

**Benefits that connect to outcomes:**
- Good: "...so that I don't have to manually track who has access"
- Bad: "...so that the system records their email"

### Step 4: Apply INVEST Criteria

Verify every story meets all INVEST criteria:

| Criterion | Check | Red Flag |
|-----------|-------|----------|
| **I**ndependent | Can this story be developed independently? | "Depends on [other story] being complete" |
| **N**egotiable | Can details be adjusted during development? | Over-prescribed implementation details |
| **V**aluable | Does this deliver value to users or the business? | Pure technical stories with no user benefit |
| **E**stimable | Can the team roughly estimate the effort? | "We don't know enough to estimate" (needs spike) |
| **S**mall | Can it be completed in one sprint? | "This will take the whole team the entire sprint" (too large, split it) |
| **T**estable | Is there a clear pass/fail condition? | "The user should have a good experience" (vague) |

**Stories that fail INVEST must be rewritten, split, or marked as spikes.**

### Step 5: Write Acceptance Criteria (Gherkin)

For each story, write acceptance criteria in Given-When-Then format:

```gherkin
Given [precondition or context]
When [action or event]
Then [expected outcome]
```

**Examples:**

```gherkin
Story: Sign up with email

Given I am on the sign-up page
When I enter a valid email and password and click "Create Account"
Then I am redirected to the dashboard
And I receive a welcome email
And my account is created in the database

Given I am on the sign-up page
When I enter an email that is already registered and click "Create Account"
Then I see the error message "An account with this email already exists"
And I am shown a link to "Sign in instead"

Given I am on the sign-up page
When I enter an invalid email format and click "Create Account"
Then I see the error message "Please enter a valid email address"
And the form is not submitted

Given I am on the sign-up page
When I enter a password shorter than 8 characters and click "Create Account"
Then I see the error message "Password must be at least 8 characters"
And the password field is highlighted

Given I am on the sign-up page
When I click "Create Account" with all fields empty
Then I see validation errors on all required fields
And the form is not submitted
```

**Acceptance criteria best practices:**
- Write from the user's perspective (what they see, what happens)
- Be specific enough to test, general enough to allow implementation creativity
- Include both happy path AND error/edge cases
- Each scenario is independently testable
- Don't duplicate the story description — criteria define BOUNDARIES
- Use concrete data in examples (realistic names, emails, values)
- Cover all states: default, loading, empty, error, success, edge cases

### Step 6: Cover Edge Cases and Error States

For every user-facing story, document:
- **Data limits**: What happens when the user enters maximum/minimum values?
- **Empty states**: What does the user see when there's no data?
- **Loading states**: What does the user see while data is loading?
- **Slow/failed network**: What happens when the request times out or fails?
- **Concurrent actions**: What happens if the user double-clicks?
- **Accessibility**: What's the keyboard navigation, screen reader experience?
- **Internationalization**: RTL layouts, long text in German, short text in English
- **Permissions**: What do different roles see?

### Step 7: Define Definition of Ready (DoR)

Before a story enters a sprint, it must be:

- [ ] User story is written and follows the format
- [ ] INVEST criteria are met
- [ ] Acceptance criteria are written in Gherkin format
- [ ] Edge cases and error states are documented
- [ ] Design assets are available (if visual)
- [ ] Dependencies are identified and resolved or accepted
- [ ] Team has discussed and understands the story
- [ ] Story is small enough to complete in one sprint
- [ ] Success metrics are linked (if applicable)

### Step 8: Prioritize and Sequence

Order stories considering:
1. **Dependencies** — What must be built first?
2. **User journey** — What's the natural user flow?
3. **Value** — What delivers the most user/business value?
4. **Risk** — What's the riskiest assumption to test?
5. **Learning** — What teaches us the most about whether we're on the right track?

Draw a slicing line for the Minimum Viable Product (MVP):
```
[Must have for launch]
───────────────────── Slicing Line
[Nice to have, can ship later]
```

### Step 9: Save and Present

Document structure:
```markdown
# [Feature Name] — User Stories

**Date:** YYYY-MM-DD
**Based on PRD:** [link to PRD file]
**Status:** Draft / Approved / In Progress

## Epic 1: [Epic Name]

**Outcome:** [What user outcome does this epic deliver?]

### Story 1.1: [Story Title]

**As a** [persona]
**I want to** [goal]
**So that** [benefit]

**Priority:** Must Have / Should Have / Could Have
**Estimate:** [Story Points / T-shirt size]
**Dependencies:** [List any]

**Acceptance Criteria:**
[Gherkin scenarios]

**Edge Cases:**
[List]

**Definition of Ready:**
[Checklist items specific to this story]

---

### Story 1.2: [Story Title]
...

## Epic 2: [Epic Name]
...

## Story Map (Visual)
[ASCII or describe the story map: user journey horizontal, priority vertical]

## MVP Scope
[What's above the slicing line]
```

## User Review Gate

After completing all stories:

> "User stories written and saved to `docs/product-superpowers/stories/<filename>.md`. The document includes [N] epics with [M] stories, INVEST-validated with Gherkin acceptance criteria. Please review and let me know if you want changes."

## Key Principles

- **Stories are placeholders for conversations** — They capture intent, not every detail. Details emerge during development.
- **Acceptance criteria define DONE** — If it passes the ACs, it's done. If not, it's not.
- **INVEST is a quality gate** — Stories that fail INVEST don't enter sprints.
- **Small stories > big stories** — Split until each fits in a sprint (ideally a few days).
- **Stories deliver user value** — If a story doesn't deliver value to a user or the business, it's probably a task, not a story.
- **Every state must be designed** — Default, hover, active, focus, disabled, loading, empty, error, success.

## Common Mistakes

- Writing stories that are too large (epic disguised as story)
- Stories without clear acceptance criteria ("I'll know it when I see it")
- Technical stories disguised as user stories ("As a developer, I want to refactor the database")
- Stories that depend on other stories (fails Independent in INVEST)
- Acceptance criteria that dictate implementation ("Use a dropdown component")
- No error states or edge cases documented
- Personas that are too generic ("As a user...")
- Stories without a clear benefit clause ("So that..." is missing or vague)

## Key References

- "User Story Mapping" by Jeff Patton
- Atlassian's Agile guides on user stories
- "Essential Scrum" by Kenneth Rubin
- INVEST criteria (originated by Bill Wake)
- Gherkin/Cucumber specification format
