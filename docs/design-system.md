# Design System: Tabulas × IOTA Hackathon Page

**Version:** 1.0  
**Date:** 18 February 2026  
**Context:** A promotional page for the IOTA hackathon. IOTA is primary visual language, Tabulas is referenced subtly.

---

## Philosophy

IOTA's brand is bold, spacious, and tech-forward — dark backgrounds, electric blues, clean geometry. Tabulas is restrained infrastructure confidence. The blend: **IOTA's energy with Tabulas' discipline.**

Think: IOTA's website meets a well-structured changelog.

---

## Color Tokens

### Backgrounds

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#000000` | Page background |
| `--bg-elevated` | `#0A0A0F` | Cards, sections with subtle lift |
| `--bg-surface` | `#12121A` | Log entries, team cards, hover states |
| `--bg-border` | `#1E1E2A` | Dividers, grid lines |

### Text

| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#FFFFFF` | Headlines, names, key content |
| `--text-secondary` | `#8A8A9A` | Body text, descriptions, dates |
| `--text-tertiary` | `#4A4A5A` | Placeholders, disabled, hints |

### IOTA Brand Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--iota-blue` | `#0101FF` | Primary accent — CTAs, key highlights, links |
| `--iota-lavender` | `#A59AFA` | Secondary accent — tags, hover states, subtle emphasis |
| `--iota-navy` | `#000060` | Deep accent — gradient anchors, section backgrounds |

### Tabulas Reference (used sparingly)

| Token | Hex | Usage |
|-------|-----|-------|
| `--tabulas-sage` | `#88927D` | Subtle Tabulas nod — one element max (e.g. "powered by Tabulas" text) |

### Functional

| Token | Hex | Usage |
|-------|-----|-------|
| `--status-live` | `#22C55E` | Active/live indicators |
| `--status-upcoming` | `#F59E0B` | Upcoming/planned items |

---

## Color Rules

1. **Background is always dark** — pure black or near-black with a blue undertone
2. **One accent system** — IOTA blue is the hero, lavender supports it
3. **90/10 rule still applies** — 90% monochrome/neutral, 10% IOTA blue
4. **No gradients in v1** — add later if evolving toward IOTA's full visual style
5. **Tabulas sage appears once max** — a watermark, not a theme

---

## Typography

### Font Stack

| Role | Font | Fallback | Google Fonts |
|------|------|----------|--------------|
| **Display** | Inter | system-ui, sans-serif | `Inter:wght@300;400;500;600;700` |
| **Mono** | JetBrains Mono | Consolas, monospace | `JetBrains+Mono:wght@400;500` |

Why Inter: it's clean, geometric, reads well at all sizes, and doesn't fight IOTA's visual identity. It bridges both brands — Tabulas uses it for body text, and it matches IOTA's modern tech aesthetic.

### Type Scale

| Token | Size | Weight | Line Height | Usage |
|-------|------|--------|-------------|-------|
| `--type-hero` | clamp(36px, 5vw, 64px) | 300 | 1.1 | Hero headline |
| `--type-h2` | 24px | 500 | 1.3 | Section headlines |
| `--type-h3` | 16px | 600 | 1.4 | Log entry titles, card names |
| `--type-body` | 15px | 400 | 1.6 | Paragraphs, descriptions |
| `--type-small` | 13px | 400 | 1.5 | Secondary info, locations |
| `--type-label` | 11px | 500 | 1.0 | Section labels, tags (mono, uppercase, tracked) |
| `--type-tiny` | 10px | 400 | 1.0 | Footer, legal (mono) |

### Typography Rules

- Hero headline is **light weight (300)** — confident, not shouting
- Section labels are **mono, uppercase, letter-spaced 0.15em** — structural markers
- Body text is **secondary color** — headlines own the contrast
- Tags and metadata are always **mono**
- No bold body text — use color or size for emphasis
- No italics except inside quotes

---

## Spacing

### Base Unit: 8px

| Token | Value | Usage |
|-------|-------|-------|
| `--space-xs` | 4px | Tight gaps (tag padding vertical) |
| `--space-sm` | 8px | List gaps, tight element spacing |
| `--space-md` | 16px | Paragraph gaps, card padding inner |
| `--space-lg` | 24px | Between related sections |
| `--space-xl` | 48px | Between major sections |
| `--space-2xl` | 64px | Section padding top/bottom |
| `--space-3xl` | 96px | Hero section breathing room |

### Page Layout

| Property | Value |
|----------|-------|
| Max width | `800px` |
| Side padding | `24px` (mobile), comfortable on desktop |
| Section padding | `64px` top and bottom |
| Section dividers | `1px solid var(--bg-border)` |

---

## Components

