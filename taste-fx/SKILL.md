---
name: taste-fx
description: Companion kit for the taste-skill - components (fx-* creative parts), effects (visual grounds) and moments (animation demos), with native effects.mjs and moments.mjs whose gallery, serve, index and pick commands run against the full kits.
---

# taste-fx — components, effects, moments

Companion asset kits split out of the `taste-skill` folder to fit the RUFP
import limit. Nothing is trimmed: every file of the original
`assets/components`, `assets/effects` and `assets/moments` kits lives here.

## Layout

- `assets/components/` — the creative parts (`fx-*`), per `effects-creative.md`
  in the main skill's `references/`.
- `assets/effects/` — the full effects kit: per-effect demos and meta,
  `pick.js` (the dealing logic), `fx.js`, `index.json`.
- `assets/moments/` — the full moments kit: per-moment demos, `moments.js` /
  `moment.js` runtimes, `index.json`.
- `assets/scenes/index.json` — a copy kept so `moments.mjs pick` can weight
  scenes without the main folder.
- `scripts/effects.mjs`, `scripts/moments.mjs` — native copies; run them from
  this folder (`node scripts/effects.mjs serve`, then open
  `/assets/effects/gallery.html`) and their `index`, `gallery`, `serve` and
  `pick` commands work against the full kits.

## Using it with the main skill

The main `taste-skill` folder keeps `effects/fx.js`, `effects/pick.js` and the
`effects`, `moments` and `scenes` `index.json` files, so building, dealing and
the `consistency.mjs` checks work from there as written. When a main-skill
step reads a demo file from `assets/effects`, `assets/moments` or
`assets/components` and it is not in the main folder, take it from this folder
instead (`~/.rufp/skills/taste-fx/assets/...`). `effects.mjs publish` also
reads `assets/ui/cards.html` from the main folder; run publish from the main
skill when you need it.
