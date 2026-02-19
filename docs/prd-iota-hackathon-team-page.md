# PRD: IOTA Hackathon Team Page

**Project:** Team TEAMname — Masterz x IOTA EU Hackathon Promotion Site  
**Owner:** Ward  
**Date:** 18 February 2026  
**Status:** v1 wireframe complete, ready for development

---

## Context

We're participating in the Masterz x IOTA EU hackathon. Today there's a prize for showcasing existing work, so we need a simple promotion page for our team. The page is a **living document** — it starts minimal and evolves week by week as the project progresses.

### Team

| Name | Role | Location |
|------|------|----------|
| Ward | Founder & Product | Belgium |
| Stephanos | TBD | TBD |
| Omar | TBD | TBD |

### What We're Building

Product transparency infrastructure, verifiable on IOTA — enabling verifiable, tamper-proof product lifecycle data for supply chain transparency and compliance.

---

## Design Direction

### Style: IOTA-first with TEAMname references

The page should follow **IOTA's visual identity** since they organized the hackathon. TEAMname branding is secondary/referenced, not dominant.

**IOTA brand colors (from Brandfetch):**
- Electric Blue: `#0101FF`
- Lavender/Melrose: `#A59AFA`
- Navy Blue: `#000060`
- Dark backgrounds, clean modern typography
- Line-graphic style, smooth animations
- Spacious, lightweight feel

**TEAMname references (subtle):**
- Charcoal Black: `#1A1A1A`
- Off-White: `#F8F8F7`
- Sage accent: `#88927D` (use sparingly if at all)

### Current State: Black & White Wireframe

v1 is intentionally a pure B&W structural wireframe. No color, no decoration. The plan is to **layer in the IOTA visual identity progressively** over the coming weeks.

### Typography (wireframe)

- Sans: IBM Plex Sans (300, 400, 500, 600, 700)
- Mono: IBM Plex Mono (400, 500, 600)
- Can evolve to match IOTA's type system later

---

## Page Structure

### Header
- `TEAMname × IOTA` logo lockup (mono, uppercase, small)
- Badge: `Masterz × IOTA EU`

### Hero Section
- Large headline: "Product Transparency Infrastructure"
- One-liner subtitle explaining what the team is doing
- Lightweight, no imagery

### 01 — Team
- 3-column grid (stacks on mobile)
- Each member: name, role, location
- Separated by 1px borders (table-like, minimal)
- Roles and locations for Stephanos and Omar need to be filled in

### 02 — Problem
- Single statement paragraph
- Key date (Feb 2027) underlined for emphasis
- Placeholder marker `↓ refine as project scopes`

### 03 — What We're Building
- Single statement paragraph describing the technical approach
- Placeholder marker `↓ technical details to follow`

### 04 — Impact
- Single statement paragraph on the vision
- Placeholder marker `↓ metrics & scope evolving`

### 05 — Build Log ⭐ (key feature)
- Reverse-chronological entries
- Each entry has:
  - **Date** (left column, mono font)
  - **Title** (bold)
  - **Description** (gray body text)
  - **Tags** (small bordered pills): `meeting`, `decision`, `link`, `build`, `upcoming`
  - **Links** (optional): to demos, repos, docs
- This section grows weekly — it's the living heart of the page
- Grid layout: `120px date | 1fr content`
- Stacks to single column on mobile

### Footer
- Links to teamname.eu and iota.org
- Minimal, centered

---

## Evolution Plan

The page is designed to grow over the hackathon month:

| Week | What Changes |
|------|-------------|
| **Week 1 (now)** | B&W wireframe, team info, initial problem/solution statements, first log entry |
| **Week 2** | Add IOTA colors and visual styling, refine problem/build/impact copy, more log entries |
| **Week 3** | Add links to demos/repos, screenshots or embeds of work, richer log entries |
| **Week 4** | Final polish, results, full build log as project narrative |

---

## Technical Notes

### Current Implementation
- Single `index.html` file (inline CSS, no JS)
- Google Fonts: IBM Plex Sans + IBM Plex Mono
- Responsive: mobile-first, grid stacks at 600px
- No build tools, no framework — just HTML/CSS
- Can be deployed anywhere (Vercel, Netlify, static hosting)

### Keep It Simple
- No JavaScript required for v1
- No images for now
- No animations yet (can add later with IOTA styling phase)
- Semantic HTML, clean structure
- Easy to update — a developer should be able to add a log entry in under a minute

### Log Entry Template

To add a new build log entry, copy this block:

```html
<div class="log-entry">
  <div class="log-date">DD Mon YYYY</div>
  <div class="log-content">
    <h3>Entry title</h3>
    <p>What happened, what was decided, what was built.</p>
    <span class="log-tag">meeting</span>
    <span class="log-tag">decision</span>
    <a href="#" class="log-link">Link to thing →</a>
  </div>
</div>
```

---

## Open Questions

- [x] Hackathon name confirmed: Masterz x IOTA EU hackathon
- [ ] Stephanos — role and location
- [ ] Omar — role and location  
- [ ] What existing work to showcase for today's prize (MoMu/MoMuse? 3D viewers? DPP platform?)
- [ ] Deployment target (Vercel? Subdomain of teamname.eu?)
- [ ] Should the build log eventually pull from Notion or stay manual HTML?

---

## Reference Files

- **Wireframe:** `index.html` (delivered alongside this PRD)
- **IOTA website:** [iota.org](https://www.iota.org) — reference for visual evolution
- **IOTA brand assets:** [assets.iota.org](https://assets.iota.org)
- **IOTA brand colors:** `#0101FF` (blue), `#A59AFA` (lavender), `#000060` (navy)
- **TEAMname brand system:** See project knowledge base (Emma Rousseau's brand guidelines)
