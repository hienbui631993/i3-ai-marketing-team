---
name: blog-writer
description: >-
  Write an on-brand i3 International blog post / article optimized for SEO and AI
  search. Use when the task is to draft a blog, article, or long-form web content
  for i3. Produces a structured, question-headed, single-CTA article saved to
  marketing/working/content/.
---

# Blog Writer — i3 International

Draft long-form articles that sound like i3 and rank in both classic search and
AI answer engines.

## Before writing — load context
1. Read the brand brain in `marketing/context/`:
   - `brand-voice.md` (tone pillars: Inventive, Trustworthy, Fearless, Driven)
   - `product-offerings.md` (use real solution names: i3Ai Sentry, Heat Mapping,
     Smart-ER, Velocity Drive-thru Timer, Alert Center, etc.)
   - `marketing-strategy.md` (funnel stage, target vertical)
   - `style-guide.md` (formatting)
2. If keyword/audience input is missing and the topic is competitive, request (or
   route to) the **Keyword Research** / **Market Research** skills first.

## Inputs to confirm with the requester
- Topic / working title · target vertical (Retail, QSR, Schools…) · funnel stage
- Primary keyword + 2–4 secondary keywords (if known) · desired length
- The one CTA (demo, lead magnet, contact, etc.)

## Structure (write in this order)
1. **H1 title** — clear, benefit- or question-led, includes primary keyword.
2. **Intro (2–3 sentences)** — name the reader's problem + the payoff. No filler openers.
3. **Table of contents** — for posts > ~800 words.
4. **Body** — `## H2 headers phrased as the reader's question` ("How does AI reduce
   retail shrink?"), each followed by a **direct answer in the first sentence**, then
   detail. Use short paragraphs, bullets, and bold key terms. This structure is what
   AI search engines quote.
5. **Proof** — cite i3 solutions by real name and tie to outcomes. **Never fabricate**
   stats/customer results — insert `[confirm]` if you don't have a verified figure.
6. **Single CTA** — one clear action at the end (and optionally one mid-article).
7. **SEO/AI-search meta** — provide: meta title (≤60 chars), meta description
   (≤155 chars), URL slug, and a 1-sentence "AI snippet answer."

## Voice rules
- Affordable, trust-first, practical, warm ("family"). Plain English over jargon.
- Have a point of view (Fearless), back it with outcomes (Trustworthy).
- Avoid fear-mongering and generic AI filler.

## Output
- Save as `marketing/working/content/blog-<slug>.md`.
- Top of file: front-matter block with title, slug, meta title, meta description,
  primary/secondary keywords, vertical, funnel stage, CTA.
- End: a short "Suggested social posts" note (1–2 lines) so the Social Post skill can pick it up.

## Quality check before done
- [ ] Every H2 is a question with an immediate answer.
- [ ] One CTA, on brand, matches funnel stage.
- [ ] Real i3 solution names; no invented proof points (`[confirm]` where unsure).
- [ ] Meta fields present; slug is clean.
