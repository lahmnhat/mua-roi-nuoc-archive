# Status and Conservation Focus

_Started 2026-06-13 18:20 UTC_

---

## User

dont need this, pls delete these origin, medium, and holdings, only keep status and emphasise the endagered, actively preserved

## Assistant

_[tool: read_file]_

_[tool: str_replace_edit]_

Done. Removed Origin, Medium, and Holdings — the hero now closes on a single emphasized Status line with **Endangered** picked out in red.

_[tool: done]_

That tweak is in place — the hero stat grid is now a single Status line.

## User

dont hide it, show preview. dont need an extra release viewer or open button. just show it and if the mouse hovers over, zoom in and dim the rest of the web

## Assistant

_[tool: grep]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: str_replace_edit]_

Now I'll make the scan always show its preview, remove the toggle buttons, and add hover-to-zoom with page dimming.Now add the dim overlay element after the scans rail and wire up the logic. Let me add the overlay right after the rail's closing `</div>`:

_[tool: str_replace_edit]_

Now the logic. Add `railHover` state, the hover handlers per item, and the `railDimStyle` in the returned object:

_[tool: str_replace_edit]_

Done. The 3D scans now show their preview directly — no "View in 3D" cover, no Release/Open button. Hovering a card scales it up and dims the rest of the page behind it.

_[tool: done]_

The scan cards now display their preview immediately, and on hover each one zooms in while the rest of the page dims to focus attention on it. The redundant open/release controls are gone.

