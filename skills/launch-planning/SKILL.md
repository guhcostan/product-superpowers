---
name: launch-planning
description: Use when planning a product or feature launch. Covers go-to-market strategy, launch checklists, beta management, rollout strategies, and post-launch monitoring.
---

# Launch Planning

Plan and execute successful product launches. From pre-launch preparation through post-launch monitoring. Covers beta programs, rollout strategies, feature flags, and launch retrospectives.

**Announce at start:** "I'm using the launch-planning skill to plan the launch for [feature/product]."

## Skill Type

**Flexible** — Adapt checklists to your launch scale. Smaller features can skip heavy GTM. All launches need the pre/during/post structure.

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Define launch goals and success criteria** — What does success look like?
2. **Define target audience and launch segments** — Who gets this, and in what order?
3. **Plan the go-to-market strategy** — Pricing, positioning, channels, messaging
4. **Complete the Pre-Launch Checklist** — Everything that must happen before launch
5. **Design the beta program** — Who tests early, how do we collect feedback?
6. **Choose rollout strategy** — Phased? Feature flags? Canary? All at once?
7. **Complete the Launch Week Checklist** — What happens during launch
8. **Complete the Post-Launch Checklist** — Monitoring and iteration after launch
9. **Define kill criteria** — When do we roll back or deprecate?

## Step 1: Define Launch Goals and Success Criteria

Answer before anything else: "When the launch is over, how do we know it worked?"

| Question | Example Answer |
|----------|---------------|
| Primary success metric | Feature adopted by 30% of target users within 30 days |
| Secondary metrics | NPS increases by 5 points, support tickets stay below 50/week |
| Counter metrics (guardrails) | Core flow conversion does not decrease, app crash rate stays below 0.1% |
| Timeframe for evaluation | 30 days post-launch, with 7/14/30-day checkpoints |

## Step 2: Define Target Audience and Launch Segments

Who gets access, and when?

### Segment Definition

| Segment | Who | % of Users | When |
|---------|-----|-----------|------|
| Internal alpha | Company employees | 100% of employees | 4 weeks before launch |
| Closed beta | 50 invited power users | <1% | 2-3 weeks before launch |
| Staged rollout — Phase 1 | New users (low risk) | 5% | Launch day |
| Staged rollout — Phase 2 | All users in US | 25% | Launch + 3 days |
| Staged rollout — Phase 3 | All users | 100% | Launch + 7 days |

### User Communication Plan

| Touchpoint | Timing | Channel | Message |
|------------|--------|---------|---------|
| Beta invite | 3 weeks before | Email | "You're invited to try our new..." |
| Coming soon | 1 week before | In-app banner | "A new way to [benefit] is coming" |
| Launch announcement | Launch day | Email, blog, social | "Introducing [feature] — now you can..." |
| Follow-up | Launch + 7 days | In-app tooltip | "Have you tried [feature] yet?" |

## Step 3: Plan the Go-to-Market Strategy

### GTM Elements

| Element | Key Questions |
|---------|--------------|
| **Pricing** | Free? Premium add-on? Included in existing plan? New tier? |
| **Positioning** | How do we describe this against competitors? What's the one-sentence value prop? |
| **Channels** | Where will we promote this? (in-app, email, blog, social, PR, paid ads, events) |
| **Sales enablement** | Do sales teams need training? Pitch decks? Battle cards? |
| **Support readiness** | Is support trained? Are help docs ready? Expected ticket volume? |
| **Legal/compliance** | Any regulatory approvals? Terms of service updates? Privacy review? |

### Launch Messaging Framework

```
For [target audience]
Who [have this problem]
[Product/feature name] is a [category]
That [key benefit]
Unlike [alternatives]
Our product [unique differentiator]
```

## Step 4: Pre-Launch Checklist

### 4-8 Weeks Before Launch

