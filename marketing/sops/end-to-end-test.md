# SOP — End-to-End Test of the i3 AI Marketing Team

How to verify the whole team works: brand context loads, routing in `CLAUDE.md`
sends work to the right agent/skill, every skill produces on-brand output, and the
image-gen MCP renders visuals.

> **Run this in your LOCAL Claude Code** (desktop/IDE/terminal), where your `.env`
> with a valid `GOOGLE_AI_API_KEY` lives. A remote/cloud session cannot reach your
> local key, so the image step only works locally (see `image-gen-mcp-setup.md`).

---

## 0) Pre-flight (30 sec)
1. `git pull` so you have the latest skills/agents and the correct env-var name.
2. `.env` contains **`GOOGLE_AI_API_KEY=...`** (not `GEMINI_API_KEY`).
3. Restart Claude Code, then run **`/mcp`** → `nano-banana` shows **connected**.
4. (Optional) register agents: **`/agents`** → confirm the 5 i3 agents are listed
   (or that `marketing/agents/*.md` are copied into `.claude/agents/`).

**Pass:** `/mcp` shows nano-banana connected; `/agents` lists the 5 agents.

---

## 1) Smoke-test each layer in isolation (fast)

### a. Brand context loads
> "Without doing a task yet, list the 5 files in `marketing/context/` you load
> first, and give me i3's tagline, primary font, and 3 brand hex colors."

**Pass:** Tagline *"Affordable Integrated AI Solutions"*, font **Montserrat**, colors
include `#00588F`, `#0A1428`, `#FF007D`.

### b. A skill directly (executional)
> "Use the Social Post Copywriter skill to write one LinkedIn post announcing i3's
> cloud video analytics for retail. Save to `marketing/working/content/`."

**Pass:** On-brand voice, one CTA, file saved in the right folder.

### c. An agent (synthesis/judgment)
> "@market-researcher: give me 5 buyer-intent keywords and the top audience pain
> for QSR (quick-service restaurant) video security."

**Pass:** Routed to Market Researcher; output reads like analysis, not just copy.

### d. Image MCP (the previously-blocked piece)
> "Use the Social Creative Designer skill to generate ONE 1:1 LinkedIn graphic:
> i3 brand, navy `#0A1428` + magenta `#FF007D`, Montserrat headline 'See It Live,
> Not Later', white i3 logo. Save to `marketing/working/ads/`."

**Pass:** A PNG appears in `marketing/working/ads/`, on-brand colors, legible text.
(If you get `API_KEY_INVALID`, your key/var name is wrong — fix step 0.2.)

---

## 2) Full orchestration test (the real end-to-end)
One prompt, one theme, all 5 agents/skills — this is "the entire process":

> "Run a complete mini-campaign for **i3 cloud video analytics for quick-service
> restaurants (reduce drive-thru disputes & theft)**. Have the **Campaign Strategist**
> lead: (1) Market Researcher → research + keywords; (2) Strategist → campaign brief;
> (3) Content Creator → 1 blog + 1 LinkedIn post + 1 email; (4) Creative Designer →
> landing page + 2 social creatives via the image MCP; (5) Data Analyst → a sample
> post-launch report skeleton. Keep one theme throughout, stay on-brand, flag any
> proof points as `[confirm]`, and save every deliverable under `marketing/working/`."

**Pass criteria (check each):**
- [ ] Strategist wrote a brief first, then routed the rest (orchestration, not one blob).
- [ ] Research → `working/reports/`, copy → `working/content/`, page → `working/pages/`,
      creatives → `working/ads/`, report → `working/reports/`.
- [ ] Voice + colors + Montserrat consistent across text and visuals.
- [ ] Unverified stats are flagged `[confirm]`, not invented.
- [ ] At least one real PNG creative was produced by nano-banana.

---

## 3) Inspect outputs
```
ls -R marketing/working/
```
Open the landing page in a browser; open the PNGs; skim the blog/email for voice.

## 4) Reset between runs (optional)
Delete the test artifacts you don't want to keep:
```
# review first, then remove specific test files under marketing/working/
```

---

## What "green" looks like
Routing is correct, every layer produces on-brand output saved to the right folder,
and the image MCP renders at least one real creative. If any step fails, isolate it
with the matching smoke test in §1 before re-running the full campaign in §2.
