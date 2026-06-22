# run3d

3D tunnel runner built with Canvas 2D — switch lanes, jump gaps, collect coins, and progress through levels of increasing difficulty.

## Features

- **8 levels** with distinct visual themes (Void, Magma, Crystal, Neon, Aurora, Abyss, Prism, Galaxy)
- **3D perspective tunnel** with style-specific platform rendering
- **Shop system** — buy height upgrades, color themes, and trail effects with in-game coins
- **Progressive height unlocks** — must buy taller heights before shorter ones
- **Adaptive canvas** — scales to any viewport/window size via `ctx.scale`, crisp on retina displays
- **Persistent progress** — coins, purchased items, level bests, and config saved to `localStorage`

## Changes made so far

- Fixed canvas internal resolution bug (was defaulting to 300×150, causing zoomed/blurry display)
- Replaced CSS stretch scaling with `ctx.scale(SCALE, SCALE)` for crisp rendering at any resolution/DPI
- Adaptive aspect ratio — game fills viewport with correct proportions
- Progressive height unlocks in shop (90% → 80% → 70% → 60% → 50% must be bought in order)
- Removed stray detection code that was causing errors
- Graphics polish: rounded anti-aliased player limbs, drop shadow, visor highlight, platform edge highlights, pill-shaped progress bar, lane dot specular, UI backdrops
- Tutorial text timing slowed to roughly double the original distances
