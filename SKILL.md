---
name: design-system
description: Use this skill whenever the user asks to generate, audit, improve, choose, combine, or apply a visual design system or UI style. This is the router for bundled design styles in this folder: inspect the registry, choose the best style(s), read the relevant `design-system/<slug>/DESIGN.md`, then apply the universal quality standards here. Also use for visual consistency checks, UI redesign direction, styling PR reviews, accessibility-aware design polish, anti-AI-slop review, or prompts like "make this premium/minimal/bold/modern/dashboard/etc."
origin: ECC
---

# Design System Router

Use this skill to choose and apply a visual direction with production-quality UI standards. The root skill contains universal rules. Style resources live under `design-system/<style>/DESIGN.md`.

## Core Mission

Create interfaces that feel intentional, accessible, coherent, and specific to the user's product. Avoid generic AI-looking visuals. Treat style as a system: tokens, hierarchy, spacing, components, states, copy tone, responsiveness, and quality gates should work together.

## When to Use

Use this skill when the user wants to:

- Create a new visual direction or design system
- Pick a style such as premium, minimal, bold, dashboard, retro, vintage, agentic, etc.
- Improve UI polish, hierarchy, layout, colors, typography, or component consistency
- Audit UI for design quality, accessibility, responsive behavior, or AI slop
- Convert vague style requests into concrete tokens and implementation rules
- Combine multiple visual references into one coherent direction
- Review styling changes in code or propose design-system migration steps

## Resource Model

This folder is structured as one installable skill plus bundled style resources:

```text
SKILL.md                         # only install entrypoint and universal router
design-system/<style>/DESIGN.md  # bundled style-specific tokens, foundations, and usage notes
```

Do not expect a `SKILL.md` inside each style folder. Always read the selected style's `design-system/<slug>/DESIGN.md` before giving detailed recommendations or making UI changes.

## Router Workflow

1. Parse the user's goal, product type, audience, brand tone, constraints, and visual adjectives.
2. Use the **Design Style Registry** to shortlist 1-3 candidate styles.
3. Choose one primary style. Add one secondary style only when it adds useful nuance.
4. Read the selected style file(s): `design-system/<slug>/DESIGN.md`.
5. Apply the universal standards in this root skill.
6. If implementing code, inspect the project's existing tokens/components before changing visuals.
7. Explain trade-offs briefly when a requested style conflicts with accessibility, product context, or usability.

## Style Selection Heuristics

- Product dashboards, admin panels, analytics: `dashboard`, `enterprise`, `ant`, `application`, `bento`
- SaaS/product marketing: `premium`, `modern`, `sleek`, `levels`, `contemporary`, `professional`
- Enterprise/B2B/trust-heavy: `enterprise`, `corporate`, `professional`, `ant`, `clean`
- Editorial/content/reading: `editorial`, `publication`, `paper`, `refined`, `modern`
- Luxury/high-end brand: `luxury`, `premium`, `elegant`, `refined`
- Playful/consumer/friendly: `friendly`, `lingo`, `colorful`, `doodle`, `claymorphism`
- Bold/attention-grabbing: `bold`, `dramatic`, `expressive`, `energetic`, `neobrutalism`
- Retro/game/nostalgia: `retro`, `vintage`, `pacman`, `tetris`, `dithered`
- Futuristic/AI/dev/cyber: `agentic`, `futuristic`, `cosmic`, `neon`, `mono`
- Minimal/clarity-first: `minimal`, `simple`, `clean`, `spacious`, `flat`
- Component-library alignment: `material`, `shadcn`, `ant`

## Universal Quality Standards

### Accessibility Baseline

Design decisions must preserve usability before decoration.

- Meet WCAG 2.2 AA contrast for text, icons, focus states, and controls.
- Use semantic HTML before ARIA when implementing UI.
- Provide visible `focus-visible` states for all interactive controls.
- Keep touch targets at least 44x44px where practical.
- Support keyboard navigation for menus, dialogs, forms, tabs, and custom controls.
- Respect reduced motion preferences; avoid essential information being animation-only.
- Design loading, empty, error, disabled, and long-content states.
- Check text overflow, long labels, localization expansion, and responsive breakpoints.

### Anti AI-Slop Rules

Avoid patterns that make the interface feel generated, generic, or decoration-first:

- Do not default to purple/blue gradients unless the selected style justifies it.
- Do not add glassmorphism, glow, blur, or floating cards without functional purpose.
- Do not center every hero with generic headline/subheadline/CTA rhythm.
- Do not overuse huge rounded corners, vague shadows, stock icons, or random emoji.
- Do not mix multiple visual metaphors unless one style clearly dominates.
- Do not use arbitrary colors, spacing, or font sizes outside a coherent system.
- Replace vague adjectives with concrete tokens, spacing, hierarchy, and examples.

### Visual System Rules

- Define color roles: background, surface, surface-muted, border, text, text-muted, primary, accent, success, warning, danger.
- Define type roles: display, h1, h2, h3, body, label, caption, code/mono if needed.
- Use a spacing rhythm, usually 4px or 8px based.
- Keep radius, shadows, borders, and elevation consistent by component role.
- Make component states explicit: default, hover, active, focus, disabled, loading, error, selected.
- Preserve hierarchy: important content should win through scale, contrast, position, and spacing.
- Prefer reusable design tokens over one-off values.

