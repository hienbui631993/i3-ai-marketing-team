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
2. **Deck template (analyzed):** the reference deck lives at
   `marketing/templates/branded-deck/i3 branded deck.pptx` (Git LFS, ~327 MB) and its
   full analysis is in [`marketing/templates/branded-deck/ANALYSIS.md`](../../templates/branded-deck/ANALYSIS.md).
   **Read the analysis first** and follow the template exactly.

### Template style (follow this for decks — supersedes brand-kit defaults)
The approved deck applies branding on-slide and **diverges from the brand kit**:
- **Font: Montserrat** (not Helvetica Neue).
- **Primary dark: `#0A1428`** (near-black navy); **accent: `#FF007D`** (magenta); text white.
- **16:9** (13.333in × 7.5in); dark, cinematic, full-bleed media; one idea per slide.
- Brand-kit equivalents (`#002447` / `#DF1E71` / Helvetica Neue) are the official
  alternative — see the `[confirm]` note in ANALYSIS.md. Until i3 says otherwise, **match the template.**

### Narrative flow to reuse (corporate/sales overview)
Cover → About i3 (37+ yr, family-driven, 4 key areas) → "Core applications" divider →
Safety & Security → Asset Protection → Operational Insights → Predictive Analytics →
per-vertical (divider + value prop: QSR / Grocery / C-Store / Retail) → impact → partnership close → contact.
Adapt the sections for product- or campaign-specific decks.

## How to build
- Extend the official **PowerPoint (pptx) skill** for file generation; this skill
  supplies the i3 template layer (Montserrat, `#0A1428`/`#FF007D`, layout + flow).
- Apply the template style throughout; logo per `style-guide.md` (white logo on the dark base).
- One idea per slide; **bold/magenta the key phrases**; capability lists map to real
  solutions in `product-offerings.md`.
- **Keep new decks lean** — the template's 327 MB is embedded video; only embed media when needed.

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
