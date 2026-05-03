---
name: design-system
description: Use this skill whenever the user asks to generate, audit, improve, choose, combine, or apply a visual design system/style. This is the router skill for the bundled design styles in this folder: first inspect the design style registry, select the best matching style skill(s), then read the relevant `<slug>/DESIGN.md` and `<slug>/DESIGN.md` before implementing or advising. Also use for visual consistency checks, styling PR reviews, UI redesign direction, or prompts like “make this premium/minimal/bold/modern/dashboard/etc.”
origin: ECC
---

# Design System — Router, Generate & Audit Visual Systems

## When to Use

- Starting a new project that needs a design system
- Auditing an existing codebase for visual consistency
- Before a redesign — understand what you have
- When the UI looks "off" but you can't pinpoint why
- Reviewing PRs that touch styling
- Choosing a visual direction from the bundled design style skills
- Translating user language like “premium”, “friendly”, “dashboard”, “retro”, “bold”, or “minimal” into a concrete design style
- Combining multiple compatible design styles into one coherent direction

## Router Workflow

This skill is a parent/router for the design style skills stored in sibling folders.

1. Parse the user's goal, audience, product type, and visual adjectives.
2. Check the **Design Style Registry** below and shortlist 1-3 matching styles.
3. Pick a primary style. Optionally pick one secondary style only when it adds useful nuance.
4. Read the selected style resource before acting:
   - `<slug>/DESIGN.md` for visual tokens, examples, rationale, and implementation guidance
5. If the user names a style directly, use that style unless it conflicts with their product/audience. If it conflicts, briefly explain the concern and suggest a better match.
6. When combining styles, keep one dominant visual language. Do not stack effects blindly; combine intent, not decoration.

### Selection Heuristics

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
- Material/component-library alignment: `material`, `shadcn`, `ant`

### Output Pattern When Asked to Choose a Style

Return a concise recommendation:

```markdown
Recommended style: `<slug>` — <why it fits>
Optional secondary: `<slug>` — <what to borrow>
Use these resources: `<slug>/DESIGN.md`
Implementation notes: <3-5 bullets tailored to the user prompt>
```

When implementing code, do not stop at the recommendation. Read the chosen style files and apply the guidance.

## Design Style Registry

Use this registry to map user intent to a concrete style skill. Paths are relative to this `design-system` skill folder.

