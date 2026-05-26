---
name: design-handoff
description: Use when preparing design specifications for engineering handoff and quality assurance.
---

# Design-to-Development Handoff

Prepare comprehensive design specifications for engineering. Ensure design fidelity by documenting all states, tokens, interactions, edge cases, and accessibility requirements.

**Announce at start:** "I'm using the design-handoff skill to prepare specifications for development."

## What is the Design Handoff?

The handoff is the process of transferring design specifications, assets, and interaction guidelines from design to development. It marks the transition from "what should we build?" to "how do we build it?"

```
Discovery → Design → Prototype → Handoff → Development → QA → Ship
                                  ^^^
                          This is the critical junction
```

A poor handoff leads to rework, design drift, and user-facing quality issues. A good handoff makes development fast and the final product faithful to the design intent.

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

### States to Document

| State | When it Applies | What to Specify |
|-------|-----------------|-----------------|
| **Default** | Component at rest, no interaction | Visual appearance, layout |
| **Hover** | Cursor over element (desktop) | Color shift, underline, scale change |
| **Active/Pressed** | Click/tap in progress | Darker color, scale down |
| **Focus** | Keyboard navigation reached element | Focus ring style, offset |
| **Disabled** | Element not interactive | Opacity, cursor, tooltip explaining why |
| **Loading** | Data being fetched or processed | Skeleton, spinner, progress bar |
| **Empty** | No data to display | Illustration, message, call to action |
| **Error** | Something went wrong | Error message, retry action, visual treatment |
| **Success** | Action completed successfully | Confirmation, checkmark, auto-dismiss timing |
| **Read-only** | Data displayed but not editable | Visual distinction from editable fields |

**State audit table example:**

| Component | Default | Hover | Active | Focus | Disabled | Loading | Empty | Error |
|-----------|---------|-------|--------|-------|----------|---------|-------|-------|
| Button | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | — | — |
| Input Field | ✅ | ✅ | ✅ | ✅ | ✅ | — | — | ✅ |
| Data Table | ✅ | — | — | — | — | ✅ | ✅ | ✅ |
| Dropdown | ✅ | ✅ | ✅ | ✅ | ✅ | — | — | — |

### States Checklist
- [ ] Default state designed for every component
- [ ] Error state designed (not just "default + red border")
- [ ] Empty state designed with illustration or guidance
- [ ] Loading state designed (skeleton, spinner, or progress)
- [ ] Disabled state clearly distinguishable from default
- [ ] Focus states visible for keyboard navigation

## Step 2: Document Design Tokens

Design tokens are platform-agnostic style values that map to code variables. They enable consistency and make theme changes safe.

### Token Categories

**Colors:**
```
color-primary-500: #3B82F6
color-primary-600: #2563EB (hover/active)
color-neutral-100: #F3F4F6 (background)
color-neutral-900: #111827 (text primary)
color-error-500: #EF4444
color-success-500: #22C55E
```

**Typography:**
```
font-family-primary: "Inter", sans-serif
font-size-heading-lg: 32px / 2rem
font-size-heading-md: 24px / 1.5rem
font-size-body: 16px / 1rem
font-size-caption: 12px / 0.75rem
font-weight-regular: 400
font-weight-bold: 700
line-height-body: 1.5
```

**Spacing (use a scale):**
```
spacing-xs: 4px / 0.25rem
spacing-sm: 8px / 0.5rem
spacing-md: 16px / 1rem
spacing-lg: 24px / 1.5rem
spacing-xl: 32px / 2rem
spacing-2xl: 48px / 3rem
```

**Radii, Shadows, Breakpoints:**
```
radius-sm: 4px
radius-md: 8px
radius-lg: 12px
radius-full: 9999px

shadow-sm: 0 1px 2px rgba(0,0,0,0.05)
shadow-md: 0 4px 6px rgba(0,0,0,0.1)

breakpoint-mobile: 375px
breakpoint-tablet: 768px
breakpoint-desktop: 1024px
breakpoint-wide: 1440px
```

Never hand off hex values inline. Everything should reference tokens.

## Step 3: Specify Interactions

Document how things move, not just how they look.

### Interaction Specification Format

```
Component: [Name]
Trigger: [What starts the interaction]
Duration: [How long it takes]
Easing: [Acceleration curve]
Outcome: [What the user sees happen]
```

**Example — Dropdown Menu:**
```
Component: Navigation dropdown
Trigger: Click on menu item
Duration: 200ms
Easing: ease-out (cubic-bezier(0, 0, 0.2, 1))
Outcome: Menu slides down from trigger, opacity 0→1, translateY -4px→0
```

**Interaction checklist:**
- [ ] Page transitions defined
- [ ] Micro-interactions documented (button press, toggle, hover)
- [ ] Loading states have motion (not static spinners)
- [ ] Gestures specified for mobile (swipe, pinch, long press)
- [ ] Animation durations are consistent (use a scale: 100ms, 200ms, 300ms)

## Step 4: Document Accessibility

Accessibility is not optional. Document requirements explicitly.

### Accessibility Checklist per Component

- [ ] **ARIA labels**: What screen readers announce
- [ ] **Focus order**: Logical tab order through the component
- [ ] **Keyboard navigation**: Can the component be fully operated with a keyboard?
- [ ] **Contrast ratios**: Text meets WCAG AA (4.5:1 normal, 3:1 large text)
- [ ] **Screen reader behavior**: What is announced on state changes (errors, loading, dynamic content)
- [ ] **Alt text**: For all images and icons that convey meaning
- [ ] **Form labels**: Every input has an associated label
- [ ] **Error announcements**: Error messages are announced to screen readers
- [ ] **Reduced motion**: Respect `prefers-reduced-motion` for animations

