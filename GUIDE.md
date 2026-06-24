# GUIDE — Build Your Full AI Marketing Team (inside Claude Code)

> Master reference for turning Claude Code into a complete AI marketing team —
> agents that **research, write, analyze, and design**, all working together.
>
> **Source video:** *Build Your Full AI Marketing Team*
> https://www.youtube.com/watch?v=yLXLHnD4fco
>
> **Transcript in this repo:** [`Build Your Full AI Marketing Team.md`](./Build%20Your%20Full%20AI%20Marketing%20Team.md)
> (line numbers + timestamps preserved — every section below links back to it)
>
> **Our brand:** i3 International (`marketing@i3international.com`).
> The video builds for a travel brand ("Go Travel"). We follow the **same method**
> but swap in **i3 International's** brand context. Target shape: **5 agents · 12 skills**.

---

## 0. The core mental model

| Concept | What it is | Analogy |
|--------|-----------|---------|
| **Skill** | One repeatable workflow, packaged so Claude runs it the same way every time | The shared *playbook / SOP* |
| **Agent (sub-agent)** | A specialized team member with a focused role + its own set of skills | The *person* on the team |
| **CLAUDE.md** | Project-wide custom instructions + routing rules | The *org chart + manager* |
| **Context folder** | Brand voice, style, products, strategy — loaded once, reused everywhere | The *brand brain* |
| **MCP** | Connection to external tools (e.g. image generation, Notion) | The team's *external tools* |

> **Why agents on top of skills?** (video @ 8:03) — "The more skills you pile into
> one conversation, the less focused Claude becomes." Dedicated agents = focused,
> better work. Skills are the playbook; agents are the specialists who run them.

---

## 1. The 4-step design framework (video @ 0:27)

1. **Map your marketing function** — list the marketing tasks you actually do every week.
2. **Turn each repeatable workflow into a skill** — ideally one skill per workflow.
3. **Group similar skills into non-overlapping agent roles** — focused agents produce better work.
4. **Connect agents + skills as a team** — set up the project so Claude knows *who is on the team* and *when to use an agent vs. a skill*.

---

## 2. Target architecture (5 agents · 12 skills)

The video ships 5 agents and 12 skills. Here's our proposed mapping for i3 International
(to be confirmed in Step 1 against our real weekly tasks):

| Agent | Role (thinks in…) | Skills it owns |
|-------|-------------------|----------------|
| **Market Researcher** | trends, audiences, keywords | 1. Keyword Research · 2. Market & Audience Research |
| **Content Creator** | stories & headlines | 3. Blog Writer · 4. Social Post Copywriter · 5. Lead Magnet (PDF) · 6. Email / Newsletter |
| **Creative Designer** | visuals & brand look | 7. Social Creative Designer (MCP image gen) · 8. Branded Deck · 9. Landing Page Builder |
| **Data Analyst** | numbers, charts, patterns | 10. Campaign Report · 11. Data Visualization / Dashboard |
| **Campaign Strategist** | positioning & orchestration | 12. Campaign Brief / Strategy Deck |

> Roles are **non-overlapping** on purpose. A skill lives with exactly one agent so
> routing stays unambiguous. Counts are a starting point — adjust to i3's real workflows.

---

## 3. Folder layout (video @ 1:49)

Real businesses organize by department; we focus on `marketing/`, split into
**system folders** (reusable by agents) and **working folders** (where output lands).

```
i3-ai-marketing-team/
├── CLAUDE.md                  # project instructions + agent routing (Step "CLAUDE.md")
├── .mcp.json                  # external tool connections (image gen, Notion…)
├── marketing/
│   ├── context/               # SYSTEM · the brand brain (load first!)
│   │   ├── brand-voice.md
│   │   ├── style-guide.md
│   │   ├── product-offerings.md
│   │   └── marketing-strategy.md
│   ├── templates/             # SYSTEM · reference examples for skills
│   │   ├── branded-deck/
│   │   └── social-creatives/
│   ├── sops/                  # SYSTEM · standard operating procedures
│   ├── skills/                # the 12 skills (one folder each)
│   ├── agents/                # the 5 agent .md definitions
│   └── working/               # OUTPUT
│       ├── ads/
│       ├── pages/
│       ├── presentations/
│       ├── reports/
│       └── content/
```

> **Context first (video @ 2:23):** brand voice guide, style guide, product offerings,
> marketing strategy. Pre-equipping agents with brand knowledge "makes the whole difference."

---

## 4. Build process — ordered checklist with video timestamps

Each row maps to a tracked item in [`PROGRESS.md`](./PROGRESS.md).