| Slug | Use when the user wants... | Read next |
|---|---|---|
| `agentic` | Conversational AI-first interfaces with minimal controls, clear outcomes, and delegated task flows. | `agentic/DESIGN.md` |
| `ant` | Structured enterprise UI for data-dense web apps with clarity, consistency, and efficiency. | `ant/DESIGN.md` |
| `application` | App dashboards with purple-themed aesthetic, top-bar navigation, cards, and developer workflows. | `application/DESIGN.md` |
| `artistic` | High-contrast expressive interfaces with creative typography and striking color choices. | `artistic/DESIGN.md` |
| `bento` | Modular card grids, scannable blocks, soft spacing, and organized product layouts. | `bento/DESIGN.md` |
| `bold` | Heavy typography, high contrast, commanding layouts, and strong visual presence. | `bold/DESIGN.md` |
| `brutalism` | Raw anti-design, jarring layouts, concrete-inspired simplicity, and functional minimalism. | `brutalism/DESIGN.md` |
| `cafe` | Warm, cozy, relaxed browsing experiences with cafe-inspired tones and soft typography. | `cafe/DESIGN.md` |
| `claymorphism` | Soft, rounded, playful 3D clay-like UI with puffy colorful surfaces. | `claymorphism/DESIGN.md` |
| `clean` | Reduced clutter, ample whitespace, legible typography, and limited color palettes. | `clean/DESIGN.md` |
| `colorful` | Vibrant high-contrast palettes, gradients, and memorable modern energy. | `colorful/DESIGN.md` |
| `contemporary` | Current-era minimalism with bento grids, dark mode, accessibility, and performance. | `contemporary/DESIGN.md` |
| `corporate` | Professional, brand-aligned, structured, enterprise-safe visual systems. | `corporate/DESIGN.md` |
| `cosmic` | Futuristic sci-fi, dark themes, neon accents, and immersive spatial elements. | `cosmic/DESIGN.md` |
| `creative` | Playful, character-driven landing pages and bold graphics for creative projects. | `creative/DESIGN.md` |
| `dashboard` | Dark cloud-platform dashboards with modular grids, glass panels, and strong data hierarchy. | `dashboard/DESIGN.md` |
| `dithered` | Dot-pattern, limited-palette, nostalgic high-contrast visuals. | `dithered/DESIGN.md` |
| `doodle` | Hand-drawn, sketch-like, handwritten, imperfect, playful informal UI. | `doodle/DESIGN.md` |
| `dramatic` | Theatrical, immersive, high-contrast layouts that command attention. | `dramatic/DESIGN.md` |
| `editorial` | Magazine-inspired layouts, serif typography, structured grids, and elegant reading. | `editorial/DESIGN.md` |
| `elegant` | Graceful sophistication, delicate typography, minimal palettes, and polished layouts. | `elegant/DESIGN.md` |
| `energetic` | Motion, vitality, thick borders, geometric shapes, and expressive typography. | `energetic/DESIGN.md` |
| `enterprise` | Data-driven workflows, high contrast, drag-and-drop patterns, and structured layouts. | `enterprise/DESIGN.md` |
| `expressive` | Personality-driven visuals, bold colors, playful graphics, and dynamic layouts. | `expressive/DESIGN.md` |
| `fantasy` | Game-inspired premium fantasy visuals with rich palettes and immersive themes. | `fantasy/DESIGN.md` |
| `flat` | Two-dimensional minimal UI with vibrant colors, clean type, and no 3D effects. | `flat/DESIGN.md` |
| `friendly` | Approachable rounded UI, soft pastels, whitespace, and intuitive layouts. | `friendly/DESIGN.md` |
| `futuristic` | Innovation-driven tech aesthetics, sleek type, and forward-looking layouts. | `futuristic/DESIGN.md` |
| `glassmorphism` | Frosted glass, translucent layers, subtle blur, luminous borders, and depth. | `glassmorphism/DESIGN.md` |
| `gradient` | Smooth color transitions and gradient-rich surfaces with playful depth. | `gradient/DESIGN.md` |
| `levels` | Conversion-focused pages that reduce friction and guide users to action. | `levels/DESIGN.md` |
| `lingo` | Bright, rounded, tactile 3D, friendly illustrated consumer experiences. | `lingo/DESIGN.md` |
| `luxury` | High-end dark aesthetics, premium monochrome, and bold refined headings. | `luxury/DESIGN.md` |
| `material` | Google's Material Design patterns, layered surfaces, dynamic theming, and responsive motion. | `material/DESIGN.md` |
| `minimal` | Restrained color, whitespace, clean typography, and maximum focus. | `minimal/DESIGN.md` |
| `modern` | Contemporary editorial polish with serif typography and clean digital product layouts. | `modern/DESIGN.md` |
| `mono` | Monospace, matrix-inspired, high-contrast, compact hacker-chic interfaces. | `mono/DESIGN.md` |
| `neobrutalism` | Bold borders, vivid accents, raw high-contrast layouts, and warm surfaces. | `neobrutalism/DESIGN.md` |
| `neon` | Electric glow, high contrast, and attention-grabbing neon color pairings. | `neon/DESIGN.md` |
| `neumorphism` | Soft extruded UI with inner/outer shadows and tactile embedded surfaces. | `neumorphism/DESIGN.md` |
| `pacman` | Retro arcade, pixel fonts, dotted borders, and 8-bit game aesthetics. | `pacman/DESIGN.md` |
| `paper` | Paper-textured, print-inspired, tactile surfaces with serif/sans typography. | `paper/DESIGN.md` |
| `perspective` | Isometric/spatial depth, vanishing points, and layered 3D-like realism. | `perspective/DESIGN.md` |
| `premium` | Apple-inspired polish, precise spacing, refined typography, and premium feel. | `premium/DESIGN.md` |
| `professional` | Business-ready trust, modern typography, structured layouts, and polished identity. | `professional/DESIGN.md` |
| `publication` | Books, magazines, reports, editorial grids, and expressive print typography. | `publication/DESIGN.md` |
| `refined` | Curated modern minimalism, elegant serif typography, and understated palettes. | `refined/DESIGN.md` |
| `retro` | Vintage-inspired typography, nostalgic palettes, and throwback visual elements. | `retro/DESIGN.md` |
| `shadcn` | shadcn/ui-style clean components, monochrome palette, and utility-first patterns. | `shadcn/DESIGN.md` |
| `simple` | No-frills clarity, neutral colors, intuitive layouts, and unobtrusive UI. | `simple/DESIGN.md` |
| `skeumorphism` | Real-world mimicry, textures, 3D effects, and familiar physical metaphors. | `skeumorphism/DESIGN.md` |
| `sleek` | Clean lines, intentional color, subtle interactions, and consistent spacing. | `sleek/DESIGN.md` |
| `spacious` | Generous whitespace, consistent padding, grid layouts, and breathing room. | `spacious/DESIGN.md` |
| `storytelling` | Narrative-driven visuals, copy, and interactions that guide users emotionally. | `storytelling/DESIGN.md` |
| `tetris` | Classic block-game energy, playful colors, compact layouts, and bold display fonts. | `tetris/DESIGN.md` |
| `vibrant` | Lively color, playful typography, warm accents, and dynamic visual energy. | `vibrant/DESIGN.md` |
| `vintage` | 1950s-1990s nostalgia, grain, retro palettes, pixel typography, and skeuomorphic touches. | `vintage/DESIGN.md` |

