---
name: social-creative-designer
description: >-
  Design on-brand i3 International social creatives — single posts or carousels —
  using an image-generation MCP, guided by the creative style library. Use for
  visual social assets. Saves to marketing/working/ads/. REQUIRES an image-gen MCP.
---

# Social Creative Designer — i3 International

Generate on-brand social visuals that match i3's *vibe* (not copies) using an
external image-generation model via MCP.

## ⚠️ Setup dependency (one-time)
This skill needs the **`nano-banana` image-generation MCP** (Google Gemini) connected.
It is **already declared** in the project `.mcp.json`; you only need to supply the key:
1. Set `GEMINI_API_KEY` (via `.env` from `.env.example`, or your environment).
2. Restart the client and run `/mcp` — confirm `nano-banana` is connected.
3. Build/refresh the **style library** in `marketing/templates/social-creatives/`
   (on-brand examples = *inspiration*, not exact copies) — quality of references
   drives output quality.

Full steps: [`marketing/sops/image-gen-mcp-setup.md`](../../sops/image-gen-mcp-setup.md).
If `GEMINI_API_KEY` is unset / `/mcp` doesn't show `nano-banana`, treat this skill as
**`[blocked: needs image MCP]`** — produce the copy/layout spec via Social Post
Copywriter and flag the visual step.

## Generate via the MCP
Call the `nano-banana` MCP tools (search with ToolSearch: "nano banana image") to
generate/edit images. Save results to `marketing/working/ads/`.

## Before designing — load context
Read `marketing/context/style-guide.md` (colors `#00588F`/`#0A1428` + accents,
Montserrat, logo rules) and scan `templates/social-creatives/` for style.

## Inputs to confirm
- Goal & platform · single vs. carousel (and # slides) · campaign theme/copy source
- Which library style/vibe to follow · vertical (Retail/QSR/Schools).

## Method
1. Pull the copy (from Social Post Copywriter) and the chosen style reference.
2. Write per-image generation prompts that bake in: i3 colors, clean modern look,
   subject matter (retail floor, drive-thru, dashboard/AI UI), and space for text.
3. Generate via the image MCP; keep brand colors and a consistent template across a carousel.
4. Composite headline text (Montserrat) + logo per `style-guide.md` (white logo on dark).
5. Match the *vibe* of the library, don't copy a specific design.

## Output
- Save images to `marketing/working/ads/<campaign>-<n>.png` and a small `…-spec.md`
  noting the copy, style ref, and prompts used.

## Quality check
- [ ] On-brand colors/font/logo; consistent across a set.
- [ ] Matches a library vibe, not a copy.
- [ ] Image MCP confirmed connected (else flagged blocked).
