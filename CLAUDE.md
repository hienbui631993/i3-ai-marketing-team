# CLAUDE.md — i3 International AI Marketing Team

Project instructions for Claude Code. This is the "manager + org chart" for the
team. **Keep this file updated** as skills and agents are added (it is not a
one-off — video @ 3:08).

> Build status & plan: see [`PROGRESS.md`](./PROGRESS.md) and [`GUIDE.md`](./GUIDE.md).

---

## What this project is
A full AI marketing team for **i3 International** — a leader in **affordable,
integrated, cloud-based AI** surveillance + business-insights solutions. Agents
that **research, write, analyze, and design**, sharing a common set of skills, all on-brand.

Target shape: **5 agents · 12 skills** (see GUIDE §2). Currently building the
**basic** core first.

### Brand snapshot (from the official i3 Brand Kit)
- **Tagline:** *Affordable Integrated AI Solutions*
- **Promise:** "We're not just building technology. We're building trust, one solution at a time."
- **Tone pillars:** Inventive · Trustworthy · Fearless · Driven ("we speak with purpose")
- **Colors:** Brand Blue `#00588F`, Dark Blue `#002447`; expression: Pink `#DF1E71`, Green `#00A661`, Yellow `#FFC107`
- **Fonts:** Helvetica Neue (primary); Gitlab Sans / Barlow (secondary for Schools/QSR/Retail)
- **Brand assets:** [`/i3 Media Kit/`](./i3%20Media%20Kit/) — logos, brand kit PDF, product & solution images. **Use these as the source of truth.**

---

## Always load brand context first
Before producing ANY marketing output, read the brand brain in
[`marketing/context/`](./marketing/context/):
- [`brand-voice.md`](./marketing/context/brand-voice.md) — how i3 sounds
- [`style-guide.md`](./marketing/context/style-guide.md) — colors, fonts, formatting
- [`product-offerings.md`](./marketing/context/product-offerings.md) — what we sell
- [`marketing-strategy.md`](./marketing/context/marketing-strategy.md) — goals, funnel, channels
- [`marketing-function-map.md`](./marketing/context/marketing-function-map.md) — weekly tasks → skills → agents

> Several context files contain `[confirm]` placeholders pending i3 review. If a
> placeholder is relevant to a task, flag it rather than inventing facts.

---

## Where things live
| Path | Purpose |
|------|---------|
| `marketing/context/` | Brand brain — load first, reusable |
| `marketing/templates/` | Reference examples for reference-based skills |
| `marketing/sops/` | Standard operating procedures |
| `marketing/skills/` | The skills (shared playbook) — one folder each |
| `marketing/agents/` | The agent definitions — one `.md` each |
| `marketing/working/` | **All produced output** (ads, pages, presentations, reports, content) |

**Always save deliverables under `marketing/working/`** in the matching subfolder.

---

## Agents vs. skills — when to use which
(Video @ 12:38) Default rule:
- **Use an agent** when the task needs **synthesis or judgment** — research,
  audience analysis, campaign strategy, performance analysis.
- **Use a skill directly** when the task is **executional and straightforward** —
  drafting a single blog, a social post, or a deck from a clear brief.
- For **complex multi-deliverable campaigns**, orchestrate: plan the steps, route
  each to the right agent/skill, and keep every deliverable tied to one campaign theme.

---

## Team roster & routing
> **To be completed in Step 12** once agents exist (GUIDE §4, step 12). Draft map below.

| If the task is about… | Route to agent | Likely skill(s) |
|-----------------------|----------------|-----------------|
| Keywords, audience, competitor, market trends | **Market Researcher** | Keyword Research, Market & Audience Research |
| Blogs, social copy, emails, lead magnets | **Content Creator** | Blog Writer, Social Post Copywriter, Email/Newsletter, Lead Magnet |
| Decks, social creatives, landing pages | **Creative Designer** | Branded Deck, Social Creative Designer, Landing Page Builder |
| Reporting, dashboards, metrics | **Data Analyst** | Campaign Report, Data Visualization |
| Campaign brief, positioning, orchestration | **Campaign Strategist** | Campaign Brief / Strategy |

*(Agents are not built yet — this table documents the intended routing.)*

---

## Conventions
- Match i3's voice and style guide in every asset.
- Write web/blog content for SEO **and** AI search: question-style headers, clear
  structured answers, one CTA.
- Don't fabricate proof points, customer results, or compliance claims — flag `[confirm]`.
- Save outputs to `marketing/working/<type>/` with descriptive filenames.

---

*Update this file whenever a skill or agent is added or routing changes.*
