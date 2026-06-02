# Creative Iteration Engine — Scale Winners Without Burning Them Out

**Generate 10+ strategic ad creative iterations from a winning Meta/Facebook ad through a 4-Filter Winner Validation Gate and a 5-vector iteration system.**

Give Claude a winning Meta ad and it runs the full chain — detects what's connected (Meta Ads MCP, /watch skill, Competitor Ad Spy), pulls your account data filtered to sales-objective campaigns only, derives benchmarks from your own ads, validates the candidate winner through the 4-Filter Test (Spend / Signal / Stability / Scale), diagnoses the winning DNA across 7 components, then produces 10+ iterations ordered by the Andromeda Template Rule (templates first, copy second). Refuses to iterate on fake winners.

## Install

**Claude Desktop (Cowork):** download [`creative-iteration-engine.skill`](https://github.com/the-baweja/creative-iteration-engine/releases/latest) → Settings → Skills → drop it in.

**Claude Code:**

```
git clone https://github.com/the-baweja/creative-iteration-engine.git ~/.claude/skills/creative-iteration-engine
```

**Manual:** clone this repo into any skills directory your Claude setup reads from.

## What it does

You give it a winning Meta ad — or no winner yet, just a brand. It runs the full pipeline:

1. **Preflight Check + Setup Runbook** — detects what's connected (Meta Ads MCP, /watch skill, Competitor Ad Spy), gives you exact install instructions for anything missing, offers fallback paths so you're never blocked
2. **Mode selection** — Mode A (you have a winner with performance data) or Mode B (no winner, enter the category strategically via competitive analysis)
3. **Data import (3-tier ladder)** — Meta Ads MCP → CSV upload from Ads Manager → manual paste. Always reads the highest tier available.
4. **Benchmark derivation** — pulls last 30 days at ad level, filters to sales-objective campaigns only (no skewed averages from awareness/traffic), computes account-specific CTR / CPM / CPC / CPA / hook rate / hold rate using top-quartile median as the bar
5. **4-Filter Winner Validation Gate** — Spend (4-5× / 10-15× / 21-25× CPA thresholds), Signal (CPM + CTR + CPC read together), Stability (post-budget-bump hold), Scale (CPA drift). Refuses to iterate on fake winners.
6. **DNA diagnosis** — breaks the winner into 7 components (hook, angle, proof, offer/CTA, format, tone, audience signal), identifies the 2-3 elements driving performance
7. **Video import** — chains into the `/watch` skill when the ad is a video. Downloads, extracts frames, transcribes — iterations are grounded in what's actually on screen, not guessed from the title.
8. **Iteration generation** — produces 10+ iterations across 5 vectors, ordered per the Andromeda Template Rule:
   - **Template/Format swap** (safest) — different visual structure, same message
   - **Hook swap** — same template, different opener
   - **Proof swap** — different testimonial / stat / before-after / demo
   - **Tone swap** — UGC ↔ polished, positive ↔ fear ↔ contrarian
   - **Angle extension** (experimental) — new persuasion approach grounded in the same audience insight
9. **100-Variation Mode** (exceptional winners only) — if the ad clears all 4 filters, produces 100 variations across templates / hooks / proofs / tones / formats / placements / angles / contrarian tests
10. **Scoring + 3-wave testing roadmap** — each iteration scored on a 6-factor rubric. Wave 1 validates, Wave 2 explores, Wave 3 discovers. Per-wave kill / iterate / scale thresholds anchored to your own benchmarks.

Plus a **decision framework** — what every test outcome teaches you and what to test next. Every result becomes strategic intelligence, not pass/fail.

## Two modes

**Mode A — Own Winner.** You have a Meta ad that's working and want 10+ strategic iterations. The skill imports your performance data via MCP / CSV / paste, validates the candidate through the 4-Filter Gate, and refuses to iterate on fake winners.

**Mode B — Competitor Research.** You don't have a winner yet. The skill chains into [Competitor Ad Spy](https://github.com/the-baweja/competitor-ad-spy) to identify saturated patterns (table stakes, with your brand twist) and uncontested gaps (whitespace), then generates iterations for either lane.

## Output

A branded DOCX report with:

- Executive summary and preflight check summary
- Mode and rationale
- Derived account benchmarks (sales-objective only)
- Candidate winner breakdown with 30-day performance against your own benchmarks
- 4-Filter Validation Gate results
- DNA diagnosis — what to preserve across iterations
- Iteration strategy with Andromeda Template Rule rationale
- All 10+ iterations organized by risk level (safe → medium → experimental), each with a complete production spec (hook, shot list, on-screen text overlays, music direction, end card)
- 3-wave testing roadmap with budget thresholds, kill / iterate / scale rules
- Decision framework — what every result teaches you
- Iteration ceiling warning + handoff to PLAN-tier skills (Ad Angle Generator, Pain Point Miner, Competitor Ad Spy) when the concept is exhausted

## Customize Your Branding

Edit `references/branding.md` with your own brand colors, typography, and document structure. The skill reads this file to generate reports that match your brand identity.

## Example

Prompt:

```
Iterate on a winning Meta ad in my Kass Care ad account.
Focus on Instagram Reels placement.
```

Output: Preflight Check confirmed Meta Ads MCP connected, 47 ad accounts surfaced grouped by business, Kass Care PreP selected. Pulled last 30 days at ad level filtered to sales-objective campaigns (64 ads). Derived benchmarks: top-quartile median CTR 2.29%, CPC ₹36, CPA ₹1,302. Candidate winner identified (₹1,302 CPA, 12× spend gate). 4-Filter Gate: Pass / Pass / Fatigue Warning / Inconclusive. DNA diagnosed — Founder Video format is the driver (3 of top 4 winners). 10 Reels-specific iterations generated (3 safe + 4 medium + 3 experimental), each with full production spec. 3-wave testing roadmap with budget thresholds anchored to derived benchmarks. Decision framework included.

## Who this is for

Media buyers, creative strategists, brand owners, and performance marketers who have a winning Meta ad and want to extend its life systematically — without burning the audience out by running it until CPA collapses. Or who want to enter a new category strategically by iterating into competitive whitespace.

This is skill 7 of 10 in the **AI Skills for Media Buyers** series by [Baweja Media](https://bawejamedia.com).

---

## Want Baweja Media to audit your ad account and explore opportunities to work together?

[→ Book a strategy call](https://webinar.sannidhyabaweja.com/vsl-lp-ind)

---

Built by [Baweja Media](https://bawejamedia.com) · MIT License
