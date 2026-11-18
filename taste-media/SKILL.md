---
name: taste-media
description: Companion kit for the taste-skill - objects (renders, prints) and photos (the vetted photograph library), with a native photos.mjs whose search and fetch run against the full library.
---

# taste-media — objects, photos

Companion asset kits split out of the `taste-skill` folder to fit the RUFP
import limit. Nothing is trimmed: every file of the original
`assets/objects` and `assets/photos` kits lives here. The `assets/scenes`
kit lives in the `taste-scenes` folder.

## Layout

- `assets/objects/` — objects and prints, including `product-render`
  (`effects-objects.md` in the main skill's `references/`).
- `assets/photos/` — the vetted photograph library: the `photos.json` catalog
  and the `img/` WebP frames.
- `scripts/photos.mjs` — a native copy; `search` and `fetch` run against this
  full library from this folder.

## Using it with the main skill

The main `taste-skill` folder keeps `photos/photos.json`, so its own
`photos.mjs` still reads the catalog, and its `fetch` looks for the `img/`
frames in this folder automatically (`~/.rufp/skills/taste-media/assets/photos`).
When a main-skill step reads an object demo from `assets/objects` and it is
not in the main folder, take it from this folder instead; a scene demo comes
from the `taste-scenes` folder (`~/.rufp/skills/taste-scenes/assets/scenes`).
