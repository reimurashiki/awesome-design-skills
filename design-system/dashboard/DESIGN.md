---
name: Dashboard
colors:
  primary: "#0C5CAB"
  secondary: "#0a4a8a"
  success: "#10b981"
  warning: "#f59e0b"
  danger: "#ef4444"
  surface: "#09090b"
  text: "#fafafa"
  neutral: "#09090b"
typography:
  h1:
    fontFamily: "IBM Plex Sans"
    fontSize: 2rem
  body-md:
    fontFamily: "IBM Plex Sans"
    fontSize: 1rem
  label-caps:
    fontFamily: "IBM Plex Sans"
    fontSize: 0.75rem
  sourceScale: "12/14/16/20/24/32"
  weights: "100, 200, 300, 400, 500, 600, 700, 800, 900"
rounded:
  sm: 4px
  md: 8px
spacing:
  sm: 8px
  md: 16px
  sourceScale: "8pt baseline grid"
---

# Dashboard Design Style

## Overview

Dark cloud-platform dashboards with modular grids, glass panels, and strong data hierarchy.

Use this style when the interface should feel structured, data-forward, efficient, and highly scannable. The design should be recognizable as Dashboard, but still prioritize clarity, accessibility, and product fit over decoration.

## Style Intent

This style should help the interface feel:

- coherent and recognizable as Dashboard
- aligned with the user's product, audience, and task context
- visually distinctive without becoming decorative noise
- accessible, responsive, and implementation-ready
- consistent across layout, components, states, and content tone

## Design Tokens

### Color

- **Primary:** `#0C5CAB` - main actions, active states, and key highlights.
- **Secondary:** `#0a4a8a` - supporting accents, secondary surfaces, or tonal variation.
- **Surface:** `#09090b` - page backgrounds, cards, panels, and layout surfaces.
- **Text:** `#fafafa` - primary readable content.
- **Neutral:** `#09090b` - borders, muted backgrounds, dividers, or inactive UI.
- **Success:** `#10b981` - completed, positive, or confirmed states.
- **Warning:** `#f59e0b` - caution, pending, or review-needed states.
- **Danger:** `#ef4444` - destructive, failed, or high-risk states.

Keep color usage role-based. Do not introduce new raw colors unless they extend this palette deliberately.

### Typography

- **Display / H1:** IBM Plex Sans, `2rem`
- **Body:** IBM Plex Sans, `1rem`
- **Labels / metadata:** IBM Plex Sans, `0.75rem`
- **Scale:** 12/14/16/20/24/32
- **Weights:** 100, 200, 300, 400, 500, 600, 700, 800, 900

Use typography to create hierarchy before adding decoration. Headings should establish intent; body copy should stay readable; labels should clarify system state.

### Spacing and Radius

- **Spacing scale:** 8pt baseline grid
- **Small spacing:** `8px`
- **Medium spacing:** `16px`
- **Small radius:** `4px`
- **Medium radius:** `8px`

Use spacing consistently across sections, cards, forms, and component internals. Avoid one-off values that make the system feel uneven.

## Component Guidance

Prioritize these component patterns for this style:

- Metric cards and data panels
- Tables, filters, and search controls
- Status badges, alerts, and activity logs

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

- Prioritize scannable hierarchy and state visibility.
- Use cards, tables, charts, and filters consistently.
- Keep dense information organized by task priority.
- Use the defined tokens as the default source of truth.
- Keep component behavior predictable across the product.

## Don't

- Do not hide key metrics behind decorative surfaces.
- Do not use low-contrast chart colors.
- Do not let density collapse spacing or touch targets.
- Do not add visual effects that are not supported by the style intent.
- Do not introduce arbitrary colors, spacing, radius, or shadow values.

## Best Used For

- analytics dashboards
- admin panels
- data-heavy workflows
- operations tools
- developer consoles
