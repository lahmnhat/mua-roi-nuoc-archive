# 360 Film Embed

_Started 2026-06-13 15:03 UTC_

---

## User

no need an all records anymore. delete and replace with 360 film only. make it that we can embed an mp4 in

## Assistant

_[tool: read_file]_

_[tool: read_file]_

_[tool: dc_js_str_replace]_

I understand the file now. I'll remove the "All records" tab, default the ledger to the **360° film** filter, and add MP4-embedding to the 360° film record. Let me make these edits.

_[tool: dc_js_str_replace]_

_[tool: dc_js_str_replace]_

_[tool: dc_js_str_replace]_

_[tool: dc_js_str_replace]_

Now the template edits — add the film plate and the embed control:

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: show_html]_

The edits are in. Let me verify the ledger renders the 360° film tab and card correctly.

_[tool: show_html]_

_[tool: eval_js]_

_[tool: save_screenshot]_

_[tool: save_screenshot]_

_[tool: save_screenshot]_

_[tool: eval_js]_

The "All records" tab is gone, **360° FILM** is now the default tab showing just the film record, and the empty plate prompts an MP4 embed. Let me verify the embed actually renders a video:

_[tool: eval_js]_

_[tool: eval_js]_

Embed works — pasting an MP4 URL renders a `<video>` player. Let me clear the test embed I just added so the user lands on the clean empty slot:Done. The ledger now opens on **360° film** by default, the "All records" tab is gone, and the film record has an MP4 embed slot — paste an `.mp4` link (or a 360° video URL / file path) and hit Embed to render an inline `<video>` player, with a Remove control to clear it. Embeds persist across reloads.

_[tool: done]_

Changes are in and the page loads cleanly. Quick note: I kept the other class tabs (3D objects, oral histories, soundscapes) since they map to real holdings — only the "All records" tab was removed and 360° film is now the default. If you'd rather the ledger be *exclusively* the film with no other tabs, just say so.

