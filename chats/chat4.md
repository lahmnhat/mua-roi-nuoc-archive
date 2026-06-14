# Input Box Management

_Started 2026-06-13 13:02 UTC_

---

## User

once i paste in the link, pls hide this box, the audience dont need to see it. also, delete the name and description for all, i will input in later

## Assistant

_[tool: read_file]_

_[tool: read_file]_

_[tool: dc_html_str_replace]_

I have a clear picture. The element you commented on is the embed/paste box inside the **Object scans** cards. I'll make two changes:

1. **Hide the paste-link box once a link is embedded** (across the scan cards, the featured object, and the oral-history players) — so the audience never sees the input.
2. **Clear the name + description on the scan cards** so you can fill them in later, leaving a faint "to be added" marker.

Let me apply these.

_[tool: dc_html_str_replace]_

Now the featured object's active-state control bar — hide the status + paste input once embedded, keep "Release viewer":

_[tool: dc_html_str_replace]_

Now the oral-history (interview) SoundCloud paste box:

_[tool: dc_html_str_replace]_

Now clear the name + description on the scan-rail cards in the logic:

_[tool: dc_js_str_replace]_

_[tool: show_html]_

All edits applied. Let me verify the scans section renders correctly.

_[tool: show_html]_

Let me scroll to the scans section to confirm the cards and the embed-box behavior.

_[tool: eval_js]_

_[tool: screenshot]_

_[tool: eval_js]_

_[tool: screenshot]_

_[tool: eval_js]_

The cards now show the faint "Name & description — to be added" marker and clean fill-in slots. Let me confirm the paste box actually disappears once a link is embedded.

_[tool: eval_js]_

_[tool: eval_js]_

_[tool: eval_js]_

_[tool: screenshot]_

The behavior is working — card 0 already has a pasted link (`rail-0`) persisted, so its paste box is correctly hidden. Let me confirm the embedded viewer shows and the box stays hidden.

_[tool: done]_

Both changes are confirmed working. Card 0 (which already has a pasted link) shows the embedded 3D viewer with the paste box hidden — only "Release viewer" remains — while the name/description area shows the faint "to be added" marker ready for you to fill in.

Summary of what changed:
- **Paste box auto-hides once a link is embedded** — on the scan cards, the featured Chú Tễu object, and the oral-history players. The audience won't see the input fields after you've pasted.
- **Name + description cleared on all scan cards**, replaced with a subtle "Name & description — to be added" marker so you know where to type later.

The accession numbers, "View in 3D" controls, and embed functionality are untouched.Done — both edits are live and the page loads cleanly.

## User

i dont need this, delete all in this archival plates and delete the section too

## Assistant

_[tool: read_file]_

The user clicked the **"Archival plates · 16"** filter tab in the ledger. They want the entire archival-plates class gone — all 16 plate records, the filter tab, and references to it. Let me remove them.Now let me make the JS edits — remove the photo tab, the 5 hardcoded photo records, and the photo slot definitions:

_[tool: dc_js_str_replace]_

_[tool: dc_js_str_replace]_

_[tool: dc_js_str_replace]_

_[tool: dc_html_str_replace]_

Now update the references to plates and the counts in the template:

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: eval_js]_

_[tool: show_html]_

The hot-reload kept the cached registry. Let me reload the page fresh to pick up the new data.

_[tool: eval_js]_

_[tool: eval_js]_

The archival plates class is fully removed — tabs now read "All records · 37" with no plates tab. Let me confirm the ledger grid visually.

_[tool: screenshot]_

_[tool: done]_

The archival plates class is completely removed — the filter tab is gone, all 16 plate records are deleted, and the counts (37 records · 4 media classes) plus the colophon breakdown are updated to match.

Summary:
- Deleted all 16 archival-plate records (5 catalogued + 11 reserved slots).
- Removed the "Archival plates" filter tab from the ledger.
- Updated record/class counts in the hero, ledger header, "how to read" guide, and colophon so nothing references plates anymore.Done — archival plates and their filter tab are gone, with all counts updated to match. The page loads cleanly.

