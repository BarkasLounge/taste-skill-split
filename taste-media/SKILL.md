---
name: taste-media
description: Companion kit for the taste-skill - objects (renders, prints), photos (the vetted photograph library) and scenes (big scenes), with a native photos.mjs whose search and fetch run against the full library.
---

# taste-media — objects, photos, scenes

Companion asset kits split out of the `taste-skill` folder to fit the RUFP
import limit. Nothing is trimmed: every file of the original
`assets/objects`, `assets/photos` and `assets/scenes` kits lives here.

## Layout

- `assets/objects/` — objects and prints, including `product-render`
  (`effects-objects.md` in the main skill's `references/`).
- `assets/photos/` — the vetted photograph library: the `photos.json` catalog
  and the `img/` WebP frames.
- `assets/scenes/` — the big scenes with their `index.json`.
- `scripts/photos.mjs` — a native copy; `search` and `fetch` run against this
  full library from this folder.

## Using it with the main skill

The main `taste-skill` folder keeps `photos/photos.json`, so its own
`photos.mjs` still reads the catalog, and its `fetch` looks for the `img/`
frames in this folder automatically (`~/.rufp/skills/taste-media/assets/photos`).
When a main-skill step reads a scene or object demo from `assets/scenes` or
`assets/objects` and it is not in the main folder, take it from this folder
instead.
