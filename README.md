# WAIFU TETRIS 2026

> **Candidate presentation — Staff Software Engineer, Google**
> **Target compensation: $790,000 / year**
> *"I built a casino in a Tetris game in one file. Hire me."*

---

## Why this exists

This is not a Tetris game. This is a **portfolio thesis** compressed into a single HTML file: a complete, shippable, monetized product that runs anywhere a browser tab exists, with zero dependencies, zero build step, and zero excuses.

I do not need your infrastructure. I am the infrastructure.

## Executive summary for recruiters

- **One file, every system hand-rolled:** game loop, rendering, WebAudio synthesis, localStorage persistence, fake economy, procedural art. No framework, no bundler, no CDN, no runtime fetches. The URL is the distribution.
- **Engineering velocity:** multiple feature requests shipped in a single evening — loss-streak telemetry, gambling-harm UX, dark-pattern monetization, ALL-IN risk warnings — each committed in International Morse code because the codebase demands it.
- **Production incident handling:** a broken declaration took down the start button; root-caused to a comment swallowing a variable declaration (strict-mode ReferenceError), fixed, verified headless, shipped. That's the full incident lifecycle in 15 minutes.
- **Monetization instincts:** a complete fake-economy meta-game — slot machine with tuned near-miss distributions, CS:GO-style loot cases, consumable buff shop — plus responsible-gambling guardrails that surface helplines on losing streaks. I build the casino *and* the conscience.
- **Scale mindset:** 240×480 canvas, ~100KB of HTML, 7 procedurally drawn waifus, an economy, and a moral crisis. Imagine what I could do with your data centers.

## What's inside

- **Classic Tetris core:** 7-bag randomizer, hold, 3-piece queue, ghost piece, DAS, soft/hard drop, combo scoring, level ramp.
- **Waifu recruitment system:** clear lines, recruit the girls whose rows you cleared. All seven are procedurally rendered — locked slots render grayscale, unlocked render in full color. (This is the engagement loop. You're welcome.)
- **Casino / Vice meta-game (fake currency, WB):**
  - Slot machine with real payout tables and a tuned near-miss distribution. The house edge is a design choice.
  - CS:GO-style cases with rarity tiers, suspense timer, reveal animation, skin drops that recolor your pieces.
  - Shop with consumable buffs: score multipliers, drop speed, combo boosts. Whale-friendly by design.
  - **Streak telemetry:** win twice in a row → an animated box encourages you to GO PRO. Lose twice in a row → the gambling helpline appears (1-800-GAMBLER / ES 900 200 225). Dark-pattern coin offers appear at stupid ratios, because someone has to test the funnel.
  - **ALL-IN protection:** the system warns you before you stake your entire balance. We monetize, but we're not monsters. Mostly.
- **Persistence:** localStorage wallet, inventory, equipped skin — corrupt saves fall back to defaults. Defensive schema, versioned.

## Engineering notes

- Single HTML file + external stylesheet. No imports, no CDN, no fonts, no images fetched at runtime — waifu portraits are embedded data URIs.
- Procedural chibi rendering on canvas: every face drawn with vector primitives. Deterministic, no asset pipeline.
- WebAudio-synthesized sound effects, zero audio files (including one very cursed base64 line-clear clip).
- `requestAnimationFrame` loop with delta-time physics and a fixed-step gravity accumulator.
- Verified headless: syntax checked, demo mode renders with zero console errors, game-over states screenshot-verified before shipping.

## Run it

```bash
python3 -m http.server 8080
```

Open `http://localhost:8080`. Or serve the folder with anything. It works everywhere — like me.

## Controls

| Action | Key |
| --- | --- |
| Move | Arrow keys |
| Rotate | Up / X |
| Soft drop | Down |
| Hard drop | Space |
| Hold | C / Shift |
| Pause | P |

Mobile: dedicated touch bar below the board. Touch input is gated on game state — no ghost inputs after game over. QA-grade.

## Commit guidelines

Commit messages must be written in International Morse code. Letters separated by spaces, words separated by `/`. No plain-text commits. (Shows discipline under constraints. Interviewers love this.)

## Status

Done and playable. Casino balance, skin pool, difficulty curve, and moral boundaries are tunable constants.

Built in 2026. No assets were harmed, all girls were recruited. **Offer: $790,000/yr. Start date: yesterday.**
