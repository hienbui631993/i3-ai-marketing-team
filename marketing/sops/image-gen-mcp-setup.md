# SOP — Enable Image Generation (nano-banana MCP)

Unlocks the **Social Creative Designer** skill so the team can render on-brand visuals.
Follow once per machine. (Video reference: *Build Skill 2 — Social Creative Designer*, 6:15.)

## What's already wired
- **`.mcp.json`** (project root) declares a `nano-banana` MCP server that runs
  [`@ycse/nanobanana-mcp`](https://www.npmjs.com/package/@ycse/nanobanana-mcp)
  (Google Gemini "nano banana" image generation) via `npx`.
- The Gemini API key is read from the **`GEMINI_API_KEY`** environment variable —
  **no key is stored in the repo.** (`.mcp.json` maps it to the `GOOGLE_AI_API_KEY`
  variable the package actually expects, so you only ever set `GEMINI_API_KEY`.)
- On Windows, `.env` is **not** auto-loaded into the MCP environment. Set
  `GEMINI_API_KEY` as a user environment variable (e.g.
  `[Environment]::SetEnvironmentVariable('GEMINI_API_KEY', '<key>', 'User')`) and
  restart the IDE, **or** export it in the shell that launches Claude Code.

## One-time setup
1. **Get a Gemini API key** from Google AI Studio (https://aistudio.google.com/apikey).
2. **Provide the key** (pick one):
   - Copy `.env.example` → `.env` and set `GEMINI_API_KEY=...` (`.env` is gitignored), **or**
   - Export it in your shell / Claude Code environment: `export GEMINI_API_KEY=...`
3. **Restart** Claude Code (or your IDE) so it reads `.mcp.json`.
4. Run **`/mcp`** — you should see `nano-banana` listed as connected.
5. (Optional) Approve the server when prompted.

## Verify it works
- Ask: *"Use the nano-banana MCP to generate a test image of an i3-blue abstract banner."*
- If it returns an image, you're set. If not, re-check the key and that `/mcp` shows it connected.

## Notes
- Node.js must be installed (the server runs via `npx`).
- Prefer a different provider/package? Swap the `command`/`args` in `.mcp.json`
  (other options: `@nanana-ai/mcp-server-nano-banana`, `ConechoAI/Nano-Banana-MCP`).
  Keep the key in an env var, never inline.
- Build the **style library** in `marketing/templates/social-creatives/` (on-brand
  examples = inspiration, not copies) — reference quality drives output quality.

## Security
- Never commit `.env` or paste the key into `.mcp.json`, skills, or chat history.
- The key grants billable API access — rotate it if exposed.
