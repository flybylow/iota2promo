# Design System Application

**Date:** 18 February 2026

## Summary

Applied the design system from `design-system.md` to the `index.html` page.

## Changes Applied

### Typography
- ✅ Changed fonts from IBM Plex to **Inter** (sans) and **JetBrains Mono** (mono)
- ✅ Updated hero headline size to `clamp(36px, 5vw, 64px)` with weight 300
- ✅ Updated body text to 15px (was 16px)
- ✅ Updated section labels to match design system specs (11px, mono, uppercase, 0.15em tracking)

### Colors
- ✅ Replaced custom color variables with design system tokens:
  - `--bg-primary: #000000` (was `--black: #0a0a0a`)
  - `--text-primary: #FFFFFF` (was `--white: #f5f5f5`)
  - `--text-secondary: #8A8A9A` (was `--gray: #888`)
  - `--bg-border: #1E1E2A` (was `--border: #222`)
- ✅ Added IOTA brand color tokens (ready for v2+):
  - `--iota-blue: #0101FF`
  - `--iota-lavender: #A59AFA`
  - `--iota-navy: #000060`

### Spacing
- ✅ Replaced hardcoded spacing values with design system tokens:
  - `--space-xs: 4px`
  - `--space-sm: 8px`
  - `--space-md: 16px`
  - `--space-lg: 24px`
  - `--space-xl: 48px`
  - `--space-2xl: 64px`
  - `--space-3xl: 96px`

### Components
- ✅ Updated all components to use design system tokens
- ✅ Team cards use `--bg-primary` background
- ✅ Log entries use proper spacing tokens
- ✅ Tags use design system border and color tokens
- ✅ Links use `--bg-border` for underlines

## Current State

The page now follows the design system v1 (B&W wireframe phase). All tokens are in place for future evolution:
- v2: Introduce IOTA blue accents
- v3: Add IOTA lavender and animations
- v4: Full IOTA visual treatment

## Notes

- Design system is documented in `docs/design-system.md`
- All color tokens are ready for v2+ evolution
- Typography and spacing now match design system specifications
- No border-radius applied (sharp rectangles as per design system)
