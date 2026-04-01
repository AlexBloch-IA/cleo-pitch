# Cleo Insight — Brand Guidelines

## Philosophy

Inspired by Jony Ive's design philosophy: **reduction to essence**. Every element earns its place. White space is not empty — it's the product breathing. The brand communicates authority and trust through restraint, not through visual noise.

---

## Colors

### Primary Palette

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Brand Purple** | `#7c3aed` | 124, 58, 237 | CTA buttons, badges, key accents — use **very** sparingly |
| **Purple Dark** | `#6d28d9` | 109, 40, 217 | Hover states on purple elements |
| **Purple Light** | `#ede9fe` | 237, 233, 254 | Light backgrounds, tags, subtle highlights |
| **Purple 50** | `#f5f3ff` | 245, 243, 255 | Barely-there purple tint for sections |

### Neutral Palette

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Black** | `#0a0a0a` | 10, 10, 10 | Headings, primary text, dark sections |
| **Gray 800** | `#262626` | 38, 38, 38 | Secondary dark backgrounds, card borders |
| **Gray 600** | `#525252` | 82, 82, 82 | Body text, descriptions |
| **Gray 500** | `#737373` | 115, 115, 115 | Section labels, subtle text |
| **Gray 400** | `#a3a3a3` | 163, 163, 163 | Placeholders, muted text on dark |
| **Gray 200** | `#d4d4d4` | 212, 212, 212 | Borders, dividers |
| **Gray 100** | `#e8e8e8` | 232, 232, 232 | Light borders, card outlines |
| **Gray 50** | `#f5f5f5` | 245, 245, 245 | Soft section backgrounds |
| **White** | `#fafafa` | 250, 250, 250 | Primary background |

### AI Model Colors (pipeline context only)

| Model | Background | Text | Usage |
|-------|-----------|------|-------|
| Opus | `rgba(124,58,237,0.15)` | `#a78bfa` | Tags, badges for Opus references |
| Sonnet | `rgba(59,130,246,0.15)` | `#93c5fd` | Tags, badges for Sonnet references |
| Haiku | `rgba(16,185,129,0.15)` | `#6ee7b7` | Tags, badges for Haiku references |

### Color Rules

- Purple is the **single accent** — never use it on more than 1 element per section
- Never use purple-to-blue gradients (cliche AI aesthetic)
- Alternate white (`#fafafa`) and soft gray (`#f5f5f5`) section backgrounds
- Dark sections use `#0a0a0a` background with `#fafafa` text
- Borders are always 1px, never heavier
- No shadows on cards — use borders only (1px `#e8e8e8` on light, 1px `rgba(255,255,255,0.08)` on dark)

---

## Typography

### Font Stack

| Role | Font | Source | Fallbacks |
|------|------|--------|-----------|
| **Display / Headings** | Instrument Serif | Google Fonts | Georgia, serif |
| **Body / UI** | DM Sans | Google Fonts | -apple-system, sans-serif |

```html
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Instrument+Serif:ital@0;1&display=swap" rel="stylesheet">
```

### Type Scale

| Element | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|---------|------|------|--------|-------------|----------------|-------|
| **Display** | Instrument Serif | `clamp(3rem, 8vw, 6.5rem)` | 400 | 1.05 | -0.03em | Hero only |
| **H2** | Instrument Serif | `clamp(2.5rem, 5vw, 4rem)` | 400 | 1.1 | -0.02em | Section headings |
| **H3** | DM Sans | 1.25–1.35rem | 500–600 | 1.3 | 0 | Card titles, step names |
| **Subtitle** | DM Sans | `clamp(1rem, 1.5vw, 1.25rem)` | 400 | 1.7 | 0 | Max-width 640px |
| **Body** | DM Sans | 0.95rem | 400 | 1.7 | 0 | Descriptions, paragraphs |
| **Small** | DM Sans | 0.85rem | 400 | 1.5 | 0 | Feature lists, stat labels |
| **Label** | DM Sans | 0.75rem | 600 | 1.3 | 0.15em | UPPERCASE, section labels |
| **Micro** | DM Sans | 0.7rem | 600 | 1.3 | 0.12em | Tags, badges |

### Typography Rules

- **Instrument Serif italic** (`<em>`) is the accent — use it for the ONE key word per heading (e.g., "propulsée par l'*IA*")
- Never use italic serif for body text
- Section labels: UPPERCASE, 0.75rem, 600 weight, 0.15em letter-spacing, gray-500
- Numbers and stats: Instrument Serif at large sizes (3rem+), regular weight
- Never use bold serif — it only has Regular and Italic
- DM Sans ranges from 100 to 1000 weight — use 400 (body), 500 (H3), 600 (labels/buttons)

---

## Spacing

### Section Padding

| Context | Padding |
|---------|---------|
| Standard section | `120px` top/bottom, `40px` left/right |
| Featured sections (dark/CTA) | `140px` top/bottom |
| Mobile | `80px` top/bottom, `24px` left/right |

### Internal Spacing

| Element | Margin |
|---------|--------|
| Section label → H2 | 24px |
| H2 → Subtitle | 24px |
| Subtitle → Content | 48–72px |
| Card internal padding | 40–56px vertical, 32–40px horizontal |
| Grid gap (cards) | 24–48px |

### Max Widths

| Element | Max Width |
|---------|-----------|
| Content container | 1200px |
| Subtitle text | 640px |
| Full-bleed dark sections | 100vw (inner content 1200px) |

---

## Components

### Buttons

| Type | Background | Text | Border | Radius | Padding |
|------|-----------|------|--------|--------|---------|
| **Primary CTA** | `#7c3aed` | white | none | 100px (pill) | 20px 48px |
| **Secondary CTA** | `#0a0a0a` | white | none | 100px | 16px 36px |
| **Outline** | transparent | `#0a0a0a` | 1px `#d4d4d4` | 12px | 14px 24px |
| **Featured (on dark)** | `#7c3aed` | white | `#7c3aed` | 12px | 14px 24px |

