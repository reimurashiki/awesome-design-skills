---
name: Elegant
colors:
  primary: "#3B82F6"
  secondary: "#8B5CF6"
  success: "#16A34A"
  warning: "#D97706"
  danger: "#DC2626"
  surface: "#FFFFFF"
  text: "#111827"
  neutral: "#FFFFFF"
typography:
  h1:
    fontFamily: "Google Sans"
    fontSize: 2.5rem
  body-md:
    fontFamily: "Google Sans"
    fontSize: 1rem
  label-caps:
    fontFamily: "Anonymous Pro"
    fontSize: 0.875rem
  sourceScale: "14/16/18/24/32/40"
  weights: "100, 200, 300, 400, 500, 600"
rounded:
  sm: 4px
  md: 8px
spacing:
  sm: 4px
  md: 8px
  sourceScale: "4/8/12/16/24/32"
---

# Elegant Design Style

## Overview

Graceful sophistication, delicate typography, minimal palettes, and polished layouts.

Use this style when the interface should feel refined, spacious, restrained, and premium. The design should be recognizable as Elegant, but still prioritize clarity, accessibility, and product fit over decoration.

## Style Intent

This style should help the interface feel:

- coherent and recognizable as Elegant
- aligned with the user's product, audience, and task context
- visually distinctive without becoming decorative noise
- accessible, responsive, and implementation-ready
- consistent across layout, components, states, and content tone

## Design Tokens

### Color

- **Primary:** `#3B82F6` - main actions, active states, and key highlights.
- **Secondary:** `#8B5CF6` - supporting accents, secondary surfaces, or tonal variation.
- **Surface:** `#FFFFFF` - page backgrounds, cards, panels, and layout surfaces.
- **Text:** `#111827` - primary readable content.
- **Neutral:** `#FFFFFF` - borders, muted backgrounds, dividers, or inactive UI.
- **Success:** `#16A34A` - completed, positive, or confirmed states.
- **Warning:** `#D97706` - caution, pending, or review-needed states.
- **Danger:** `#DC2626` - destructive, failed, or high-risk states.

Keep color usage role-based. Do not introduce new raw colors unless they extend this palette deliberately.

### Typography

- **Display / H1:** Google Sans, `2.5rem`
- **Body:** Google Sans, `1rem`
- **Labels / metadata:** Anonymous Pro, `0.875rem`
- **Scale:** 14/16/18/24/32/40
- **Weights:** 100, 200, 300, 400, 500, 600

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

- Large hero imagery and editorial sections
- Minimal navigation and premium CTAs
- Product or portfolio detail cards

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

- Use restraint, precision, and spacious composition.
- Let typography, imagery, and material cues carry the premium feel.
- Keep interactions subtle and polished.
- Use the defined tokens as the default source of truth.
- Keep component behavior predictable across the product.

## Don't

- Do not overcrowd the layout.
- Do not use loud color unless it is a deliberate accent.
- Do not cheapen the style with generic effects.
- Do not add visual effects that are not supported by the style intent.
- Do not introduce arbitrary colors, spacing, radius, or shadow values.

## Best Used For

- premium brands
- high-end product pages
- portfolio sites
- boutique ecommerce
- exclusive member experiences
