---
name: campaign-report
description: >-
  Analyze campaign/marketing datasets and produce an i3 International performance
  report with channel breakdowns, insights, and recommendations. Use for reporting
  tasks. Saves to marketing/working/reports/.
---

# Campaign Report — i3 International

Synthesize raw campaign data into a clear, decision-ready report. This is an
**analysis** task — find the story in the numbers.

## Before starting — load context
Read `marketing/context/marketing-strategy.md` (KPIs, channels, funnel) and
`style-guide.md` (brand formatting). Pair with the **Data Visualization** skill for charts.

## Inputs to confirm
- The dataset(s) + their meaning/columns · the period covered · the campaign/KPIs
- Comparison baseline (prior period / target) · audience for the report.

## Method
1. **Validate** the data — note gaps, anomalies, assumptions (don't invent missing data).
2. **Top-line summary** — headline results vs. KPI/baseline, up front.
3. **Channel breakdown** — performance per channel (traffic, leads, conversion, cost, ROI).
4. **Trends** — week-over-week / period-over-period movements.
5. **Insights** — *why* the numbers moved; what worked / didn't.
6. **Recommendations** — specific next actions.
7. Hand chart specs to **Data Visualization** for the dashboard.

## Output (`marketing/working/reports/report-<campaign>-<period>.md`)
- Executive summary → KPI scorecard → channel tables → trend analysis → insights →
  recommendations. On-brand headings; numbers as numerals.
- Flag any computed metric whose source is uncertain.

## Quality check
- [ ] Leads with top-line results vs. target.
- [ ] Per-channel breakdown + trends.
- [ ] Insights explain the "why"; recommendations are actionable.
- [ ] No fabricated/filled-in data; gaps noted.