| # | Phase | What to do | Video section | Transcript ts |
|---|-------|-----------|---------------|---------------|
| 0 | **Preparation** | Learn transcript, list process, create PROGRESS.md + GUIDE.md | (intro) | 0:00 |
| 1 | **Map function** | List i3's weekly marketing tasks; confirm the 12-skill / 5-agent map | Design Your AI Marketing Team | 0:27 |
| 2 | **Folder setup** | Create `marketing/` system + working folders | Project Folder Setup | 1:49 |
| 3 | **Load context** | Write brand-voice, style-guide, product-offerings, marketing-strategy | Project Folder Setup | 2:23 |
| 4 | **CLAUDE.md** | Init project instructions (`/init`-style); keep updating it | Project Folder Setup | 2:50 |
| 5 | **Official skills** | Install Anthropic's prebuilt skills (e.g. document/PowerPoint skills) | Install Claude Code | 3:15 |
| 6 | **Skill 1 — Branded Deck** | Reference-based: add template → analyze → extend PowerPoint skill | Build Skill 1 | 3:42 |
| 7 | **Skill 2 — Social Creative** | MCP-based: style library + `.mcp.json` (image-gen model) → skill | Build Skill 2 | 6:15 |
| 8 | **Skills 3–12** | Build remaining skills (blog, keyword, lead magnet, report, viz, landing page, email, etc.) | Marketing Skills Library | 8:03 |
| 9 | **Agent 1 — Data Analyst** | `/agents` → create project agent; assign report + viz skills | Build Agent 1 | 8:34 |
| 10 | **Agent 2 — Content Creator** | `/agents` → assign the content skills | Build Agent 2 | 10:27 |
| 11 | **Agents 3–5** | Market Researcher, Creative Designer, Campaign Strategist | Agent Routing | 11:42 |
| 12 | **Routing rules** | Update CLAUDE.md with explicit "when to use which agent" routes | Agent Routing | 11:42 |
| 13 | **Orchestration test** | Give a complex multi-deliverable brief; verify agents collaborate | Team Orchestration | 12:10 |
| 14 | **Notion task board** | (Optional) Shared Kanban → agents pick up pending tasks | Notion Task Board | 13:53 |
| 15 | **Remote control** | (Optional) `/remote-control` to drive the team from mobile | Remote Control Team | 15:18 |

---

## 5. Method notes (the techniques that matter)

### Reference-based skills (video @ 3:48 — Branded Deck)
"You give Claude examples or templates of what good looks like, and it studies the patterns."
1. Drop a branded template in `templates/`.
2. Have Claude **analyze the template** → detailed analysis report.
3. Ask it to **extend the official PowerPoint skill** using template + analysis → new branded-deck skill.
Output is ~90% done; minor fixes (margins, charts) expected. Add more templates (strategy deck,
client reporting, product launch) the same way.

### MCP-connected skills (video @ 6:15 — Social Creative Designer)
1. Build a **creative style library** under `templates/social-creatives/` (inspiration, *not* exact copies) + a style guide.
2. Create **`.mcp.json`** in project root declaring external tools (the video uses the
   "nano banana" image model via a Gemini API key).
3. Restart, run `/mcp` to confirm servers are connected.
4. Generate the skill — it scans the style library and matches the *vibe*, not a copy.
> Setting up good references is what drives output quality.

### Creating agents (video @ 8:44)
`/agents` → *Create New Agent* → *for this project only* → let Claude draft the `agent.md`.
Tell it: the role, which skills it uses, tools, default model, color, and memory location.
Each agent becomes a markdown file under `agents/` defining role + skills + responsibilities.
Call an agent with `@agent-name`.

### Routing in CLAUDE.md (video @ 11:42)
Add explicit rules so Claude knows when to dedicate to an agent vs. just run a skill.
Rule of thumb from the video: tasks needing **synthesis** (research, campaign strategy) →
use an agent; **executional / straightforward** content → a skill is enough.

---

## 6. Optional extensions

- **Notion task board (13:53):** a Kanban of marketing tasks (priority / title / details / status).
  Prompt Claude to scan pending To-Do items, assign an agent, execute by priority, and flip
  status to Complete with output file paths. (Needs a Notion MCP connection.)
- **Remote control (15:18):** `/remote-control` prints a link to drive your live local session
  from the Claude mobile app. **Never share the link** — it grants full session control.
  One session at a time; `/clear` when context fills.

---

## 7. Quick links back to the video

| Timestamp | Section |
|-----------|---------|
| 0:00 | What we're covering |
| 0:27 | Design Your AI Marketing Team (the 4 steps) |
| 1:05 | Popular ways to use Claude Code |
| 1:31 | Install Claude Code (VS Code) |
| 1:49 | Project Folder Setup |
| 3:42 | Build Skill 1: Branded Deck |
| 6:15 | Build Skill 2: Social Creative Designer |
| 8:03 | Marketing Skills Library + why move beyond skills |
| 8:34 | Build Agent 1: Data Analyst |
| 10:27 | Build Agent 2: Content Creator |
| 11:42 | Agent Routing with CLAUDE.md |
| 12:10 | Team Orchestration |
| 13:53 | Notion Task Board |
| 15:18 | Remote Control Team |

---

*Step 0 deliverable. See [`PROGRESS.md`](./PROGRESS.md) for live build status.*
