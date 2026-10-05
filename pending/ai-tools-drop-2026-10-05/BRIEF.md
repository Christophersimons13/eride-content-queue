# Production Brief - AI Tools Drop, Week of 5 October 2026

**Episode 9.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 15:08 (measured, 2,413 narration words at 160 wpm)
- Short runtime target: 1:07 (measured, 179 narration words)

---

## 0. Read this before you spend anything

**Backlog warning. This is the ninth unrendered episode in `pending/`.**

Checked on 5 October: `pending/` holds eight earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 5 Oct | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 9 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 8 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 7 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 5 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 4 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 3 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 2 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 1 week | Not rendered. **1 October wording is now stale** - "from the first of October" must become "since". 2 November date still in the future. |
| `ai-tools-drop-2026-10-05` | 5 October | Current | This brief |

Michael has been asked to choose between rendering only the current episode (recommended), current plus previous, all nine, or pausing. **No answer yet. Do not render any backlog episode without his written choice.**

**This episode carries three time-limited items.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Eleven v4 API discount (72 percent) and Creator+ 3x credits | **12 October 2026** | Segments 2, 3 and 17, short segment 3, the WhatsApp broadcast, YouTube description and all captions present it as current. After 12 October, cut the discount lines and restate list price only. **Seven days out from this brief.** |
| WhatsApp Business Platform reply billing | Took effect **1 October 2026** | Already past tense in the script. No change needed. |
| MAI-Transcribe-2-Streaming introductory price | **31 December 2026** | The $0.54 per hour figure in segment 9 lapses. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**One note on this episode's top pick, so nobody acts on it by accident.** Segment 3 covers Eleven v4, a newer ElevenLabs model than the `eleven_multilingual_v2` this pipeline uses. That is editorial content, not a pipeline instruction. **Do not switch models for this episode.** Note that v4 does not support the Style slider or SSML, so the section 2 settings would not carry across unchanged. Any model change is Michael's decision.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 15:08 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:07 | TikTok, Instagram Reels, YouTube Shorts |

Both deliverables carry the AI disclosure described in section 8. Neither ships without it.

Audio: single narration track per deliverable, no background music bed unless a stage render shows the pacing needs one. If music is added, use a royalty-free track.

---

## 2. ElevenLabs voiceover

```
voice_id:         P1LmKcX63Ihgqy11sVRt   (Andrew, South African male)
model_id:         eleven_multilingual_v2
stability:        0.60
similarity_boost: 0.75
style:            0.15
use_speaker_boost: true
output_format:    mp3_44100_128
```

**Render one API call per segment.** Seventeen calls for deliverable A, five for deliverable B. Do not batch.

Name the files `seg01.mp3` through `seg17.mp3` for A and `short01.mp3` through `short05.mp3` for B, in an `audio/` subdirectory.

**Voice direction.** Warm, measured, South African English. Conversational, not presenter-bright. No hype, no rising sales cadence. Slight slowdown on every caveat line ("Here is the honest part", "Two catches", "I could not confirm"). Those lines are the series' credibility and must not be rushed.

**Pronunciation guide is in the script header.** This week's high-risk tokens: `Clef` (klef - not "cleff" or "clay"), `Suno` (SOO-noh), `MAI` (em-ay-EYE, spelled out), `Wati` (WAH-tee), `Exten` (EX-ten), `Fort Hare` (fort HAIR), and the language names `isiZulu`, `isiXhosa`, `Sesotho`, `Setswana`. Listen to segments 3, 8, 9 and 13 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Five clips, K1 to K5, named in the script's B-ROLL notes.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images once they exist.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime. Every price card, counter, flow diagram and checklist is built here.

