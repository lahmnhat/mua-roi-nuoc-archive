# Stage 3D Scan Slot

_Started 2026-06-13 18:37 UTC_

---

## User

in this section, add in one addition big slot for a 3d scan of the stage. make it separate from the carousel of the individual model, but have the same parts (name placeholder, place to put the embed link). no need to dim or zoom.

## Assistant

_[tool: read_file]_

_[tool: grep]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: grep]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: str_replace_edit]_

I have what I need. Let me add the standalone stage scan slot — markup, state, and logic.Now the logic — add state, persistence, and render values:

_[tool: str_replace_edit]_

Added a standalone whole-stage 3D slot below the carousel — its own name field and SuperSplat embed link input, with no dim/zoom overlay. Both the name and the embed persist locally.

_[tool: done]_

Done. The Object scans section now has a large, full-width stage scan slot beneath the puppet carousel — a 16:9 viewer plate with its own name field and SuperSplat link input, kept separate from the rail and free of the hover-dim/zoom behavior.

## User

https://uploads.knightlab.com/storymapjs/5a74f1a20ad8a244b2c4febadedd61c2/puppet-water-map/index.html

embed this

## Assistant

_[tool: read_file]_

_[tool: read_file]_

_[tool: str_replace_edit]_

The StoryMap is now embedded in the Figure 02 slot in the Origins section, sized tall enough for the map with a matching framed border and caption.

_[tool: done]_

Embedded. The KnightLab StoryMap now lives in the Figure 02 map slot in Origins, framed to match and captioned.

## User

just display the name, the rest pls hide.

## Assistant

_[tool: str_replace_edit]_

Now add the `stageNameDisplay` render value:

_[tool: str_replace_edit]_

The stage scan card now just displays the name; the SuperSplat embed link input, button, and status note are hidden.

_[tool: done]_

Done — the stage scan footer now shows only the name.

## User

make this bigger, whole page width

## Assistant

_[tool: grep]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: str_replace_edit]_

_[tool: str_replace_edit]_

_[tool: str_replace_edit]_

The "A Day at the Pond — 360° Vlog" card now spans the full ledger width with a much taller video plate, while the rest of the records stay in the grid.

_[tool: done]_

Done — the 360° vlog card is now full page width with a large video area.

