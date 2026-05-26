---
name: launch-planning
description: Use when planning a product or feature launch and preparing go-to-market execution.
---

# Launch Planning

Plan and execute successful product launches using staged rollouts, feature flags, beta programs, and go-to-market strategy.

**Announce at start:** "I'm using the launch-planning skill to plan the launch for [feature/product]."

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

| Question | Example Answer |
|----------|---------------|
| Primary success metric | Feature adopted by 30% of target users within 30 days |
| Secondary metrics | NPS increases 5 points, support tickets stay below 50/week |
| Counter metrics (guardrails) | Core flow conversion does not decrease, crash rate below 0.1% |
| Evaluation timeframe | 30 days post-launch, with 7/14/30-day checkpoints |

## Step 2: Define Target Audience and Launch Segments

| Segment | Who | % of Users | When |
|---------|-----|-----------|------|
| Internal alpha | Company employees | 100% of employees | 4 weeks before launch |
| Closed beta | Invited power users (50) | <1% | 2–3 weeks before launch |
| Phase 1 rollout | New users (low risk) | 5% | Launch day |
| Phase 2 rollout | All users in primary region | 25% | Launch + 3 days |
| Phase 3 rollout | All users | 100% | Launch + 7 days |

**User communication plan:**

| Touchpoint | Timing | Channel | Message |
|------------|--------|---------|---------|
| Beta invite | 3 weeks before | Email | "You're invited to try our new..." |
| Coming soon | 1 week before | In-app banner | "A new way to [benefit] is coming" |
| Launch | Launch day | Email, blog, social | "Introducing [feature] — now you can..." |
| Follow-up | Launch + 7 days | In-app tooltip | "Have you tried [feature] yet?" |

## Step 3: Plan the Go-to-Market Strategy

| Element | Key Questions |
|---------|--------------|
| **Pricing** | Free? Premium add-on? Included in existing plan? New tier? |
| **Positioning** | How do we describe this against competitors? One-sentence value prop? |
| **Channels** | In-app, email, blog, social, PR, paid ads, events? |
| **Sales enablement** | Do sales teams need training? Pitch decks? Battle cards? |
| **Support readiness** | Is support trained? Help docs ready? Expected ticket volume? |
| **Legal/compliance** | Regulatory approvals? Terms of service updates? Privacy review? |

**Messaging framework:** For [target audience] who [have this problem], [product/feature] is a [category] that [key benefit]. Unlike [alternatives], our product [unique differentiator].

## Step 4: Pre-Launch Checklist

**4–8 Weeks Before:**
- [ ] Launch goals and success metrics defined; target segments identified
- [ ] Messaging and positioning finalized
- [ ] Marketing collateral created: landing page, blog post draft, email sequence, social posts, screenshots/GIFs, help docs and FAQs
- [ ] Sales enablement materials prepared; support team trained
- [ ] Analytics and tracking instrumented; monitoring dashboard created
- [ ] Rollback plan defined and tested; legal/compliance review completed
- [ ] Internal announcement ready; beta program recruitment started