### Section Label
```
01 — Team
```
- Font: Mono, 11px, uppercase
- Color: `--text-secondary`
- Letter-spacing: 0.15em
- Margin-bottom: 32px

### Team Card
- Background: `--bg-primary` (transparent, separated by 1px borders)
- Grid: 3 columns, 1px gap (acts as border)
- Padding: 32px 24px per card
- Name: `--type-h3`, white
- Role: Mono, 12px, `--text-secondary`
- Location: 13px, `--text-secondary`, prefixed with `↳`

### Statement Block (Problem / Build / Impact)
- Font: 20px, weight 300, white
- Max-width: 640px
- Key terms: underlined with `--text-secondary` color border
- Placeholder pills below: mono, 12px, bordered, `--text-secondary`

### Build Log Entry
- Layout: `120px | 1fr` grid
- Date: Mono, 13px, `--text-secondary`, left column
- Title: 15px, weight 500, white
- Description: 14px, `--text-secondary`
- Tags: bordered pills, mono, 10px, uppercase
- Links: white text, underlined with `--bg-border`, brighten on hover

### Tag
```css
.tag {
  font-family: var(--font-mono);
  font-size: 10px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 3px 8px;
  border: 1px solid var(--bg-border);
  color: var(--text-secondary);
}
```

When IOTA colors are introduced (v2+):
- `meeting` tag → default border
- `decision` tag → `--iota-lavender` border
- `build` tag → `--iota-blue` border
- `link` tag → `--iota-blue` text

---

## Borders & Dividers

| Element | Style |
|---------|-------|
| Section divider | `1px solid var(--bg-border)` |
| Card grid gaps | `1px` background-color trick |
| Tag borders | `1px solid var(--bg-border)` |
| Link underlines | `1px solid var(--bg-border)`, white on hover |

No border-radius anywhere. Everything is sharp rectangles. This is infrastructure, not a consumer app.

---

## Motion (v2+, not in wireframe)

When evolving past wireframe:

| Element | Animation |
|---------|-----------|
| Page load | Staggered fade-in, sections appear 100ms apart |
| Log entries | Slide up + fade, 200ms, ease-out |
| Links | Underline color transition, 150ms |
| Tags | Border color transition, 150ms |
| Hero text | Subtle fade-in, 400ms, slight translateY |

No spring physics. No bounce. Clean, linear transitions. Think: terminal loading, not playful UI.

---

## Responsive Breakpoints

| Breakpoint | Changes |
|------------|---------|
| `> 800px` | Max-width container, comfortable reading |
| `≤ 600px` | Team grid → single column, log grid → stacked, header stacks |

Mobile is first-class. Most hackathon judges browse on phones.

---

## Evolution Roadmap

| Phase | Design Changes |
|-------|---------------|
| **v1 (now)** | Pure B&W wireframe. No accent colors. Structure only. |
| **v2 (week 2)** | Introduce `--iota-blue` for one accent element. Blue undertone on backgrounds. Colored tags. |
| **v3 (week 3)** | IOTA lavender as secondary accent. Subtle animations. Team photos (B&W). Links to live demos. |
| **v4 (week 4)** | Full IOTA visual treatment. Possible hero animation. Results section. Complete build log narrative. |

---

## CSS Variables (copy-paste ready)

```css
:root {
  /* Backgrounds */
  --bg-primary: #000000;
  --bg-elevated: #0A0A0F;
  --bg-surface: #12121A;
  --bg-border: #1E1E2A;

  /* Text */
  --text-primary: #FFFFFF;
  --text-secondary: #8A8A9A;
  --text-tertiary: #4A4A5A;

  /* IOTA */
  --iota-blue: #0101FF;
  --iota-lavender: #A59AFA;
  --iota-navy: #000060;

  /* Tabulas (one-off use) */
  --tabulas-sage: #88927D;

  /* Functional */
  --status-live: #22C55E;
  --status-upcoming: #F59E0B;

  /* Typography */
  --font-sans: 'Inter', system-ui, sans-serif;
  --font-mono: 'JetBrains Mono', Consolas, monospace;

  /* Spacing */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 48px;
  --space-2xl: 64px;
  --space-3xl: 96px;
}
```

---

## Quick Do / Don't

| ✓ Do | ✗ Don't |
|------|---------|
| Dark backgrounds, always | Light mode (not for this project) |
| Sharp corners, no radius | Rounded corners |
| Mono for metadata | Mono for body text |
| One IOTA blue accent | Multiple competing colors |
| Generous whitespace | Cramped layouts |
| 1px borders for structure | Thick borders, drop shadows |
| Real content or nothing | Lorem ipsum, placeholder images |
| Underlines for links | Colored link text without underline |