- [ ] Launch goals and success metrics defined
- [ ] Target audience and segments identified
- [ ] Messaging and positioning finalized
- [ ] Marketing collateral created:
  - [ ] Landing page
  - [ ] Blog post draft
  - [ ] Email sequence (announcement, follow-up, re-engagement)
  - [ ] Social media posts
  - [ ] Product screenshots/screen recordings/GIFs
  - [ ] Help documentation and FAQs
- [ ] Sales enablement materials prepared (pitch deck, one-pager, battle cards)
- [ ] Support team trained on the feature
- [ ] Analytics and tracking instrumented (all success metrics measurable)
- [ ] Monitoring dashboard created (adoption, errors, performance, support tickets)
- [ ] Rollback plan defined and tested
- [ ] Legal and compliance review completed
- [ ] Internal company announcement ready
- [ ] Beta program designed and recruitment started

### 1 Week Before

- [ ] Feature flags configured and tested
- [ ] All environments verified (staging, production)
- [ ] Load testing completed (if applicable)
- [ ] War room schedule set (who's on call during launch)
- [ ] Communication channels set up (Slack channel, incident response)
- [ ] Final stakeholder sign-off obtained
- [ ] Launch day runbook written (who does what, in what order)

## Step 5: Design the Beta Program

### Beta Types

| Type | Users | Purpose | Duration |
|------|-------|---------|----------|
| **Internal Alpha** | Company employees | Dogfooding, catch obvious bugs | 1-2 weeks |
| **Closed Beta** | Invited customers (20-200) | Controlled testing, deep feedback | 2-4 weeks |
| **Open Beta** | Anyone who opts in | Scale testing, broad feedback | 2-8 weeks |

### Beta Feedback Collection

- **In-app feedback**: Widget or button for quick reactions
- **Surveys**: Short NPS or CSAT after key actions
- **Interviews**: 5-10 beta users for in-depth conversations
- **Analytics**: Track what beta users actually do (not just what they say)
- **Feedback triage**: Categorize as bug / UX issue / feature request / confusion

### Beta Success Criteria

- [ ] X% of beta users try the feature
- [ ] Y% of those continue using it after first try
- [ ] Critical bugs resolved (P0/P1 fixed)
- [ ] NPS from beta users is at or above product average
- [ ] Support load is within expected range
- [ ] No showstopper issues remain

## Step 6: Choose Rollout Strategy

### Rollout Options

| Strategy | How It Works | Best For | Risk Level |
|----------|-------------|----------|-----------|
| **Phased/Staged** | 1% → 5% → 25% → 50% → 100% | Most features | Low |
| **Feature Flags** | Toggle on/off per user segment | Everything (recommended) | Lowest |
| **Canary** | Route % of traffic to new version | Backend changes, API updates | Low |
| **Blue-Green** | Switch between two environments | Infrastructure changes | Low |
| **Big Bang** | Everyone at once | Urgent fixes, compliance | High |

### Feature Flag Strategy (Recommended)

Types of flags to use:

| Flag Type | Purpose | Example |
|-----------|---------|---------|
| **Release toggle** | Control who sees the feature | `new-onboarding-enabled` |
| **Experiment toggle** | A/B test variants | `onboarding-variant-a` |
| **Ops toggle** | Kill switch for emergencies | `recommendations-engine-kill` |
| **Permission toggle** | Entitlement-based access | `premium-analytics-access` |

### Staged Rollout Schedule

| Phase | % of Users | Duration | Check Before Proceeding |
|-------|-----------|----------|------------------------|
| 1 | 1% | 1-2 hours | Error rate < 0.1%, no critical bugs |
| 2 | 5% | 24 hours | Metrics stable, adoption positive |
| 3 | 25% | 48 hours | Support tickets within range, metrics healthy |
| 4 | 50% | 24 hours | All systems nominal |
| 5 | 100% | — | Launch complete |

## Step 7: Launch Week Checklist

### Launch Day

- [ ] Deploy to production (or flip feature flags)
- [ ] Activate marketing campaigns:
  - [ ] Send announcement email
  - [ ] Publish blog post
  - [ ] Post on social media
  - [ ] Update in-app messaging
- [ ] War room active (monitor metrics, errors, support tickets)
- [ ] Internal announcement sent
- [ ] Sales/support notified of go-live

### Launch Week

- [ ] Daily standup with launch team
- [ ] Monitor dashboards continuously first 48 hours
- [ ] Triage incoming bugs and feedback
- [ ] Fix critical issues immediately
- [ ] Adjust messaging if adoption is lower than expected
- [ ] Escalate blockers to leadership

## Step 8: Post-Launch Checklist

### 24-Hour Check

- [ ] Error rates normal?
- [ ] Core metrics stable (no regressions)?
- [ ] Support tickets within expected range?

### 48-Hour Check

- [ ] Adoption tracking toward target?
- [ ] User feedback trending positive or negative?
- [ ] Any unexpected usage patterns?

### 1-Week Check

- [ ] Adoption patterns emerging? Which segments are adopting fastest?
- [ ] Does the feature work for users who adopted? (retention, repeat use)
- [ ] Any UX issues or confusion emerging from user feedback?
- [ ] Adjustments needed to messaging or onboarding?

### 2-Week Check

- [ ] Deep dive into user behavior. Segment by persona, plan, region.
- [ ] Interview 5-10 users who adopted AND 5-10 who didn't.
- [ ] Prepare findings for stakeholder update.

### 30-Day Retrospective

- [ ] Did we hit our primary success metric?
- [ ] What surprised us (positive and negative)?
- [ ] What would we do differently on the next launch?
- [ ] What did we learn about our users?
- [ ] What's the next iteration?

### 90-Day Health Check

- [ ] Is the feature being retained? Or was it novelty?
- [ ] Is it driving the business outcomes we expected?
- [ ] Should we invest more, maintain, or consider deprecation?

## Step 9: Define Kill Criteria

Decide in advance when to roll back or deprecate:

### Roll Back Criteria (immediate action required)

- [ ] Error rate exceeds X% (e.g., 1%)
- [ ] Core conversion metric drops by more than Y% (e.g., 5%)
- [ ] Data loss or security incident
- [ ] Critical P0 bug affecting >Z% of users

### Deprecation Criteria (evaluate after launch window)

- [ ] Adoption below X% at 30 days
- [ ] Feature retention below Y% at 60 days
- [ ] Maintenance cost exceeds value delivered
- [ ] User satisfaction (NPS/CSAT) significantly lower for feature users

## Key Principles

- **Decouple deployment from release** — Use feature flags. Ship code anytime, release when ready.
- **Launch is a process, not a moment** — Pre-launch starts weeks before. Post-launch continues for months.
- **Progressive exposure** — Start small, monitor, expand. Never 100% at once unless forced.
- **Kill criteria before launch** — Know what "failure" looks like before you ship.
- **War room discipline** — During launch, monitoring is someone's full-time job.
- **Close the feedback loop** — Tell beta users and early adopters what you changed because of their input.
- **Launch retrospective** — Always. Every launch. No exceptions.

## Common Pitfalls

- No defined success metrics ("we'll know if it's successful when we see it")
- Launching to 100% on day one without staged rollout
- No rollback plan ("we're sure it will work")
- Analytics not instrumented before launch (can't measure what you didn't track)
- Support team not trained (drowning in tickets they can't answer)
- No war room (everyone assumes someone else is watching)
- Feature flags left in code forever (flag debt)
- Marketing launches before the feature is actually available to users
- Ignoring early feedback because "the metrics will catch up"
- No kill criteria (keeping features that don't work because no one decided to deprecate)

## Key References

- LaunchDarkly feature management and feature flag best practices
- "Loved" by Martina Lauchengco (SVPG book on product marketing)
- "Obviously Awesome" by April Dunford (product positioning)
- "Product-Led Growth" by Wes Bush
- ProductPlan GTM Strategy templates
