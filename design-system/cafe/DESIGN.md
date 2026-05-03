---
name: Cafe
colors:
  primary: "#5D4432"
  secondary: "#E9E3DD"
  success: "#16A34A"
  warning: "#D97706"
  danger: "#DC2626"
  surface: "#F9F7F5"
  text: "#3E2B1E"
  neutral: "#F9F7F5"
typography:
  h1:
    fontFamily: "Poppins"
    fontSize: 3rem
  body-md:
    fontFamily: "Poppins"
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
  sm: 2px
  md: 4px
  sourceScale: "2/4/8/12/16/24/32/48"
---

# Cafe Design Style

## Overview

Warm, cozy, relaxed browsing experiences with cafe-inspired tones and soft typography.

Use this style when the interface should feel layered, tactile, atmospheric, and depth-driven. The design should be recognizable as Cafe, but still prioritize clarity, accessibility, and product fit over decoration.

## Style Intent

This style should help the interface feel:

- coherent and recognizable as Cafe
- aligned with the user's product, audience, and task context
- visually distinctive without becoming decorative noise
- accessible, responsive, and implementation-ready
- consistent across layout, components, states, and content tone

## Design Tokens

### Color

- **Primary:** `#5D4432` - main actions, active states, and key highlights.
- **Secondary:** `#E9E3DD` - supporting accents, secondary surfaces, or tonal variation.
- **Surface:** `#F9F7F5` - page backgrounds, cards, panels, and layout surfaces.
- **Text:** `#3E2B1E` - primary readable content.
- **Neutral:** `#F9F7F5` - borders, muted backgrounds, dividers, or inactive UI.
- **Success:** `#16A34A` - completed, positive, or confirmed states.
- **Warning:** `#D97706` - caution, pending, or review-needed states.
- **Danger:** `#DC2626` - destructive, failed, or high-risk states.

Keep color usage role-based. Do not introduce new raw colors unless they extend this palette deliberately.

### Typography

- **Display / H1:** Poppins, `3rem`
- **Body:** Poppins, `1rem`
- **Labels / metadata:** JetBrains Mono, `0.75rem`
- **Scale:** desktop-first expressive scale
- **Weights:** 100, 200, 300, 400, 500, 600, 700, 800, 900

Use typography to create hierarchy before adding decoration. Headings should establish intent; body copy should stay readable; labels should clarify system state.

### Spacing and Radius

- **Spacing scale:** 2/4/8/12/16/24/32/48
- **Small spacing:** `2px`
- **Medium spacing:** `4px`
- **Small radius:** `4px`
- **Medium radius:** `8px`

Use spacing consistently across sections, cards, forms, and component internals. Avoid one-off values that make the system feel uneven.

## Component Guidance

Prioritize these component patterns for this style:

- Layered cards and tactile surfaces
- Feature panels and immersive hero blocks
- Badges, overlays, and material callouts

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

- Use depth, material, or texture to reinforce hierarchy.
- Keep decorative effects attached to clear content roles.
- Test blur, shadows, and overlays for contrast.
- Use the defined tokens as the default source of truth.
- Keep component behavior predictable across the product.

## Don't

- Do not obscure content with effects.
- Do not add expensive visual treatments everywhere.
- Do not combine too many surface metaphors.
- Do not add visual effects that are not supported by the style intent.
- Do not introduce arbitrary colors, spacing, radius, or shadow values.

## Best Used For

- immersive landing pages
- brand moments
- visual showcases
- creative product pages
- highly tactile interfaces
