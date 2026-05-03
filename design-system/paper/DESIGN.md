---
name: Paper
colors:
  primary: "#111111"
  secondary: "#8B5CF6"
  success: "#16A34A"
  warning: "#D97706"
  danger: "#DC2626"
  surface: "#FFFFFF"
  text: "#111827"
  neutral: "#FFFFFF"
typography:
  h1:
    fontFamily: "Montserrat"
    fontSize: 2.5rem
  body-md:
    fontFamily: "Roboto"
    fontSize: 1rem
  label-caps:
    fontFamily: "PT Mono"
    fontSize: 0.875rem
  sourceScale: "14/16/18/24/32/40"
  weights: "100, 200, 300, 400, 500, 600, 700, 800, 900"
rounded:
  sm: 4px
  md: 8px
spacing:
  sm: 4px
  md: 8px
  sourceScale: "4/8/12/16/24/32"
---

# Paper Design Style

## Overview

Paper-textured, print-inspired, tactile surfaces with serif/sans typography.

Use this style when the interface should feel readable, paced, typographic, and content-led. The design should be recognizable as Paper, but still prioritize clarity, accessibility, and product fit over decoration.

## Style Intent

This style should help the interface feel:

- coherent and recognizable as Paper
- aligned with the user's product, audience, and task context
- visually distinctive without becoming decorative noise
- accessible, responsive, and implementation-ready
- consistent across layout, components, states, and content tone

## Design Tokens

### Color

- **Primary:** `#111111` - main actions, active states, and key highlights.
- **Secondary:** `#8B5CF6` - supporting accents, secondary surfaces, or tonal variation.
- **Surface:** `#FFFFFF` - page backgrounds, cards, panels, and layout surfaces.
- **Text:** `#111827` - primary readable content.
- **Neutral:** `#FFFFFF` - borders, muted backgrounds, dividers, or inactive UI.
- **Success:** `#16A34A` - completed, positive, or confirmed states.
- **Warning:** `#D97706` - caution, pending, or review-needed states.
- **Danger:** `#DC2626` - destructive, failed, or high-risk states.

Keep color usage role-based. Do not introduce new raw colors unless they extend this palette deliberately.

### Typography

- **Display / H1:** Montserrat, `2.5rem`
- **Body:** Roboto, `1rem`
- **Labels / metadata:** PT Mono, `0.875rem`
- **Scale:** 14/16/18/24/32/40
- **Weights:** 100, 200, 300, 400, 500, 600, 700, 800, 900

Use typography to create hierarchy before adding decoration. Headings should establish intent; body copy should stay readable; labels should clarify system state.

### Spacing and Radius

- **Spacing scale:** 4/8/12/16/24/32
- **Small spacing:** `4px`
- **Medium spacing:** `8px`
- **Small radius:** `4px`
- **Medium radius:** `8px`

Use spacing consistently across sections, cards, forms, and component internals. Avoid one-off values that make the system feel uneven.

## Component Guidance

Prioritize these component patterns for this style:

- Article headers and content blocks
- Pull quotes, captions, and side notes
- Cards for related stories or resources

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

- Build strong reading rhythm and typographic contrast.
- Use whitespace and grids to create pace.
- Support long-form hierarchy and captions.
- Use the defined tokens as the default source of truth.
- Keep component behavior predictable across the product.

## Don't

- Do not make line lengths too wide.
- Do not overuse card chrome around reading content.
- Do not sacrifice readability for decorative type.
- Do not add visual effects that are not supported by the style intent.
- Do not introduce arbitrary colors, spacing, radius, or shadow values.

## Best Used For

- blogs and magazines
- documentation sites
- long-form product pages
- reports
- content-heavy experiences
