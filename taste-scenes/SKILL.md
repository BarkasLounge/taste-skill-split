---
name: taste-scenes
description: Companion kit for the taste-skill - the big scenes (assets/scenes) with their runtime (lib.js, print.js, scenes.js, scenes.css) and the scenes index.json.
---

# taste-scenes — big scenes

Companion asset kit split out of the `taste-media` folder to fit the RUFP
import size limit. Nothing is trimmed: every file of the original
`assets/scenes` kit lives here.

## Layout

- `assets/scenes/` — the big scenes: ten scene folders plus `_demo`,
  `index.json`, `lib.js`, `print.js`, `scenes.css`, `scenes.js`
  (`scenes.md` in the main skill's `references/`).

## Using it with the main skill

The main `taste-skill` folder keeps `scenes/index.json`, so its own checks and
`moments.mjs pick` still weight scenes. When a main-skill step reads a scene
demo or the scenes runtime from `assets/scenes` and it is not in the main
folder, take it from this folder instead
(`~/.rufp/skills/taste-scenes/assets/scenes`).