### Interaction and Motion

- Motion should clarify state, hierarchy, or cause/effect.
- Use transforms and opacity for performance-friendly animation.
- Keep transitions short and purposeful for common UI interactions.
- Avoid scroll-triggered theatrics in utility-heavy workflows unless the product context calls for it.

### Responsive Behavior

- Define how layout changes across mobile, tablet, and desktop.
- Avoid fixed-width layouts that break on small screens.
- Stack dense grids thoughtfully; do not simply shrink everything.
- Keep primary actions reachable and forms easy to complete on touch devices.

## Output Patterns

### When asked to choose a style

Return a concise recommendation:

```markdown
Recommended style: `<slug>` - <why it fits>
Optional secondary: `<slug>` - <what to borrow>
Read next: `design-system/<slug>/DESIGN.md`
Implementation notes:
- <token/component/layout note>
- <accessibility note>
- <anti-slop or quality note>
```

### When asked to generate a design system

Produce implementation-ready guidance:

```markdown
## Context and goals
## Selected style direction
## Design tokens
## Typography system
## Layout and spacing rules
## Component rules and states
## Accessibility requirements
## Anti-patterns to avoid
## Implementation checklist
```

### When auditing an existing UI

Score and explain:

1. Color consistency
2. Typography hierarchy
3. Spacing rhythm
4. Component consistency
5. Responsive behavior
6. Accessibility
7. Interaction states and motion
8. Information density
9. Brand/style fit
10. Polish and anti-slop

For code reviews, include exact file paths and actionable fixes when available.

## Design Style Registry

Paths are relative to the repository root when installed from the GitHub repo URL.

