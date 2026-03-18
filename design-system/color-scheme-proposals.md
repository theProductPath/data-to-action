# SMJ Color Scheme Proposals
**Prepared by:** Desy 👩🏽‍💻  
**Date:** 2026-03-17  
**Purpose:** Replace the interim dark navy / purple-CTA default across the SMJ demo portfolio

---

## Current State (for reference)

The portfolio currently uses what I'd call the "Claude Default" — a dark navy base with purple CTAs that reads as AI-generated template to anyone who's seen more than two AI demos. It's not bad, but it's not *us*.

| Token | Current Value |
|---|---|
| Background | `#0f172a` |
| Surface/Card | `#1e293b` |
| CTAs | purple-based (`#6366f1` range) |
| Text | `#f1f5f9` / `#94a3b8` |

The onboarding demo notably breaks from this with white cards on a dark shell — which is actually closer to where we should be. That hybrid approach (dark chrome, light content) is worth preserving.

---

## Proposal 1: Obsidian & Ember

**Character:** Authoritative. Precise. The boardroom material.

### Rationale
Charcoal-to-near-black backgrounds communicate solidity and permanence — the kind of software that large organizations trust with real decisions. The ember accent (a deep warm amber-orange) is distinctive without being trendy. It reads as "strategic insight" rather than "startup energy." This scheme says: *we've done this before.*

### Palette

| Role | Token | Value | Notes |
|---|---|---|---|
| Background | `--color-bg` | `#111214` | Near-black with slight warm undertone |
| Surface | `--color-surface` | `#1c1e21` | Dark charcoal for sidebars/shells |
| Card | `--color-card` | `#25282d` | Lifted surface for cards |
| Card (light variant) | `--color-card-light` | `#f7f6f4` | For content-heavy panels |
| Primary CTA | `--color-primary` | `#d97706` | Amber-600 — confident, not garish |
| Primary hover | `--color-primary-hover` | `#b45309` | Amber-700 |
| Accent | `--color-accent` | `#f59e0b` | Amber-400 — highlights, active states |
| Text primary | `--color-text` | `#f0ede8` | Warm white — easier on eyes than pure white |
| Text secondary | `--color-text-muted` | `#9ca3af` | Gray-400 |
| Text on card | `--color-text-card` | `#1a1a1a` | For light card variant |
| Border | `--color-border` | `#2e3035` | Subtle separation |
| Success | `--color-success` | `#16a34a` | Green-600 |
| Warning | `--color-warning` | `#d97706` | Aligns with primary |
| Error | `--color-error` | `#dc2626` | Red-600 |
| Info | `--color-info` | `#0ea5e9` | Sky-500 |

### Mood
Understated power. The visual equivalent of a CFO who never raises their voice. Resonates with: finance, legal, ops leadership. Works equally well in dark mode (shell) and light mode (content panels).

### Risk ⚠️
Amber is associated with "caution" in some contexts (think warning states, traffic lights). The semantic warning color will need to differentiate clearly — likely via icon/label rather than color alone.

---

## Proposal 2: Slate & Sage

**Character:** Considered. Human. Quietly sophisticated.

### Rationale
Enterprise buyers are fatigued by aggressive CTA colors and high-contrast dark UIs. Slate & Sage leans into restraint — a cool neutral base with a muted sage green accent that signals *thoughtfulness* over *urgency*. This is the scheme for clients who've been burned by flashy tech before and want something that feels like it was made by people, for people.

The sage green also implicitly aligns with growth themes — without being Calendly-basic.

### Palette

| Role | Token | Value | Notes |
|---|---|---|---|
| Background | `--color-bg` | `#0e1117` | Cool near-black |
| Surface | `--color-surface` | `#171c25` | Slate-tinted dark |
| Card | `--color-card` | `#1e2533` | Mid-dark card |
| Card (light variant) | `--color-card-light` | `#f8f9fa` | Clean white-ish for content |
| Primary CTA | `--color-primary` | `#4d7c6f` | Sage-600 — calm, decisive |
| Primary hover | `--color-primary-hover` | `#3d6459` | Slightly deeper |
| Accent | `--color-accent` | `#6db39a` | Sage-400 — highlights, links |
| Text primary | `--color-text` | `#e8edf4` | Slightly cool white |
| Text secondary | `--color-text-muted` | `#8b95a8` | Blue-gray muted |
| Text on card | `--color-text-card` | `#1e2533` | |
| Border | `--color-border` | `#252d3a` | |
| Success | `--color-success` | `#4d7c6f` | Aligns with primary |
| Warning | `--color-warning` | `#d97706` | Amber — contrast with sage |
| Error | `--color-error` | `#dc2626` | |
| Info | `--color-info` | `#3b82f6` | |

