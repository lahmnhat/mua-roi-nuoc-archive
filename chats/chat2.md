# PLY Upload Alternative

_Started 2026-06-13 03:55 UTC_

---

## User

since i cant upload .ply scan, please transform every placeholders to upload .ply to website embed, i will attach supersplat links

## Assistant

_[tool: list_files]_

_[tool: read_file]_

_[tool: read_file]_

I need to find all the ".ply scan upload" placeholders. Let me search for them.

_[tool: grep]_

_[tool: read_file]_

This is a substantial custom file with a hand-built PLY point-cloud viewer. Let me read the relevant template and logic sections before rewriting the embed mechanism.

_[tool: read_file]_

Now I understand the placeholder structure. There are three upload spots (featured preview, featured active viewer, and each rail card) plus a custom canvas point-cloud viewer. Since SuperSplat embeds *are* the viewer, I'll replace the upload+canvas machinery with iframe embeds driven by pasted SuperSplat links. Let me read the rest of the logic first.

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

I now have the full picture. Let me read the remaining PLY/viewer machinery (975–1110) so I can cleanly remove it.

_[tool: update_todos]_

I have the complete picture. The file uses a hand-built canvas point-cloud viewer plus a `.ply` file-upload/parser. I'll replace all of that with SuperSplat **iframe embeds** driven by pasted share links (persisted to localStorage), in all three spots: the featured object (preview + active), and every rail card. Let me make the changes.

_[tool: run_script]_

All logic edits landed. Now the template edits (the three placeholder areas + remove the dead zoom overlay + copy).

_[tool: run_script]_

_[tool: grep]_

All edits applied. Let me check for any leftover references to the removed machinery.Clean — no dangling references. Let me render it and verify.

_[tool: show_html]_

_[tool: show_html]_

_[tool: eval_js]_

Header renders. Let me verify the featured embed flow functionally — paste a test SuperSplat link, click Embed, and confirm an iframe mounts.

_[tool: eval_js]_

_[tool: eval_js]_

Embed flow works and persists correctly, normalizing `superspl.at/s/…` to a full URL. Let me clear the test value I just wrote so the user starts with empty slots.

_[tool: eval_js]_

_[tool: update_todos]_

Test value reset to empty. Let me finalize.Done. Every `.ply` upload placeholder is now a **SuperSplat website embed**:

- **Featured object** (Chú Tễu) and **every rail card** now take a SuperSplat share link instead of a file. Paste a link → hit **Embed** (or press Enter) and the published splat loads as a live, orbitable `<iframe>`.
- The input is forgiving: it accepts a full `superspl.at/s/…` URL, a bare share ID, or even a pasted `<iframe src="…">` snippet — it normalizes them all.
- Links **persist** (saved locally), so they survive reloads. The old hand-built point-cloud viewer and `.ply` parser are removed.

Send me your SuperSplat links whenever you're ready and I can hard-code them in as defaults so the slots come pre-filled — otherwise you can just paste them straight into the page.

_[tool: done]_

Loaded cleanly with no console errors, and the background verifier is running. You're all set — paste your SuperSplat links into any slot, or send them to me to wire in as defaults.