### Accessibility Notes Format

```markdown
### Component: Signup Form

**Focus Order:**
1. Email input
2. Password input
3. Confirm password input
4. "Show password" toggle
5. Submit button
6. "Sign in instead" link

**ARIA:**
- Email input: aria-label="Email address", aria-required="true"
- Error message container: role="alert", aria-live="polite"

**Keyboard:**
- Tab through fields
- Enter to submit
- Space to toggle password visibility
- Escape to dismiss validation errors
```

## Step 5: Cover Edge Cases

Designs that look perfect with ideal data break in the real world.

### Edge Cases to Document

| Edge Case | What to Specify |
|-----------|----------------|
| **Long text** | How does the layout handle text 3x longer than the design? Truncation? Line clamping? |
| **No text** | What if a field is empty when you expected content? |
| **Many items** | What happens with 1,000 items in a list? Pagination? Virtual scrolling? |
| **Very long names** | How does the UI handle "Hubert Blaine Wolfeschlegelsteinhausenbergerdorff Sr."? |
| **RTL languages** | What does the layout look like in Arabic, Hebrew? |
| **Small viewport** | What does the UI look like at 320px width? |
| **Large viewport** | What does the UI look like at 2560px width? |
| **No internet** | What happens when the user is offline? |
| **Slow connection** | What happens during a 5+ second API call? |
| **First-time user** | What does a new user see before any data exists? |
| **Power user** | What does a user with 10,000+ items see? |
| **Permission-restricted** | What does a user with limited permissions see? |

## Step 6: Prepare Asset Exports

### Image/Icon Checklist

- [ ] Icons exported as SVG (preferred) or PNG @2x and @3x
- [ ] Illustrations exported at appropriate resolution
- [ ] Favicon and social sharing images provided
- [ ] File naming follows convention: `icon-name-type@scale.format`
- [ ] All assets organized by component or feature
- [ ] Dark mode variants provided where applicable

## Step 7: Design QA Checklist

Create a checklist for reviewing the built UI against design:

```markdown
## Design QA — [Feature Name]

### Visual Fidelity
- [ ] Spacing matches design (check padding, margins, gaps)
- [ ] Typography matches (font, size, weight, line-height, letter-spacing)
- [ ] Colors match design tokens (not hardcoded hex values)
- [ ] Border radius, shadows match
- [ ] Icon sizes and alignment match

### Responsive
- [ ] Mobile layout matches at 375px
- [ ] Tablet layout matches at 768px
- [ ] Desktop layout matches at 1024px
- [ ] No horizontal overflow at any breakpoint

### States Verify
- [ ] All states implemented (default, hover, focus, active, disabled, loading, empty, error)
- [ ] Loading states show appropriate skeleton/spinner
- [ ] Empty states show illustration and guidance
- [ ] Error states show actionable messages

### Interactions
- [ ] Animations match specified duration and easing
- [ ] Hover/active transitions are smooth (no jarring changes)
- [ ] Gestures work on mobile

### Accessibility
- [ ] Keyboard navigation works (Tab, Enter, Escape, Arrow keys)
- [ ] Focus indicators visible
- [ ] Screen reader announces content correctly
- [ ] Contrast meets WCAG AA minimum

### Data Variability
- [ ] Layout works with short content (1 character)
- [ ] Layout works with long content (500+ characters)
- [ ] Layout works with no content (empty state)
- [ ] Layout works with many items (stress test)
```

## Step 8: Link Designs to Stories

Connect design files to specific user stories:

| User Story | Figma File | Design Version | Status |
|------------|------------|---------------|--------|
| Sign up with email | [Figma link] | v3 (approved May 20) | Ready for dev |
| Dashboard overview | [Figma link] | v1 (approved May 22) | Ready for dev |
| Settings page | [Figma link] | v2 (draft May 25) | In review |

## Step 9: Review with Engineering

Before development starts:

- [ ] Engineering has reviewed designs for feasibility
- [ ] Technical constraints have been discussed
- [ ] Design tokens map to existing CSS variables or code constants
- [ ] Component breakdown aligns with current architecture
- [ ] Complex interactions have been prototyped and tested
- [ ] Third-party limitations are identified (API constraints, library limitations)
- [ ] Performance implications are understood (animation cost, asset size)

## Key Principles

- **Design with tokens, not values** — Hex codes become variables. Spacing uses a scale.
- **Handoff is a conversation** — Not a one-time documentation dump. Ongoing dialogue.
- **All states, always** — Missing states = rework. Design every state before handing off.
- **Accessibility is not optional** — Document it explicitly, test it rigorously.
- **Link designs to code** — Every story should know which design version it implements.
- **Design QA is a required step** — Not a "nice to have." Budget time for it.

## Common Mistakes

- Designers not understanding technical constraints (review with engineering early)
- Missing states in designs (especially error, loading, empty)
- Static designs that don't account for dynamic content lengths
- No design system, leading to inconsistent implementations
- Handoff treated as "throw it over the wall" rather than collaboration
- Hex values used instead of design tokens (hard to maintain, hard to theme)
- Accessibility left to engineering to figure out
- Designs not version-linked to code (confusion about what's current)
- No design QA process (design fidelity degrades over time)

## Key References

- Brad Frost, "Atomic Design"
- "Design Systems" by Alla Khmelnitsky
- Figma Dev Mode documentation
- Storybook documentation
- WCAG 2.1 Accessibility Guidelines