| Slug | Use when the user wants... | Read next |
|---|---|---|
| `agentic` | Conversational AI-first interfaces with minimal controls, clear outcomes, and delegated task flows. | `design-system/agentic/DESIGN.md` |
| `ant` | Structured enterprise UI for data-dense web apps with clarity, consistency, and efficiency. | `design-system/ant/DESIGN.md` |
| `application` | App dashboards with purple-themed aesthetic, top-bar navigation, cards, and developer workflows. | `design-system/application/DESIGN.md` |
| `artistic` | High-contrast expressive interfaces with creative typography and striking color choices. | `design-system/artistic/DESIGN.md` |
| `bento` | Modular card grids, scannable blocks, soft spacing, and organized product layouts. | `design-system/bento/DESIGN.md` |
| `bold` | Heavy typography, high contrast, commanding layouts, and strong visual presence. | `design-system/bold/DESIGN.md` |
| `brutalism` | Raw anti-design, jarring layouts, concrete-inspired simplicity, and functional minimalism. | `design-system/brutalism/DESIGN.md` |
| `cafe` | Warm, cozy, relaxed browsing experiences with cafe-inspired tones and soft typography. | `design-system/cafe/DESIGN.md` |
| `claymorphism` | Soft, rounded, playful 3D clay-like UI with puffy colorful surfaces. | `design-system/claymorphism/DESIGN.md` |
| `clean` | Reduced clutter, ample whitespace, legible typography, and limited color palettes. | `design-system/clean/DESIGN.md` |
| `colorful` | Vibrant high-contrast palettes, gradients, and memorable modern energy. | `design-system/colorful/DESIGN.md` |
| `contemporary` | Current-era minimalism with bento grids, dark mode, accessibility, and performance. | `design-system/contemporary/DESIGN.md` |
| `corporate` | Professional, brand-aligned, structured, enterprise-safe visual systems. | `design-system/corporate/DESIGN.md` |
| `cosmic` | Futuristic sci-fi, dark themes, neon accents, and immersive spatial elements. | `design-system/cosmic/DESIGN.md` |
| `creative` | Playful, character-driven landing pages and bold graphics for creative projects. | `design-system/creative/DESIGN.md` |
| `dashboard` | Dark cloud-platform dashboards with modular grids, glass panels, and strong data hierarchy. | `design-system/dashboard/DESIGN.md` |
| `dithered` | Dot-pattern, limited-palette, nostalgic high-contrast visuals. | `design-system/dithered/DESIGN.md` |
| `doodle` | Hand-drawn, sketch-like, handwritten, imperfect, playful informal UI. | `design-system/doodle/DESIGN.md` |
| `dramatic` | Theatrical, immersive, high-contrast layouts that command attention. | `design-system/dramatic/DESIGN.md` |
| `editorial` | Magazine-inspired layouts, serif typography, structured grids, and elegant reading. | `design-system/editorial/DESIGN.md` |
| `elegant` | Graceful sophistication, delicate typography, minimal palettes, and polished layouts. | `design-system/elegant/DESIGN.md` |
| `energetic` | Motion, vitality, thick borders, geometric shapes, and expressive typography. | `design-system/energetic/DESIGN.md` |
| `enterprise` | Data-driven workflows, high contrast, drag-and-drop patterns, and structured layouts. | `design-system/enterprise/DESIGN.md` |
| `expressive` | Personality-driven visuals, bold colors, playful graphics, and dynamic layouts. | `design-system/expressive/DESIGN.md` |
| `fantasy` | Game-inspired premium fantasy visuals with rich palettes and immersive themes. | `design-system/fantasy/DESIGN.md` |
| `flat` | Two-dimensional minimal UI with vibrant colors, clean type, and no 3D effects. | `design-system/flat/DESIGN.md` |
| `friendly` | Approachable rounded UI, soft pastels, whitespace, and intuitive layouts. | `design-system/friendly/DESIGN.md` |
| `futuristic` | Innovation-driven tech aesthetics, sleek type, and forward-looking layouts. | `design-system/futuristic/DESIGN.md` |
| `glassmorphism` | Frosted glass, translucent layers, subtle blur, luminous borders, and depth. | `design-system/glassmorphism/DESIGN.md` |
| `gradient` | Smooth color transitions and gradient-rich surfaces with playful depth. | `design-system/gradient/DESIGN.md` |
| `levels` | Conversion-focused pages that reduce friction and guide users to action. | `design-system/levels/DESIGN.md` |
| `lingo` | Bright, rounded, tactile 3D, friendly illustrated consumer experiences. | `design-system/lingo/DESIGN.md` |
| `luxury` | High-end dark aesthetics, premium monochrome, and bold refined headings. | `design-system/luxury/DESIGN.md` |
| `material` | Google's Material Design patterns, layered surfaces, dynamic theming, and responsive motion. | `design-system/material/DESIGN.md` |
| `minimal` | Restrained color, whitespace, clean typography, and maximum focus. | `design-system/minimal/DESIGN.md` |
| `modern` | Contemporary editorial polish with serif typography and clean digital product layouts. | `design-system/modern/DESIGN.md` |
| `mono` | Monospace, matrix-inspired, high-contrast, compact hacker-chic interfaces. | `design-system/mono/DESIGN.md` |
| `neobrutalism` | Bold borders, vivid accents, raw high-contrast layouts, and warm surfaces. | `design-system/neobrutalism/DESIGN.md` |
| `neon` | Electric glow, high contrast, and attention-grabbing neon color pairings. | `design-system/neon/DESIGN.md` |
| `neumorphism` | Soft extruded UI with inner/outer shadows and tactile embedded surfaces. | `design-system/neumorphism/DESIGN.md` |
| `pacman` | Retro arcade, pixel fonts, dotted borders, and 8-bit game aesthetics. | `design-system/pacman/DESIGN.md` |
| `paper` | Paper-textured, print-inspired, tactile surfaces with serif/sans typography. | `design-system/paper/DESIGN.md` |
| `perspective` | Isometric/spatial depth, vanishing points, and layered 3D-like realism. | `design-system/perspective/DESIGN.md` |
| `premium` | Apple-inspired polish, precise spacing, refined typography, and premium feel. | `design-system/premium/DESIGN.md` |
| `professional` | Business-ready trust, modern typography, structured layouts, and polished identity. | `design-system/professional/DESIGN.md` |
| `publication` | Books, magazines, reports, editorial grids, and expressive print typography. | `design-system/publication/DESIGN.md` |
| `refined` | Curated modern minimalism, elegant serif typography, and understated palettes. | `design-system/refined/DESIGN.md` |
| `retro` | Vintage-inspired typography, nostalgic palettes, and throwback visual elements. | `design-system/retro/DESIGN.md` |
| `shadcn` | shadcn/ui-style clean components, monochrome palette, and utility-first patterns. | `design-system/shadcn/DESIGN.md` |
| `simple` | No-frills clarity, neutral colors, intuitive layouts, and unobtrusive UI. | `design-system/simple/DESIGN.md` |
| `skeumorphism` | Real-world mimicry, textures, 3D effects, and familiar physical metaphors. | `design-system/skeumorphism/DESIGN.md` |
| `sleek` | Clean lines, intentional color, subtle interactions, and consistent spacing. | `design-system/sleek/DESIGN.md` |
| `spacious` | Generous whitespace, consistent padding, grid layouts, and breathing room. | `design-system/spacious/DESIGN.md` |
| `storytelling` | Narrative-driven visuals, copy, and interactions that guide users emotionally. | `design-system/storytelling/DESIGN.md` |
| `tetris` | Classic block-game energy, playful colors, compact layouts, and bold display fonts. | `design-system/tetris/DESIGN.md` |
| `vibrant` | Lively color, playful typography, warm accents, and dynamic visual energy. | `design-system/vibrant/DESIGN.md` |
| `vintage` | 1950s-1990s nostalgia, grain, retro palettes, pixel typography, and skeuomorphic touches. | `design-system/vintage/DESIGN.md` |

## Implementation Checklist

Before finalizing a design recommendation or UI change:

- Selected style file has been read.
- Tokens are coherent and not arbitrary.
- Accessibility constraints are preserved.
- Responsive behavior is accounted for.
- Component states are specified or implemented.
- The design has a clear primary visual language.
- AI-slop patterns have been removed or justified by the style.
- The result matches the user's product, audience, and goal.
