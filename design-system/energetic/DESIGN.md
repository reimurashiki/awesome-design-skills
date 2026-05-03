---
name: Energetic
colors:
  primary: "#EA580B"
  secondary: "#F59E0B"
  background: "#FFEDD5"
  surface: "#FDBA74"
  text: "#EA580C"
  neutral: "#FDBA74"
typography:
  h1:
    fontFamily: "Limelight"
    fontSize: 3rem
  body-md:
    fontFamily: "Limelight"
    fontSize: 1rem
  label-caps:
    fontFamily: "JetBrains Mono"
    fontSize: 0.75rem
  sourceScale: "12/14/16/20/24/32/48"
  weights: "400"
rounded:
  sm: 4px
  md: 8px
spacing:
  sm: 4px
  md: 8px
  sourceScale: "4/8/12/16/24/32/48/64"
---

# Energetic Design Style

## Overview

Motion, vitality, thick borders, geometric shapes, and expressive typography.

Use this style when the interface should feel confident, high-contrast, memorable, and energetic. The design should be recognizable as Energetic, but still prioritize clarity, accessibility, and product fit over decoration.

## Style Intent

This style should help the interface feel:

- coherent and recognizable as Energetic
- aligned with the user's product, audience, and task context
- visually distinctive without becoming decorative noise
- accessible, responsive, and implementation-ready
- consistent across layout, components, states, and content tone

## Design Tokens

### Color

- **Primary:** `#EA580B` - main actions, active states, and key highlights.
- **Secondary:** `#F59E0B` - supporting accents, secondary surfaces, or tonal variation.
- **Surface:** `#FDBA74` - page backgrounds, cards, panels, and layout surfaces.
- **Text:** `#EA580C` - primary readable content.
- **Neutral:** `#FDBA74` - borders, muted backgrounds, dividers, or inactive UI.
- **Success:** `define success token` - completed, positive, or confirmed states.
- **Warning:** `define warning token` - caution, pending, or review-needed states.
- **Danger:** `define danger token` - destructive, failed, or high-risk states.

Keep color usage role-based. Do not introduce new raw colors unless they extend this palette deliberately.

### Typography

- **Display / H1:** Limelight, `3rem`
- **Body:** Limelight, `1rem`
- **Labels / metadata:** JetBrains Mono, `0.75rem`
- **Scale:** 12/14/16/20/24/32/48
- **Weights:** 400

Use typography to create hierarchy before adding decoration. Headings should establish intent; body copy should stay readable; labels should clarify system state.

### Spacing and Radius

- **Spacing scale:** 4/8/12/16/24/32/48/64
- **Small spacing:** `4px`
- **Medium spacing:** `8px`
- **Small radius:** `4px`
- **Medium radius:** `8px`

Use spacing consistently across sections, cards, forms, and component internals. Avoid one-off values that make the system feel uneven.

## Component Guidance

Prioritize these component patterns for this style:

- Hero typography and campaign sections
- High-contrast buttons and tags
- Statement cards and large visual blocks

### Surfaces and Cards

- Use surfaces to group related content and actions.
- Keep card padding, border radius, and border/shadow treatment consistent.
- Make selected, active, hover, and disabled states visually distinct.

### Navigation and Hierarchy

- Keep primary navigation predictable and easy to scan.
- Use typography, spacing, and color contrast to guide attention.
- Keep secondary actions visually quieter than primary actions.

### Forms and Actions

- Labels should be clear and visible.
- Validation and error states should be specific and recoverable.
- Primary actions should describe outcomes, not vague actions.

## Layout Rules

- Start from a clear content hierarchy before styling details.
- Use the spacing scale to separate sections, groups, and individual controls.
- Keep alignment consistent across repeated components.
- Design mobile, tablet, and desktop behavior intentionally.
- Preserve whitespace where it improves comprehension; reduce it where density is the product need.

## Accessibility Notes

- Maintain WCAG 2.2 AA contrast for text and interactive elements.
- Provide visible focus states for keyboard users.
- Do not rely on color alone for status or validation.
- Keep touch targets at least 44x44px where practical.
- Support reduced motion preferences for animated effects.
- Test long labels, empty states, loading states, error states, and overflow.

## Do

- Use strong scale contrast and confident composition.
- Anchor bold moments to the most important content.
- Balance intensity with readable structure.
- Use the defined tokens as the default source of truth.
- Keep component behavior predictable across the product.

## Don't

- Do not make every element compete for attention.
- Do not use contrast that fails accessibility.
- Do not stack multiple loud effects at once.
- Do not add visual effects that are not supported by the style intent.
- Do not introduce arbitrary colors, spacing, radius, or shadow values.

## Best Used For

- campaign pages
- launch moments
- creative portfolios
- event pages
- high-impact product announcements
