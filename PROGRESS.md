# PROGRESS — AI Marketing Team Build

Live tracker for building i3 International's AI marketing team inside Claude Code.
Full method + timestamps in [`GUIDE.md`](./GUIDE.md). Source video:
https://www.youtube.com/watch?v=yLXLHnD4fco

**Status legend:** ✅ done · 🔄 in progress · ⬜ not started · ⏸️ optional / deferred

_Last updated: 2026-06-24 — Steps 0–12 complete: brand grounded in real Media Kit, all 12 skills + 5 agents built, routing finalized. Remaining: orchestration test (13) + optional Notion/remote (14–15) + image-gen MCP for Social Creative._

---

## Target
**5 agents · 12 skills**, orchestrated via `CLAUDE.md`, with brand context pre-loaded.

---

## Build checklist

| # | Phase | Status | Notes |
|---|-------|--------|-------|
| 0 | **Preparation** — learn transcript, list process, create PROGRESS.md + GUIDE.md | ✅ | Transcript studied; GUIDE.md + PROGRESS.md created |
| 1 | **Map marketing function** — list i3's weekly tasks; confirm skill/agent map | ✅ | Basic set mapped → `marketing/context/marketing-function-map.md` (confirm) |
| 2 | **Folder setup** — `marketing/` system + working folders | ✅ | Full `marketing/` tree scaffolded |
| 3 | **Load context** — brand voice, style guide, products, strategy | ✅ | 4 DRAFT context files written (need i3 review of `[confirm]` items) |
| 4 | **CLAUDE.md** — project instructions | ✅ | Created with context-loading + draft routing (routing finalized in Step 12) |
| 5 | **Install official skills** — Anthropic prebuilt skills pack | ⏸️ | done in-app via `/plugin` (pptx/docs) — referenced by skills |
| 6 | **Skill 1 — Branded Deck** (reference-based) | ✅ | `skills/branded-deck/` — needs a `.pptx` template to fully match |
| 7 | **Skill 2 — Social Creative Designer** (MCP) | ⬜ | needs image-gen MCP — sequenced last |
| 8 | **Skills 3–12** — remaining library | ✅ | all 12 skills built in `marketing/skills/` |
| 9 | **Agent 1 — Data Analyst** | ✅ | `marketing/agents/data-analyst.md` |
| 10 | **Agent 2 — Content Creator** | ✅ | `marketing/agents/content-creator.md` |
| 11 | **Agents 3–5** — Researcher, Designer, Strategist | ✅ | all in `marketing/agents/` |
| 12 | **Routing rules in CLAUDE.md** | ✅ | roster + agent-vs-skill rules finalized |
| 13 | **Orchestration test** — complex multi-deliverable brief | ✅ | "Stop Shrink Before It Walks Out" campaign — 5 deliverables in `marketing/working/` |
| 14 | **Notion task board** | ⏸️ | optional — needs Notion MCP |
| 15 | **Remote control** | ⏸️ | optional — mobile driving |

---

## Skills tracker (12)

| # | Skill | Owner agent | Type | Status |
|---|-------|-------------|------|--------|
| 1 | Keyword Research | Market Researcher | tool-based | ✅ |
| 2 | Market & Audience Research | Market Researcher | research | ✅ |
| 3 | Blog Writer | Content Creator | content | ✅ |
| 4 | Social Post Copywriter | Content Creator | content | ✅ |
| 5 | Lead Magnet (PDF guide) | Content Creator | content | ✅ |
| 6 | Email / Newsletter | Content Creator | content | ✅ |
| 7 | Social Creative Designer | Creative Designer | MCP image gen | ✅* |
| 8 | Branded Deck | Creative Designer | reference-based | ✅ |
| 9 | Landing Page Builder | Creative Designer | build | ✅ |
| 10 | Campaign Report | Data Analyst | analysis | ✅ |
| 11 | Data Visualization / Dashboard | Data Analyst | analysis | ✅ |
| 12 | Campaign Brief / Strategy | Campaign Strategist | strategy | ✅ |

---

## Agents tracker (5)

| # | Agent | Thinks in… | Status |
|---|-------|-----------|--------|
| 1 | Market Researcher | trends, audiences, keywords | ✅ |
| 2 | Content Creator | stories & headlines | ✅ |
| 3 | Creative Designer | visuals & brand look | ✅ |
| 4 | Data Analyst | numbers, charts, patterns | ✅ |
| 5 | Campaign Strategist | positioning & orchestration | ✅ |

> **\*** Social Creative Designer skill is written and ready, but needs an
> **image-generation MCP** connected (`.mcp.json`) before it can render visuals.
> Agent `.md` files define the roles; register via `/agents` (or copy to
> `.claude/agents/`) to invoke them as `@agent-name` sub-agents.

---

## Open questions / inputs needed from i3 International
- [ ] **Review the DRAFT context files** in `marketing/context/` — fix every `[confirm]` item
      (real positioning, verticals, product names, KPIs).
- [ ] Provide the **brand kit** — official colors (hex), fonts, logo files → updates `style-guide.md`.
- [ ] Provide a **branded deck template** → `marketing/templates/branded-deck/` (for Branded Deck skill).
- [ ] Provide **social creative examples** + which image-gen MCP/API to use → for Social Creative skill.
- [ ] Decide whether to wire up the optional **Notion** board and **remote control**.

---

## Orchestration test — "Stop Shrink Before It Walks Out" (Step 13)
First end-to-end campaign run by the team (Retail / Loss Prevention), one theme throughout:
| Step | Skill / Agent | Output |
|------|---------------|--------|
| Research | Market Researcher | `working/reports/research-retail-shrink.md` |
| Brief | Campaign Strategist | `working/reports/brief-stop-retail-shrink.md` |
| Blog | Content Creator → Blog Writer | `working/content/blog-cut-retail-shrink-with-ai.md` |
| Social | Content Creator → Social Post Copywriter | `working/content/social-stop-retail-shrink-linkedin.md` |
| Landing page | Creative Designer → Landing Page Builder | `working/pages/stop-retail-shrink.html` |

All proof points/stats flagged `[confirm]` pending verified i3 figures. Next: lead magnet,
social creatives (needs image MCP), post-launch report/dashboard (needs data).

## Changelog
- **2026-06-24** — Step 0 done: studied transcript, created GUIDE.md + PROGRESS.md, defined target architecture (5 agents / 12 skills) and ordered build checklist.
- **2026-06-24** — Steps 1–3 done (basic build): mapped the basic weekly marketing function (`marketing-function-map.md`), scaffolded the full `marketing/` folder tree, and wrote 4 DRAFT brand-context files (brand voice, style guide, product offerings, marketing strategy). Next: CLAUDE.md (Step 4).