**1 Week Before:**
- [ ] Feature flags configured and tested; all environments verified (staging, production)
- [ ] Load testing completed; war room schedule set (who's on call)
- [ ] Communication channels set up (Slack, incident response)
- [ ] Final stakeholder sign-off obtained; launch day runbook written

## Step 5: Design the Beta Program

| Type | Users | Purpose | Duration |
|------|-------|---------|----------|
| **Internal Alpha** | Company employees | Dogfooding, catch obvious bugs | 1–2 weeks |
| **Closed Beta** | Invited customers (20–200) | Controlled testing, deep feedback | 2–4 weeks |
| **Open Beta** | Anyone who opts in | Scale testing, broad feedback | 2–8 weeks |

**Feedback collection:** in-app widget, NPS/CSAT surveys after key actions, 5–10 beta user interviews, analytics on actual behavior. Triage feedback as bug / UX issue / feature request / confusion.

**Beta success criteria:** X% of beta users try the feature, Y% continue using it after first try, critical bugs resolved, NPS at or above product average, support load within expected range, no showstopper issues.

## Step 6: Choose Rollout Strategy

| Strategy | How It Works | Best For | Risk |
|----------|-------------|----------|------|
| **Phased/Staged** | 1% → 5% → 25% → 50% → 100% | Most features | Low |
| **Feature Flags** | Toggle on/off per user segment | Everything (recommended) | Lowest |
| **Canary** | Route % of traffic to new version | Backend changes, API updates | Low |
| **Blue-Green** | Switch between two environments | Infrastructure changes | Low |
| **Big Bang** | Everyone at once | Urgent fixes, compliance | High |

**Feature flag types:** release toggle (who sees it), experiment toggle (A/B test), ops toggle (kill switch), permission toggle (entitlement-based access).

**Staged rollout schedule:**

| Phase | % of Users | Duration | Gate |
|-------|-----------|----------|------|
| 1 | 1% | 1–2 hours | Error rate < 0.1%, no critical bugs |
| 2 | 5% | 24 hours | Metrics stable, adoption positive |
| 3 | 25% | 48 hours | Support tickets within range |
| 4 | 50% | 24 hours | All systems nominal |
| 5 | 100% | — | Launch complete |

## Step 7: Launch Week Checklist

**Launch Day:** Deploy to production (or flip feature flags). Activate marketing: announcement email, blog post, social media, in-app messaging. War room active (monitor metrics, errors, support). Internal announcement sent. Sales/support notified.

**Launch Week:** Daily standup with launch team. Monitor dashboards continuously first 48 hours. Triage incoming bugs and feedback. Fix critical issues immediately. Adjust messaging if adoption is low. Escalate blockers to leadership.

## Step 8: Post-Launch Checklist

| Checkpoint | Verify |
|------------|--------|
| **24-hour** | Error rates normal? Core metrics stable? Support tickets within expected range? |
| **48-hour** | Adoption tracking toward target? User feedback trending positive? Unexpected usage patterns? |
| **1-week** | Which segments adopting fastest? Retention/repeat use healthy? UX issues emerging? |
| **2-week** | Deep dive by persona/plan/region. Interview 5–10 adopters AND 5–10 non-adopters. |
| **30-day retrospective** | Hit primary metric? What surprised us? What would we do differently? What's the next iteration? |
| **90-day health check** | Feature being retained or was it novelty? Driving expected outcomes? Invest more, maintain, or deprecate? |

## Step 9: Define Kill Criteria

**Roll back** (immediate) if: error rate exceeds X%, core conversion drops >Y%, data loss/security incident, critical P0 bug affecting >Z% of users.

**Consider deprecation** if: adoption below X% at 30 days, feature retention below Y% at 60 days, maintenance cost exceeds value, user satisfaction significantly lower.

## Key Principles

- **Decouple deployment from release** — Use feature flags. Ship code anytime, release when ready.
- **Launch is a process, not a moment** — Pre-launch starts weeks before. Post-launch continues months.
- **Progressive exposure** — Start small, monitor, expand. Never 100% at once unless forced.
- **Kill criteria before launch** — Know what "failure" looks like before you ship.
- **War room discipline** — During launch, monitoring is someone's full-time job.
- **Close the feedback loop** — Tell beta users what you changed because of their input.
- **Launch retrospective** — Always. Every launch. No exceptions.

## Common Mistakes

- No defined success metrics ("we'll know it's successful when we see it")
- Launching to 100% on day one without staged rollout
- No rollback plan; analytics not instrumented before launch
- Support team not trained; no war room (everyone assumes someone else is watching)
- Feature flags left in code forever (flag debt)
- Marketing launches before the feature is actually available to users
- Ignoring early feedback; no kill criteria (zombie features accumulate)

## Key References

- LaunchDarkly feature management and feature flag best practices
- "Loved" by Martina Lauchengco (product marketing)
- "Obviously Awesome" by April Dunford (product positioning)
- "Product-Led Growth" by Wes Bush