Rough split by runtime: Kling about 25 seconds, Soul stills about 2 minutes, Shotstack the remaining 12-plus minutes.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`:

- `B1` - abstract data-flow field, dark, amber accents
- `B2` - desk workspace, low light, screens (used this week as phone and message streams)
- `B3` - abstract network mesh
- `B6` - dusk cityscape, warm (used this week behind the fashion and try-on segment; if it reads wrong, fall back to a Shotstack card)
- `A16` - Johannesburg skyline

**Ninth brief asking for this cache. Checked on 5 October: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

Assignments this episode:

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 1 (Cold open) and 15 (dimmed) | Slow push in |
| B2 | 4 (WhatsApp pricing) | Ken Burns, slow push in |
| B3 | 6 (GPT-6.1 Sol) | Ken Burns, slow drift left, cool grade |
| B6 | 10 (ChatGPT try-on) | Ken Burns, warm |
| A16 | 13 (SA corner) and 17 (Close) | Slow push in; push out and fade on the close |

If a new still is genuinely needed:

```
POST https://platform.higgsfield.ai/v1/text2image/soul
Header: hf-api-key: ${HF_API_KEY}
Body:  width_and_height: "2048x1152"   (or "1152x2048" for vertical)
       quality: "1080p"
       enhance_prompt: true
```

Poll `GET https://platform.higgsfield.ai/v1/jobs/{id}` until complete.

Style direction: documentary realism, low-key lighting, no text in frame, no logos, no recognisable faces, no readable UI. Palette biased to `#111111` with `#F5C542` accents.

---

## 5. Higgsfield Kling - image to video

```
POST https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video
Header: Authorization: Key ${HF_API_KEY}:${HF_SECRET}
Duration: 5 seconds per clip
```

| Clip | Segment | Prompt direction |
| --- | --- | --- |
| K1 | 3 - Eleven v4 | An abstract animated waveform rising over a dark studio desk with a microphone silhouette, warm amber light. No text, no people. |
| K2 | 5 - Shopify Canvas | A generic online storefront layout assembling itself tile by tile on a dark background. Blank image blocks, no readable text, no logos. |
| K3 | 7 - Dots, Space and Pages | Small glowing amber dots drifting between blank floating document panels. Abstract, no readable text. |
| K4 | 9 - Microsoft MAI | A headset resting on a desk in a dim call centre, soft lines of abstract caption bars flowing beneath it. No readable text, no faces. |
| K5 | 11 - Suno Speech | Abstract sound bars morphing into the outline of a speaking silhouette, then back. Dark background, amber edge light. |

Negative direction on all five: no text, no watermarks, no logos, no identifiable faces, no fast camera whips.

**K2 is the one most likely to fail.** Kling tends to put readable store UI or a brand mark on storefront layouts. Shopify's logo and any readable product names must not appear. If it comes back with either, replace K2 with a Shotstack-built tile animation rather than re-rolling twice.

---

## 6. Shotstack composition

```
POST https://api.shotstack.io/edit/stage/render
Header: x-api-key: ${SHOTSTACK_API_KEY_STAGE}
```

**Stage endpoint only for this pass.**

Palette:

```
background: #111111
text:       #FFFFFF
accent:     #F5C542
warning:    #E5533D
```

Overlay styles: `style: "minimal"` for body overlays, `style: "future"` for full-frame title cards.

Composition rules:

- Overlay text enters on a 0.4 second fade, holds, exits on a 0.3 second fade. No slides, no bounces.
- Body overlay text sits in the lower third for 16:9 and the middle band for 9:16, never within 12 percent of any edge.
- **Uncertain or negative items render in `warning`, not accent.** This episode: NOT LISTED column in segment 3; "Sources disagree" and "SA rate: not confirmed" in segment 4; NOT AT LAUNCH in segment 5; "limited preview" and "not published" in segment 6; the agents security line in segment 7; UNCONFIRMED in segment 8; "SA languages: NOT CONFIRMED" in segment 9; the PRIVACY block in segment 10; NO COMMERCIAL RIGHTS in segment 11; every NOT AVAILABLE IN SA stamp in segment 12; the zero counts in segment 13; "took effect 1 OCT" in segment 15.
- **Segment 1:** a generic chat bubble, no WhatsApp logo or green, types a short reply; a price tag drops onto it. Built in Shotstack, not Kling.
- **Segment 3:** split card. ON THE LIST in accent, NOT LISTED in warning, side by side, equal weight.
- **Segment 4:** a counter ticks from 998 to 1,001; the last digit turns warning colour at 1,001.
- **Segment 8:** three messages sort into three bins labelled BOOKING, COMPLAINT, HUMAN.
- **Segment 14:** a plain flow diagram with ASCII labels only. Use drawn lines, not arrow glyphs.
- On deliverable B, short segment 1 is a **hard cut in on frame one, no fade**.