### Mood
A senior HR leader or Chief of Staff reviewing this demo would feel comfortable. It doesn't perform — it *presents*. Calm confidence, not bravado. Best for demos targeting people-focused buyers (HR, onboarding, knowledge management).

### Risk ⚠️
Sage green CTAs may not have sufficient click-urgency for lower-context users. We'd want to be deliberate with CTA copy — the button needs to work harder than the color. Also: at low contrast ratios, sage-on-dark needs WCAG validation.

---

## Proposal 3: Ink & Signal

**Character:** Sharp. Modern. Unapologetically intelligent.

### Rationale
This scheme doesn't apologize for being AI-forward — it leans into it. The base is a deep cool ink (almost midnight blue, but desaturated) paired with a vivid electric teal/cyan signal color. This is what "AI for enterprises" looks like when you make it *intentional* rather than default. It's bold, but controlled — the signal color is used sparingly, like a laser pointer in a dark room.

The key differentiator from the Claude purple default: teal-cyan is associated with clarity, precision, and real-time intelligence. Purple reads as "AI tool." Teal reads as "competitive advantage."

### Palette

| Role | Token | Value | Notes |
|---|---|---|---|
| Background | `--color-bg` | `#080e14` | Deep ink — darker than navy |
| Surface | `--color-surface` | `#0f1923` | Dark blue-tinted |
| Card | `--color-card` | `#182030` | Mid-dark card |
| Card (light variant) | `--color-card-light` | `#f5f8fc` | Slightly blue-tinted white |
| Primary CTA | `--color-primary` | `#0e9488` | Teal-600 — vivid, decisive |
| Primary hover | `--color-primary-hover` | `#0c7a6f` | |
| Accent | `--color-accent` | `#2dd4bf` | Teal-300 — for highlights, icons |
| Accent glow | `--color-accent-glow` | `rgba(45,212,191,0.12)` | For hover halos, focus rings |
| Text primary | `--color-text` | `#e4eef8` | Cool bright white |
| Text secondary | `--color-text-muted` | `#7a8fa6` | Desaturated blue-gray |
| Text on card | `--color-text-card` | `#0f1923` | |
| Border | `--color-border` | `#1e2d3d` | |
| Success | `--color-success` | `#10b981` | Emerald — family of teal |
| Warning | `--color-warning` | `#f59e0b` | Amber — clear contrast |
| Error | `--color-error` | `#f43f5e` | Rose — warmer than pure red |
| Info | `--color-info` | `#38bdf8` | Sky — distinct from teal |

### Mood
C-suite tech buyers. CIOs, CTOs, Chiefs of Staff who've been around the block and want to see something that looks like it was *designed* with intention. The demos feel like a product pitch, not a prototype. High energy without being aggressive.

### Risk ⚠️
This is the boldest option. If executed poorly, it can slide back into "AI demo aesthetic." Execution discipline matters — the signal/accent color must be used at maximum 20% coverage or it overwhelms. Also: the AI Room demo's existing teal (`#4ecdc4`) already overlaps with this scheme, which is either convenient or confusing depending on how we handle the transition.

---

## My Recommendation

**Start with Proposal 3 (Ink & Signal)** for the main demo portfolio — it's the strongest brand signal and differentiates clearly from the Claude default.

**Apply Proposal 1 (Obsidian & Ember)** to any demos targeting finance or legal personas — the amber authority reads differently in those rooms.

**Hold Proposal 2 (Slate & Sage)** as the people-team variant — it's perfect for the Onboarding and SME Brain Dump demos if we ever want persona-specific skinning.

---

## Next Steps

1. **Jones reviews and picks a direction** (or says "none of the above")
2. If approved, I build out the full design system tokens for the chosen scheme
3. I produce a visual mockup via Nano Banana so you can see it rendered before Codey touches anything
4. Codey gets a spec, not a guess

---

*Design audit and proposals by Desy 👩🏽‍💻 — 2026-03-17*
