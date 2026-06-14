# Interview Layout Design

Before I edit these interviews, I need clarification on a few things:

1. **Layout structure** — Should each of the

_Started 2026-06-13 09:56 UTC_

---

## User

i will paste in the transcript of 2 interviews, please edit the interview part and make only 2 slots for interview. make a place for listening (embed soundcloud), an excerpt of transcript, and box for the most outstanding line (choose for me through transcript). ask me anything to make clear before doing

## Assistant

_[tool: read_file]_

_[tool: list_files]_

_[tool: grep]_

Let me look more closely at the interview-related parts of the file.

_[tool: questions_v2]_

I've read the archive and found the interview/oral-history section. Before I rework it, a few things to pin down:

## User

Questions answered:
- scope: the interview is the oral history; keep the soundscape part, we'll work with them later
- soundcloud_links: Not yet — leave a ready embed slot where I can paste the link later (like the 3D scan slots)
- language: Vietnamese original with a short English translation underneath
- speakers: we have names but idk yet, just leave placeholder for name
- excerpt_length: Short — 2-3 sentences, the most vivid bit

## Assistant

_[tool: read_file]_

Got it. Let me read the exact oral-history block and the logic that drives it (plus the splat-embed pattern I'll reuse for SoundCloud).

_[tool: read_file]_

Let me read the logic class — state, the oral handlers, and the embed-normalize helper I'll adapt for SoundCloud.

_[tool: read_file]_

Now let me read `renderVals` — the oral/transcript values and how rail items expose embed props.

_[tool: read_file]_

_[tool: read_file]_

_[tool: str_replace_edit]_

I have everything I need. I'll replace the single oral-history card with two interview slots (each: SoundCloud embed slot, short VN excerpt + English translation, and a "most outstanding line" box), keeping the soundscape card. Let me make the markup edit.Now the logic — add the SoundCloud normalizer/setter, build the `interviews` array, and remove the now-unused oral-history render values.

_[tool: str_replace_edit]_

## Assistant

_[tool: str_replace_edit]_

_[tool: str_replace_edit]_

_[tool: str_replace_edit]_

Now expose `interviews` and remove the now-unused oral-history render keys.

_[tool: str_replace_edit]_

_[tool: show_html]_

_[tool: show_html]_

Let me scroll to the interview section and screenshot it.

_[tool: eval_js]_

_[tool: save_screenshot]_

_[tool: save_screenshot]_

The first interview slot renders cleanly. Let me scroll down a bit to confirm the excerpt + outstanding-line box and the second interview.

_[tool: save_screenshot]_

_[tool: done]_

Both interview slots render correctly — SoundCloud embed slot up top, VN transcript excerpt with English translation underneath, and the "Most outstanding line" box (VN quote + English + attribution). The soundscape card is preserved below.Done. The interview section is now exactly **2 interview slots** (the soundscape card is kept untouched). Each slot has:

- **Listen** — a SoundCloud embed slot. It shows an empty "Audio slot" placeholder with a paste field + **Embed** button (same pattern as the 3D scan slots). Paste any SoundCloud track/playlist URL — or the full `<iframe>` embed code — and it builds the player automatically. Links persist across reloads.
- **Transcript excerpt** — the most vivid 2–3 sentences in Vietnamese, with a short English translation in italics underneath.
- **Most outstanding line** — a boxed pull-quote I picked from each transcript (VN + English):
  - Interview 1 (the carver): *"Trong quá trình lao động, người ta sáng tạo — cái đấy nhiều khi trường lớp không dạy được."*
  - Interview 2 (Hồng Quang): *"Bảo tồn nghề múa rối nước này là bảo tồn rất nhiều nghề."*

Speaker names are left as `[ name pending ]` placeholders for you to fill in. Just tell me the names (and the SoundCloud links) whenever you have them and I'll drop them in.

## User

for this section, we only have a 360 vlog, only 1 video. please change it to only 1. and it's quite casual too, like a vlog full of b-rolls

## Assistant

_[tool: read_file]_

The "360° FILM · 12" comes from the ledger registry generating many reserved 360 slots plus 2 live ones. Let me collapse that to a single casual vlog record. Let me check the footer count line too.

_[tool: grep]_

_[tool: read_file]_

_[tool: str_replace_edit]_

I'll calculate: removing the 2 live 360 entries + the 10 generated 360 slots and adding 1 casual vlog brings the registry from 64 → 53 records, with the 360 tab showing just 1. Let me make the edits.

_[tool: eval_js]_

Let me verify the 360 tab now shows just 1 and the vlog card reads casually.

_[tool: show_html]_

The page is showing cached registry. Let me reload it.

_[tool: eval_js]_

The 360° section now holds a single record. Let me confirm the vlog card renders properly under the 360 filter.

_[tool: save_screenshot]_

_[tool: save_screenshot]_

The filter applied (count = 1). Let me capture the actual vlog card in the ledger grid.

_[tool: save_screenshot]_

The 360° section is now a single, casual vlog entry — **"A Day at the Pond — 360° Vlog"** (14:20, tagged *vlog · b-roll · field visit*), described as a loose handheld walkaround of the village rather than a polished film. The tab reads "360° film · 1", and the total dropped to 53 records.

_[tool: done]_

Done. The 360° film section now holds just the one casual vlog ("A Day at the Pond — 360° Vlog") — b-roll-style, field-visit tone — and all the counts updated accordingly (360° film · 1, 53 records total).

## User

one more slot

## Assistant

_[tool: str_replace_edit]_

The user wants one more slot in the "Explore in 3D" scans rail (built from live splat records, currently 4). I'll promote one reserved subject into a live rail slot — keeping the total count balanced.The scans rail now has a 5th 3D object slot (Ông Câu, the Old Fisherman) with its own embed field, and the ledger counts stay balanced at 12 object scans / 53 records. Let me reload and confirm the rail shows five.

_[tool: show_html]_

_[tool: eval_js]_

The rail now shows five 3D object slots (MRN.3D.001–005), the fifth being **Ông Câu, the Old Fisherman** with its own "View in 3D" + SuperSplat embed field. Counts stay balanced (12 object scans, 53 records).

_[tool: done]_

Added — the "Explore in 3D" rail now has five slots, with the new one (Ông Câu, the Old Fisherman) ready for its own SuperSplat embed.

