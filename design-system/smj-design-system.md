# SMJ Design System — v1.0
**Scheme:** The Sibling  
**Author:** Desy 👩🏽‍💻  
**Date:** 2026-03-17  
**Status:** Approved by Jones — ready for implementation

---

## Overview

The Sibling is SMJ's visual identity system. It shares DNA with theProductPath.com (burnt orange anchor, dark backgrounds, warm text) but gives SMJ its own depth — a cooler, denser charcoal-slate shell that reads as a distinct product, not just a reskinned website.

**Brand relationship:** SMJ is a sibling of theProductPath, not a clone. Same family, own personality.

---

## Color Tokens

### Core Backgrounds

| Token | Value | Usage |
|---|---|---|
| `--color-bg` | `#181d26` | Page/app background — deep cool charcoal-slate |
| `--color-surface` | `#222831` | Sidebars, navigation shells, secondary panels |
| `--color-card` | `#2a303c` | Card surfaces, modal backgrounds, elevated panels |
| `--color-card-hover` | `#30374a` | Card hover state |
| `--color-card-light` | `#f6f6f6` | Light variant for content-heavy panels (tables, long-form) |

### Brand / Primary

| Token | Value | Usage |
|---|---|---|
| `--color-primary` | `#c75c2a` | Primary CTAs, active nav, key highlights — burnt orange |
| `--color-primary-hover` | `#a84a20` | CTA hover state |
| `--color-primary-subtle` | `rgba(199,92,42,0.12)` | Hover halos, focus rings, subtle backgrounds |
| `--color-primary-text` | `#e8865a` | Orange used in body text contexts (links, labels on dark) |

### Text

| Token | Value | Usage |
|---|---|---|
| `--color-text` | `#e4eaf4` | Primary body text on dark backgrounds |
| `--color-text-muted` | `#8895aa` | Secondary text, placeholders, metadata |
| `--color-text-disabled` | `#555f70` | Disabled states |
| `--color-text-on-primary` | `#ffffff` | Text on burnt orange backgrounds |
| `--color-text-on-light` | `#1e2533` | Text on `--color-card-light` surfaces |
| `--color-text-muted-on-light` | `#5a6478` | Muted text on light surfaces |

### Borders & Dividers

| Token | Value | Usage |
|---|---|---|
| `--color-border` | `#2e3848` | Standard borders — subtle, cool |
| `--color-border-strong` | `#3d4a5c` | Emphasized borders, active card outlines |
| `--color-border-light` | `#e2e6ef` | Borders on light card surfaces |

### Semantic Colors

| Token | Value | Usage |
|---|---|---|
| `--color-success` | `#16a34a` | Success states, completion badges |
| `--color-success-subtle` | `rgba(22,163,74,0.12)` | Success backgrounds |
| `--color-warning` | `#d97706` | Warning states (distinct from primary orange) |
| `--color-warning-subtle` | `rgba(217,119,6,0.12)` | Warning backgrounds |
| `--color-error` | `#dc2626` | Error states |
| `--color-error-subtle` | `rgba(220,38,38,0.12)` | Error backgrounds |
| `--color-info` | `#3b82f6` | Info states, neutral highlights |
| `--color-info-subtle` | `rgba(59,130,246,0.12)` | Info backgrounds |

### AI Room Level Colors (PRESERVED — do not replace)

These are functional game-mechanic colors. The shell gets The Sibling treatment; these level colors stay as-is.

| Token | Value | Level |
|---|---|---|
| `--level-follow` | `#4ecdc4` | Follow (beginner) |
| `--level-join` | `#ffffff` | Join |
| `--level-start` | `#f7b731` | Start |
| `--level-drive` | `#e94560` | Drive (advanced) |

---

## Typography

### Font Stack
```css
--font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'JetBrains Mono', 'Fira Code', 'Courier New', monospace;
```

> **Note for Codey:** Inter is preferred. If not already loaded, add via Google Fonts: `https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap`

### Type Scale

| Token | Size | Weight | Usage |
|---|---|---|---|
| `--text-xs` | `11px` | 400/500 | Metadata, timestamps, micro-labels |
| `--text-sm` | `13px` | 400 | Secondary body, captions |
| `--text-base` | `15px` | 400 | Primary body text |
| `--text-md` | `16px` | 500/600 | Card titles, form labels |
| `--text-lg` | `20px` | 600 | Section headings |
| `--text-xl` | `24px` | 700 | Page headings |
| `--text-2xl` | `32px` | 700 | Hero headings |

### Letter Spacing
- Labels/badges: `0.04em` (slightly tracked out)
- Headings: `-0.01em` (slightly tighter)
- Body: `0`

---

## Spacing

Base unit: `4px`

| Token | Value |
|---|---|
| `--space-1` | `4px` |
| `--space-2` | `8px` |
| `--space-3` | `12px` |
| `--space-4` | `16px` |
| `--space-5` | `20px` |
| `--space-6` | `24px` |
| `--space-8` | `32px` |
| `--space-10` | `40px` |
| `--space-12` | `48px` |
| `--space-16` | `64px` |

---

## Border Radius

| Token | Value | Usage |
|---|---|---|
| `--radius-sm` | `4px` | Badges, tags, small chips |
| `--radius-md` | `8px` | Cards, inputs, buttons |
| `--radius-lg` | `12px` | Modals, large panels |
| `--radius-xl` | `16px` | Feature cards |
| `--radius-full` | `9999px` | Pills, avatars |

---

## Elevation / Shadow