Two renders per deliverable minimum: one stage pass for inspection, one after corrections.

---

## 7. ASCII-safe overlay text - mandatory

Every string that goes into a Shotstack payload must be plain ASCII. No em dashes, no en dashes, no curly quotes, no ellipsis characters, no arrows, no non-breaking spaces, no middots.

Non-ASCII characters in overlay payloads corrupt on Windows and PowerShell tooling and render as mojibake in the output video, which is only discovered after paying for the render.

Before building any payload, run:

```
python3 /home/user/workspace/ascii_fix.py script.md social.md article.md BRIEF.md
```

It prints `<file> OK` per file when clean. The tool converts em dashes to ` - ` with padding; follow it with `sed -i 's/ - / - /g'` on any modified file.

The fenced ON-SCREEN TEXT blocks in `script.md` and `social.md` are the authoritative source for overlay strings. Copy from them.

**Protected strings.** `isiZulu` and `isiXhosa` keep their lowercase prefixes - correct orthography, not typos. `"eligible markets"` in segment 7 is quoted vendor copy and keeps its quote marks.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 13:43 to 14:08. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:07, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

Card text for deliverable A, exactly:

```
AI DISCLOSURE
Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**Minimum five seconds on screen. Never cut for runtime.** If the episode runs long, trim segment 15 first, then 14, then 13.

**Platform declaration is separate and additional.** At upload, set the AI-generated content toggle on YouTube, TikTok, Instagram and Facebook. Both the on-video card and the platform toggle are required.

---

## 9. Execution flow for Claude Code

1. Read `script.md` and `social.md` fully before touching an API.
2. **Check the date.** If it is after 12 October 2026, remove the Eleven v4 discount and triple-credit lines everywhere listed in section 0 before rendering.
3. Run `ascii_fix.py` across all four files. Confirm four `OK` lines. Confirm the protected strings in section 7 survived intact.
4. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 5 October.** Generate once and commit.
5. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
6. Listen to segments 3, 8, 9 and 13 first for names. Re-render individual segments as needed.
7. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters in `social.md` section 3 from rendered audio**, not the 160 wpm estimate.
8. Render the five Kling clips to stage. Inspect each, K2 against the no-logo brief specifically.
9. Build the Shotstack stage payload for deliverable A against the real audio durations.
10. Submit deliverable A to the **stage** endpoint. Download and inspect end to end.
11. Repeat 9 and 10 for deliverable B, including the persistent disclosure caption.
12. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
13. On approval: production render, then section 11.

Do not proceed past step 12 without approval, and do not batch steps 1 to 12 across all nine queued episodes before reporting.

---

## 10. Cost breakdown

Stage-pass estimate for this episode only:

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 15,000 characters across both deliverables | $1.35 - $1.90 |
| Higgsfield Soul stills | 5 new (cache absent), 0 thereafter | $0.00 - $1.50 |
| Higgsfield Kling clips | 5 clips at 5 seconds | $3.25 - $4.50 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 9 stage total** | | **$4.60 - $8.90** |

At R16.67 that is roughly **R77 to R148**.

**Nine-episode combined stage cost, if all nine are rendered: approximately $76.70 to $124.30, or about R1,279 to R2,072 at R16.67.** Production renders are additional, typically two to three times stage cost.

Three earlier episodes (6, 7 and 8) need content edits before they can be published.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] `isiZulu` and `isiXhosa` render with correct lowercase prefixes on screen
- [ ] No WhatsApp, Meta, Shopify, OpenAI, Google, Microsoft, Cloudflare, Amazon, ElevenLabs or Suno logos in any generated footage
- [ ] Segment 1 chat bubble is generic - no WhatsApp green, no WhatsApp logo
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] YouTube chapters in `social.md` rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] The Clef price appears only with UNCONFIRMED beside it; the SA WhatsApp rate is never stated as a figure
- [ ] **12 October wording** correct for the publication date (see section 9 step 2)
- [ ] `[LINK]` placeholder in the WhatsApp broadcast replaced with the real video URL
- [ ] WhatsApp broadcast re-counted after the link is inserted, still under 700 characters (currently 454 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **The lean budget held again.** 145 to 158 words per tool, 15:08 on the first pass.
- **Separate "not for us yet" from the list.** Gemini 4 Argon and Muse for Small Business were the two biggest launches of the week and neither is usable in South Africa. They sit in their own segment so the main list stays honest.
- **Profiles are not launches.** Exten AI is South African and interesting, but it launched earlier in 2026. It went in the SA corner, not the list.
- **Pricing changes count when they bite SMBs.** The WhatsApp change is labelled "not a tool" on air and in the overlay.
- **Last week's warning followed up.** Segment 15 notes the Microsoft uplift took effect on 1 October.
- **The unrendered backlog is now nine episodes, three need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 9
week_of: 2026-10-05
window_covered: 2026-09-28 to 2026-10-05
tools_covered: 9
platform_changes_among_them: 1 (WhatsApp Business Platform reply billing)
top_pick: Eleven v4
second_pick: Shopify Canvas
action_item: Ask WhatsApp API provider for September reply volume and October cost
not_available_in_sa: Gemini 4 Argon, Muse for Small Business
sa_story: Exten AI (profile, not a new launch)
sa_languages_eleven_v4: Afrikaans listed; isiZulu, isiXhosa, Sesotho, Setswana not listed
popia_vendor_references: 0
new_african_regions_announced: 0
content_expiry_date: 2026-10-12
content_expiry_reason: Eleven v4 discount and Creator+ 3x credits end
secondary_expiry_date: 2026-12-31
secondary_expiry_reason: MAI-Transcribe-2-Streaming introductory price ends
fx_rate_used: 16.67
fx_rate_date: 2026-10-05
fx_sources: 2
long_form_runtime_estimate: "15:08"
long_form_words: 2413
long_form_segments: 17
short_runtime_estimate: "1:07"
short_words: 179
short_segments: 5
whatsapp_broadcast_chars: 454
kling_clips: 5
soul_stills_new: 5 (cache absent in repo)
stage_cost_estimate_usd: "4.60 - 8.90"
stage_cost_estimate_zar: "77 - 148"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
backlog_episodes_unrendered: 9
backlog_episodes_needing_edits: 3 (episodes 6, 7, 8)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 8, which remain in force.

```
Eleven v4, Eleven v4 Turbo, WhatsApp Business Platform October 2026 pricing,
Shopify Canvas, GPT-6.1 Sol, OpenAI Decisions API, OpenAI Agents API computer use,
Dots, ChatGPT Space, ChatGPT Pages, Codex cloud, Cloudflare Clef, Clef-flash,
Strands Decider 2B, MAI-Transcribe-2-Streaming, MAI-Voice-2.1, MAI-Voice-2.1-Flash,
ChatGPT virtual try-on, ChatGPT Images 2.5, Suno Speech, Gemini 4 Argon,
Muse for Small Business, Exten AI, n8n Agents, Tavus Griffin-Lite
```

Exceptions: re-cover Gemini 4 Argon or Muse for Small Business only if they become available in South Africa; re-cover OpenAI Decisions API only when a price is published; re-cover ChatGPT Slides when it ships.

### Carried forward for future episodes

- **Meta smart glasses in South Africa.** TechCentral says this year, another source says 2027. Cover when a date and a rand price are official.
- **WhatsApp South African rate.** Find Meta's official ZAR or South Africa rate card for service messages and correct the per-account or per-number question.
- **Exten AI.** Cover when it opens publicly with pricing.

---

## 14. Post links

Fill in at upload.

| Platform | URL | Posted |
| --- | --- | --- |
| WhatsApp channel | | |
| YouTube (long form) | | |
| Facebook | | |
| TikTok | | |
| Instagram Reels | | |
| YouTube Shorts | | |
