---
name: design-handoff
description: Use when preparing design specifications for engineering handoff and quality assurance.
---

# Design-to-Development Handoff

Prepare comprehensive design specifications for engineering. Ensure design fidelity by documenting all states, tokens, interactions, edge cases, and accessibility requirements.

**Announce at start:** "I'm using the design-handoff skill to prepare specifications for development."

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Audit design states** — Every component must define all states
2. **Document design tokens** — Colors, typography, spacing as variables
3. **Specify interactions** — Animations, transitions, gestures
4. **Document accessibility** — ARIA labels, focus order, contrast ratios
5. **Cover edge cases** — Long text, empty states, RTL, viewport extremes
6. **Prepare asset exports** — Icons, images in correct formats
7. **Create design QA checklist** — What to verify after development
8. **Link designs to stories** — Connect Figma files to specific user stories
9. **Review with engineering** — Get feasibility feedback before development starts

## Step 1: Audit Design States

Every interactive component must specify all applicable states. Missing states are the #1 cause of design drift.

| State | When It Applies | What to Specify |
|-------|-----------------|-----------------|
| **Default** | Component at rest | Visual appearance, layout |
| **Hover** | Cursor over element (desktop) | Color shift, underline, scale |
| **Active/Pressed** | Click/tap in progress | Darker color, scale down |
| **Focus** | Keyboard navigation reached element | Focus ring style, offset |
| **Disabled** | Element not interactive | Opacity, cursor, tooltip |
| **Loading** | Data being fetched | Skeleton, spinner, progress bar |
| **Empty** | No data to display | Illustration, message, CTA |
| **Error** | Something went wrong | Error message, retry action |
| **Success** | Action completed | Confirmation, auto-dismiss timing |
| **Read-only** | Data displayed, not editable | Visual distinction from editable |

- [ ] All states designed (not just "default + red border" for errors)
- [ ] Empty state has illustration or guidance
- [ ] Loading state uses skeleton/spinner/progress
- [ ] Focus states visible for keyboard navigation

## Step 2: Document Design Tokens

Document as named variables, never raw hex values. Every visual property should reference a token.

| Category | What to Define |
|----------|---------------|
| **Colors** | Primary, neutral, error, success palettes with tints/shades (e.g. `color-primary-500`, `color-primary-600` for hover) |
| **Typography** | Font family, size scale (heading-lg/md, body, caption), weights, line-heights |
| **Spacing** | Scale in rem (xs: 0.25, sm: 0.5, md: 1, lg: 1.5, xl: 2, 2xl: 3) |
| **Radii** | sm, md, lg, full |
| **Shadows** | sm, md, lg (specify rgba values) |
| **Breakpoints** | mobile (375px), tablet (768px), desktop (1024px), wide (1440px) |

## Step 3: Specify Interactions

Document how things move. Use a consistent animation scale (100ms, 200ms, 300ms).

```
Component: [Name]
Trigger: [What starts the interaction]
Duration: [ms]
Easing: [cubic-bezier or named curve]
Outcome: [What the user sees happen]
```

- [ ] Page transitions, micro-interactions, loading motion all defined
- [ ] Gestures specified for mobile (swipe, pinch, long press)
- [ ] Respect `prefers-reduced-motion`

## Step 4: Document Accessibility

Accessibility is not optional. Document per component:

- [ ] **ARIA labels**: What screen readers announce
- [ ] **Focus order**: Logical tab order through the component
- [ ] **Keyboard navigation**: Full operation without a mouse
- [ ] **Contrast ratios**: WCAG AA (4.5:1 normal text, 3:1 large text)
- [ ] **Screen reader behavior**: Announcements on state changes (errors, loading, dynamic content)
- [ ] **Alt text**: All meaningful images and icons
- [ ] **Form labels**: Every input has an associated label
- [ ] **Error announcements**: `role="alert"`, `aria-live="polite"`
- [ ] **Reduced motion**: Respect user preference

## Step 5: Cover Edge Cases

| Edge Case | What to Specify |
|-----------|----------------|
| **Long text** | Truncation? Line clamping? How does layout handle 3x expected length? |
| **No text** | What shows when a field is empty? |
| **Many items** | 1,000+ items in a list — pagination? Virtual scrolling? |
| **Very long names** | "Hubert Blaine Wolfeschlegelsteinhausenbergerdorff Sr." |
| **RTL languages** | Layout in Arabic, Hebrew |
| **Small viewport** | 320px width |
| **Large viewport** | 2560px width |
| **No internet / slow connection** | Offline state, 5+ second API calls |
| **First-time user** | Before any data exists |
| **Power user** | 10,000+ items, high-frequency usage |
| **Permission-restricted** | Limited permissions view |

## Step 6: Prepare Asset Exports

- [ ] Icons exported as SVG (preferred) or PNG @2x and @3x
- [ ] Illustrations at appropriate resolution
- [ ] Dark mode variants where applicable
- [ ] File naming convention: `icon-name-type@scale.format`
- [ ] Assets organized by component or feature

## Step 7: Design QA Checklist

Create a checklist for reviewing built UI against design:

**Visual Fidelity:** spacing, typography, colors, border radius, shadows, icon sizes match design. No hardcoded hex values.

**Responsive:** Mobile (375px), tablet (768px), desktop (1024px) layouts match. No horizontal overflow at any breakpoint.

**States:** All states implemented (default, hover, focus, active, disabled, loading, empty, error). Loading states have skeleton/spinner. Empty states have illustration + guidance. Error states show actionable messages.

**Interactions:** Animations match specified duration/easing. Transitions are smooth. Gestures work on mobile.

**Accessibility:** Keyboard navigation works. Focus indicators visible. Screen reader announces content correctly. Contrast meets WCAG AA.

**Data Variability:** Layout works with 1 character, 500+ characters, no content, and many items (stress test).

## Step 8: Link Designs to Stories

| User Story | Design File | Version | Status |
|------------|------------|---------|--------|
| Sign up with email | [Figma link] | v3 (approved May 20) | Ready for dev |
| Dashboard overview | [Figma link] | v1 (approved May 22) | Ready for dev |
| Settings page | [Figma link] | v2 (draft May 25) | In review |

## Step 9: Review with Engineering

Before development starts:
- [ ] Engineering has reviewed designs for feasibility
- [ ] Design tokens map to existing CSS variables or code constants
- [ ] Component breakdown aligns with current architecture
- [ ] Complex interactions prototyped and tested
- [ ] Third-party limitations identified (API constraints, library limitations)
- [ ] Performance implications understood (animation cost, asset size)

## Key Principles

- **Design with tokens, not values** — Hex codes become variables. Spacing uses a scale.
- **All states, always** — Missing states = rework. Design every state before handoff.
- **Handoff is a conversation** — Not a one-time documentation dump. Ongoing dialogue.
- **Accessibility is not optional** — Document it explicitly, test it rigorously.
- **Link designs to code** — Every story should know which design version it implements.
- **Design QA is a required step** — Budget time for it. Not optional.

## Common Mistakes

- Missing states in designs (especially error, loading, empty)
- Static designs that don't account for dynamic content lengths
- No design system, leading to inconsistent implementations
- Handoff treated as "throw it over the wall" rather than collaboration
- Hex values instead of design tokens (hard to maintain, hard to theme)
- Accessibility left to engineering to figure out
- Designs not version-linked to code, no design QA process

## Key References

- Brad Frost, "Atomic Design"
- "Design Systems" by Alla Khmelnitsky
- Figma Dev Mode documentation
- Storybook documentation
- WCAG 2.1 Accessibility Guidelines