| Token | Value | Usage |
|---|---|---|
| `--shadow-sm` | `0 1px 3px rgba(0,0,0,0.3)` | Subtle card lift |
| `--shadow-md` | `0 4px 12px rgba(0,0,0,0.4)` | Cards, dropdowns |
| `--shadow-lg` | `0 8px 24px rgba(0,0,0,0.5)` | Modals, floating panels |
| `--shadow-primary` | `0 4px 16px rgba(199,92,42,0.25)` | Primary CTA buttons (hover) |

---

## Component Patterns

### Navigation Bar
```
Background: --color-surface
Height: 56px
Logo/wordmark: --color-primary (burnt orange) + --color-text
Border-bottom: 1px solid --color-border
Active nav item: --color-primary, font-weight 600
Inactive nav item: --color-text-muted, hover → --color-text
```

### Primary Button
```
Background: --color-primary
Text: --color-text-on-primary
Border-radius: --radius-md
Padding: 10px 20px
Font: --text-md, weight 600
Hover: --color-primary-hover + --shadow-primary
Active: scale(0.98)
Disabled: opacity 0.4, no hover effect
```

### Secondary Button / Ghost
```
Background: transparent
Border: 1px solid --color-border-strong
Text: --color-text
Hover: background --color-card-hover, border --color-primary
```

### Card
```
Background: --color-card
Border: 1px solid --color-border
Border-radius: --radius-md
Padding: --space-6
Hover (interactive cards): border-color --color-primary, --shadow-md
```

### Badge / Tag
```
Border-radius: --radius-sm
Font: --text-xs, weight 500, letter-spacing 0.04em
Text-transform: uppercase
Padding: 2px 8px
```

Use semantic colors for status badges (success/warning/error/info), with the `-subtle` variant as background and full color as text.

### Input / Form Field
```
Background: --color-surface
Border: 1px solid --color-border
Border-radius: --radius-md
Text: --color-text
Placeholder: --color-text-muted
Focus: border-color --color-primary, box-shadow 0 0 0 3px --color-primary-subtle
```

### Kanban Column (Onboarding demo)
```
Background: rgba(42,48,60,0.5)  /* --color-card at 50% */
Header: --color-text-muted, font --text-sm weight 600 uppercase
Cards within: --color-card, hover border --color-primary
```

---

## Motion & Interaction

| Property | Value |
|---|---|
| Transition default | `150ms ease` |
| Transition smooth | `200ms ease-out` |
| Hover scale (cards) | `transform: translateY(-1px)` |
| Button active | `transform: scale(0.98)` |

Keep motion subtle. These are enterprise tools — nothing bounces.

---

## Implementation Notes for Codey

### CSS Variable Block

Add this to the `:root` of each demo:

```css
:root {
  /* Backgrounds */
  --color-bg: #181d26;
  --color-surface: #222831;
  --color-card: #2a303c;
  --color-card-hover: #30374a;
  --color-card-light: #f6f6f6;

  /* Brand */
  --color-primary: #c75c2a;
  --color-primary-hover: #a84a20;
  --color-primary-subtle: rgba(199,92,42,0.12);
  --color-primary-text: #e8865a;

  /* Text */
  --color-text: #e4eaf4;
  --color-text-muted: #8895aa;
  --color-text-disabled: #555f70;
  --color-text-on-primary: #ffffff;
  --color-text-on-light: #1e2533;
  --color-text-muted-on-light: #5a6478;

  /* Borders */
  --color-border: #2e3848;
  --color-border-strong: #3d4a5c;
  --color-border-light: #e2e6ef;

  /* Semantic */
  --color-success: #16a34a;
  --color-success-subtle: rgba(22,163,74,0.12);
  --color-warning: #d97706;
  --color-warning-subtle: rgba(217,119,6,0.12);
  --color-error: #dc2626;
  --color-error-subtle: rgba(220,38,38,0.12);
  --color-info: #3b82f6;
  --color-info-subtle: rgba(59,130,246,0.12);

  /* Typography */
  --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', monospace;

  /* Spacing */
  --space-1: 4px; --space-2: 8px; --space-3: 12px; --space-4: 16px;
  --space-5: 20px; --space-6: 24px; --space-8: 32px; --space-10: 40px;
  --space-12: 48px; --space-16: 64px;

  /* Radius */
  --radius-sm: 4px; --radius-md: 8px; --radius-lg: 12px;
  --radius-xl: 16px; --radius-full: 9999px;

  /* Shadow */
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.3);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.4);
  --shadow-lg: 0 8px 24px rgba(0,0,0,0.5);
  --shadow-primary: 0 4px 16px rgba(199,92,42,0.25);
}
```

### Demo-Specific Notes

| Demo | Approach |
|---|---|
| **Onboarding** | Replace `--bg`, `--bg-surface`, `--accent`, `--accent-light` with system tokens. White cards (`--bg-card: #ffffff`) → swap to `--color-card`. Tag colors (pre/day1/week1 etc.) are functional — preserve them. |
| **Interview (Individual & Team)** | Straightforward token swap. Owner color badges (manager/hire/buddy/hr) are functional — preserve. |
| **SME Brain Dump** | Full token swap. No functional color dependencies. |
| **AI Room** | Shell only: `--room-bg`, `--floor`, `--wall`, `--card-bg`, `--card-border`, `--text`, `--text-muted`. **Do NOT touch `--level-follow`, `--level-join`, `--level-start`, `--level-drive`.** |
| **Demo Hub** | Apply system tokens to nav, cards, CTAs. This is the highest-value single change — it's the first thing clients see. |

---

*Design System v1.0 — SMJ / The Sibling — Desy 👩🏽‍💻 — 2026-03-17*
