# WAIFU TETRIS 2026

A single-file arcade Tetris where every tetromino is a waifu with her own procedurally drawn face, real generated portraits, and a full casino meta-game. Zero dependencies, zero build step. Open it and it runs.

## Why this project

A complete, self-contained game in one HTML file. No framework, no bundler, no external assets, no server. Every system is hand-rolled: the game loop, the rendering, the audio, the persistence, the economy, the art.

This is what I build when I want something that works everywhere and ships instantly. A browser tab is the runtime. The URL is the distribution.

## The game

Classic Tetris core:

- 7-bag randomizer, hold piece, 3-piece next queue, ghost piece, DAS
- Soft drop, hard drop, combo scoring, level speed ramp
- Line clears recruit the girls whose rows you cleared into your roster
- 7 waifus total, each a distinct piece type with her own hair, eyes, and personality
- Real generated portrait for every girl, embedded as data URIs. Locked slots render grayscale, cleared lines unlock them in full color
- Touch controls on mobile, keyboard on desktop. Responsive layout, board scales to the screen

## The casino

A full fake-economy meta-game layered on top, all in fake currency (WB):

- Slot machine with real payout tables and a tuned near-miss distribution. The house edge is a design choice
- CS:GO-style loot cases with rarity tiers from Consumer to Gold, suspense timer, reveal animation, and skin drops that visibly recolor your pieces
- Shop with consumable buffs that alter gameplay: score multipliers, drop speed, combo boosts
- Persistence via localStorage: wallet, inventory, and equipped skin survive reloads

## Engineering notes

- Single HTML file with an external stylesheet. No imports, no CDN, no fonts, no images fetched at runtime
- Procedural chibi rendering on canvas: every face is drawn with vector primitives, deterministic, no asset pipeline
- WebAudio synthesized sound effects, no audio files
- RequestAnimationFrame loop with delta-time physics, fixed-step gravity accumulator
- localStorage schema is versioned and defensive: corrupt saves fall back to defaults
- Verified headless: syntax checked, demo mode renders with zero console errors

## Run it

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`. Or just serve the folder with any static server.

## Controls

| Action | Key |
| --- | --- |
| Move | Arrow keys |
| Rotate | Up / X |
| Soft drop | Down |
| Hard drop | Space |
| Hold | C / Shift |
| Pause | P |

Mobile: dedicated touch bar below the board.

## Status

Done and playable. Casino balance, skin pool, and difficulty curve are tunable constants, easy to iterate.

Built in 2026. No assets were harmed, all girls were recruited.