## How It Works

### Mode 1: Generate Design System

Analyzes your codebase and generates a cohesive design system:

```
1. Scan CSS/Tailwind/styled-components for existing patterns
2. Extract: colors, typography, spacing, border-radius, shadows, breakpoints
3. Research 3 competitor sites for inspiration (via browser MCP)
4. Propose a design token set (JSON + CSS custom properties)
5. Generate DESIGN.md with rationale for each decision
6. Create an interactive HTML preview page (self-contained, no deps)
```

Output: `DESIGN.md` + `design-tokens.json` + `design-preview.html`

### Mode 2: Visual Audit

Scores your UI across 10 dimensions (0-10 each):

```
1. Color consistency — are you using your palette or random hex values?
2. Typography hierarchy — clear h1 > h2 > h3 > body > caption?
3. Spacing rhythm — consistent scale (4px/8px/16px) or arbitrary?
4. Component consistency — do similar elements look similar?
5. Responsive behavior — fluid or broken at breakpoints?
6. Dark mode — complete or half-done?
7. Animation — purposeful or gratuitous?
8. Accessibility — contrast ratios, focus states, touch targets
9. Information density — cluttered or clean?
10. Polish — hover states, transitions, loading states, empty states
```

Each dimension gets a score, specific examples, and a fix with exact file:line.

### Mode 3: AI Slop Detection

Identifies generic AI-generated design patterns:

```
- Gratuitous gradients on everything
- Purple-to-blue defaults
- "Glass morphism" cards with no purpose
- Rounded corners on things that shouldn't be rounded
- Excessive animations on scroll
- Generic hero with centered text over stock gradient
- Sans-serif font stack with no personality
```

## Examples

**Generate for a SaaS app:**
```
/design-system generate --style minimal --palette earth-tones
```

**Audit existing UI:**
```
/design-system audit --url http://localhost:3000 --pages / /pricing /docs
```

**Check for AI slop:**
```
/design-system slop-check
```

