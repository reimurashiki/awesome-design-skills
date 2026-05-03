---
name: Mono
colors:
  primary: "#37F712"
  secondary: "#00A6F4"
  success: "#00A63D"
  warning: "#FE9900"
  danger: "#FF2157"
  surface: "#E7E5E4"
  text: "#78716B"
  neutral: "#E7E5E4"
typography:
  h1:
    fontFamily: "Space Mono"
    fontSize: 3rem
  body-md:
    fontFamily: "Space Mono"
    fontSize: 1rem
  label-caps:
    fontFamily: "JetBrains Mono"
    fontSize: 0.75rem
  sourceScale: "desktop-first expressive scale"
  weights: "100, 200, 300, 400, 500, 600, 700, 800, 900"
rounded:
  sm: 4px
  md: 8px
spacing:
  sm: 4px
  md: 8px
  sourceScale: "compact density mode"
---

# Mono Design Style

## Overview

Monospace, matrix-inspired, high-contrast, compact hacker-chic interfaces.

Use this style when the interface should feel technical, focused, intelligent, and forward-looking. The design should be recognizable as Mono, but still prioritize clarity, accessibility, and product fit over decoration.

## Style Intent

This style should help the interface feel:

- coherent and recognizable as Mono
- aligned with the user's product, audience, and task context
- visually distinctive without becoming decorative noise
- accessible, responsive, and implementation-ready
- consistent across layout, components, states, and content tone

## Design Tokens

### Color

- **Primary:** `#37F712` - main actions, active states, and key highlights.
- **Secondary:** `#00A6F4` - supporting accents, secondary surfaces, or tonal variation.
- **Surface:** `#E7E5E4` - page backgrounds, cards, panels, and layout surfaces.
- **Text:** `#78716B` - primary readable content.
- **Neutral:** `#E7E5E4` - borders, muted backgrounds, dividers, or inactive UI.
- **Success:** `#00A63D` - completed, positive, or confirmed states.
- **Warning:** `#FE9900` - caution, pending, or review-needed states.
- **Danger:** `#FF2157` - destructive, failed, or high-risk states.

Keep color usage role-based. Do not introduce new raw colors unless they extend this palette deliberately.

### Typography

- **Display / H1:** Space Mono, `3rem`
- **Body:** Space Mono, `1rem`
- **Labels / metadata:** JetBrains Mono, `0.75rem`
- **Scale:** desktop-first expressive scale
- **Weights:** 100, 200, 300, 400, 500, 600, 700, 800, 900

Use typography to create hierarchy before adding decoration. Headings should establish intent; body copy should stay readable; labels should clarify system state.

### Spacing and Radius

- **Spacing scale:** compact density mode
- **Small spacing:** `4px`
- **Medium spacing:** `8px`
- **Small radius:** `4px`
- **Medium radius:** `8px`

Use spacing consistently across sections, cards, forms, and component internals. Avoid one-off values that make the system feel uneven.

## Component Guidance

Prioritize these component patterns for this style:

- Command panels and task cards
- Status indicators and terminal/code blocks
- Agent, automation, or system event timelines

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

- Use system status, glow, depth, or code-like detail to clarify function.
- Keep futuristic visuals controlled and purposeful.
- Make complex workflows feel guided and explainable.
- Use the defined tokens as the default source of truth.
- Keep component behavior predictable across the product.

## Don't

- Do not make interfaces feel like sci-fi decoration only.
- Do not hide controls in overly abstract layouts.
- Do not use neon or glow without contrast testing.
- Do not add visual effects that are not supported by the style intent.
- Do not introduce arbitrary colors, spacing, radius, or shadow values.

## Best Used For

- AI products
- developer tools
- cybersecurity apps
- automation dashboards
- experimental interfaces