Hover states:
- Primary CTA: `#6d28d9` + `scale(1.03)` + `box-shadow: 0 20px 60px rgba(124,58,237,0.25)`
- Secondary CTA: `#7c3aed` + `scale(1.02)`
- Outline: border-color → `#0a0a0a`

### Cards

| Context | Background | Border | Radius | Hover |
|---------|-----------|--------|--------|-------|
| Light section | `#fafafa` | 1px `#e8e8e8` | 16px | border → `#d4d4d4`, translateY(-2px) |
| Dark section | `rgba(255,255,255,0.03)` | 1px `rgba(255,255,255,0.08)` | 20px | border → `rgba(124,58,237,0.3)`, bg → `rgba(124,58,237,0.05)` |
| Featured (pricing) | `#0a0a0a` | none | inherited from grid | — |

### Badges / Tags

| Type | Background | Text | Radius | Size |
|------|-----------|------|--------|------|
| Recommended badge | `#7c3aed` | white | 100px | 0.65rem, 600, 0.1em spacing |
| Savings badge | `#7c3aed` | white | 6px | 0.7rem, 700 |
| Model tag (Opus) | `rgba(124,58,237,0.15)` | `#a78bfa` | 100px | 0.7rem, 600, 0.12em spacing |
| Model tag (Sonnet) | `rgba(59,130,246,0.15)` | `#93c5fd` | 100px | same |
| Model tag (Haiku) | `rgba(16,185,129,0.15)` | `#6ee7b7` | 100px | same |

### Tables (on dark background)

- No visible borders between cells — use `border-bottom: 1px solid rgba(255,255,255,0.06)`
- Header: 0.75rem, 500 weight, gray-400, UPPERCASE, 0.1em letter-spacing
- Cells: 0.95rem, padding 24px 32px
- Highlight row: `background: rgba(124,58,237,0.08)`, text white, last column `#a78bfa`

---

## Animation

### Reveal System

All content elements use a scroll-triggered reveal animation via Intersection Observer.

```css
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.9s cubic-bezier(0.25, 0.46, 0.45, 0.94),
              transform 0.9s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

- Duration: **0.9s** (slow, deliberate — not bouncy)
- Easing: `cubic-bezier(0.25, 0.46, 0.45, 0.94)` (gentle deceleration)
- Stagger: 0.1s increments (`.reveal-delay-1` through `.reveal-delay-5`)
- Observer threshold: 0.15 with `rootMargin: '0px 0px -40px 0px'`

### Counter Animation

Numbers count up when scrolled into view:
- Duration: 1800ms
- Easing: quartic ease-out (`1 - Math.pow(1 - progress, 4)`)
- Formatted with French locale (`toLocaleString('fr-FR')`)
- Triggered once (dataset flag prevents re-animation)

### Hover Transitions

- All transitions: `0.3s–0.4s ease`
- Cards: translateY(-2px) on hover
- Buttons: scale(1.02–1.03) on hover
- No bounce, no spring — always ease or ease-out

### Rules

- No animation on page load except hero elements
- Content reveals only when scrolled into view
- Never animate more than opacity + transform simultaneously
- No parallax effects
- No horizontal slide-ins — always vertical (translateY)

---

## Layout

### Grid System

- Max content width: 1200px, centered
- Stats/pipeline: 3–4 column grid with 1px gap (borders via background)
- Steps: 3 column grid, 48px gap
- Pricing: 4 column grid, 1px gap (borders via background)
- Economics: 4 column grid, 32px gap
- All grids collapse to 1 column on mobile (<600px), 2 columns on tablet (<900px)

### Section Rhythm

Alternate between:
1. White section (content on `#fafafa`)
2. Dark section (content on `#0a0a0a`, full bleed)
3. Soft section (content on `#f5f5f5`, full bleed)

Never stack two same-background sections.

### Responsive Breakpoints

| Breakpoint | Layout changes |
|-----------|----------------|
| > 900px | Full grid layouts |
| 600–900px | 2-column grids, reduced padding |
| < 600px | Single column, pricing stacks, table columns hidden |

---

## Tone of Voice

### French (primary)

- **Formal but not corporate** — "vous" form, professional but accessible
- **Precise** — exact numbers, not approximations ("981 régulations", not "des centaines")
- **Action-oriented** — every section ends with what to do next
- **No jargon** — explain AI in business terms, not technical terms
- Prices shown **HT** (hors taxes) — standard in French B2B

### Key phrases

- "Intelligence réglementaire propulsée par l'IA"
- "Diagnostic gratuit"
- "Signaux actionnables"
- "Prêt pour le board"

### Forbidden

- "Solution innovante" (empty buzzword)
- "Powered by AI" (say what the AI does, not that it exists)
- Exclamation marks in headings
- Emojis anywhere

---

## File Structure

```
cleo-pitch/
  index.html          # Single-page presentation (self-contained HTML/CSS/JS)
  BRAND-GUIDELINES.md  # This file
```

## CSS Variables Reference

```css
:root {
  --black: #0a0a0a;
  --white: #fafafa;
  --gray-50: #f5f5f5;
  --gray-100: #e8e8e8;
  --gray-200: #d4d4d4;
  --gray-400: #a3a3a3;
  --gray-500: #737373;
  --gray-600: #525252;
  --gray-800: #262626;
  --purple: #7c3aed;
  --purple-light: #ede9fe;
  --purple-50: #f5f3ff;
  --sans: 'DM Sans', -apple-system, sans-serif;
  --serif: 'Instrument Serif', Georgia, serif;
}
```
