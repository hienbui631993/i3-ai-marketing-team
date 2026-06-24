---
name: data-visualization
description: >-
  Turn campaign/marketing data into an on-brand, interactive i3 International
  dashboard (HTML/JS charts) with top-line metrics and key takeaways. Use for
  dashboards/data-viz tasks. Saves to marketing/working/reports/.
---

# Data Visualization / Dashboard — i3 International

Build an interactive, on-brand dashboard that visualizes campaign performance —
a reusable, on-brand "template" to refresh as new data arrives.

## Before building — load context
Read `marketing/context/style-guide.md` (brand colors/font) and pair with the
**Campaign Report** skill (it supplies the analysis; this supplies the visuals).

## Brand application
- Chart palette: Brand Blue `#00588F`, Dark Blue `#002447`, plus Pink `#DF1E71`,
  Green `#00A661`, Yellow `#FFC107` for series differentiation.
- Font: Helvetica Neue stack. Clean, labeled, legible.

## Inputs to confirm
- Dataset(s) + meaning · metrics/KPIs to feature · period & comparison baseline
- Output preference (self-contained HTML is default).

## Build
1. **Top-line metric cards** — the headline KPIs with deltas vs. baseline.
2. **Charts** — pick the right type per question: trend (line), channel mix (bar/donut),
   week-over-week (column), funnel (bar). One idea per chart, clearly labeled.
3. **Interactivity** — hover tooltips, and (where useful) toggles/filters. Use a
   lightweight approach (e.g. Chart.js via CDN, or inline SVG) in a single HTML file.
4. **Key takeaways** — a short text panel summarizing what the charts show.
5. Don't fabricate data — render only what's provided; mark gaps.

## Output
- Save as `marketing/working/reports/dashboard-<campaign>.html` (self-contained).
- Note how to refresh it with new data (which fields to update).

## Quality check
- [ ] Brand palette + font; charts labeled and accurate to the data.
- [ ] Top-line cards + interactive charts + takeaways.
- [ ] Self-contained and refreshable; no invented numbers.
