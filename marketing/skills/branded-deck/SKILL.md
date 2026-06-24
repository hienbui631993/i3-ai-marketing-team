---
name: branded-deck
description: >-
  Create an on-brand i3 International slide deck (sales, strategy, product, or
  reporting) following i3's branded template and the official brand kit. Use for
  any presentation/deck task. Reference-based. Saves .pptx to marketing/working/presentations/.
---

# Branded Deck — i3 International

Build polished, on-brand decks using the **reference-based method**: study i3's
template + brand kit, then generate slides that match exactly.

## References (study these first)
1. **Brand kit & assets:** `marketing/context/style-guide.md` and the source files in
   `/i3 Media Kit/` (logos, colors, fonts).
   - Colors: Brand Blue `#00588F`, Dark Blue `#002447`; accents Pink `#DF1E71`,
     Green `#00A661`, Yellow `#FFC107`.
   - Font: **Helvetica Neue** (use a close fallback like Arial/Helvetica if unavailable).
   - Logo: marketing logo **with tagline** on slides; white logo on dark backgrounds.
     Files in `/i3 Media Kit/i3 Logo/`.
2. **Deck template:** if a branded `.pptx`/template exists in
   `marketing/templates/branded-deck/`, **analyze it first** (layouts, master slides,
   margins, type scale, chart styling) and follow it exactly. If none exists yet,
   flag `[needs template]` and build from the brand kit using the layout below.

## How to build
- Extend the official **PowerPoint (pptx) skill** for file generation; this skill
  supplies the i3 brand layer (colors, fonts, logo, layout rules).
- Apply brand colors and Helvetica Neue throughout; logo + page number on every slide.
- One idea per slide; charts use the brand palette (blue base, expression-color accents).
- Respect logo safe zone and minimum size (see style guide).

## Default layout (when no specific structure given)
1. Title (Dark Blue hero + white logo w/ tagline)
2. Agenda
3. Problem / context
4. Solution (feature → benefit; name real i3 solutions)
5. How it works
6. Proof / results (`[confirm]` any stat)
7. Pricing/offer (if relevant)
8. Call to action / contact

## Inputs to confirm
- Deck purpose (sales, strategy, product launch, client report) · audience
- Key messages / content source · # slides target · any required sections

## Output
- Save as `marketing/working/presentations/<deck-name>.pptx`.
- Note in the hand-off any slides that need manual polish (charts, margins) — the
  reference method gets ~90% there; flag the last 10%.

## Quality check
- [ ] Brand colors + Helvetica Neue applied; correct logo variant per background.
- [ ] One idea per slide; consistent margins; logo + page number on each.
- [ ] Matches `templates/branded-deck/` if present; else `[needs template]` noted.
- [ ] No fabricated proof (`[confirm]`).
