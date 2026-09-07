# Production Brief - AI Tools Drop, Week of 7 September 2026

**Episode 5.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 15:10 (measured, 2,420 narration words at 160 wpm)
- Short runtime target: 1:22 (measured, 218 narration words)

---

## 0. Read this before you spend anything

**Backlog warning. This is the fifth unrendered episode in `pending/`.**

Queued and not yet rendered:

| Directory | Week | Status |
| --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | This brief |

Episodes 3 and 4 both carried an escalation asking for a direction on the backlog and neither was answered. Do not render five episodes on the assumption that all five should ship. Four of these are now stale as weekly news - episodes 1 through 3 reference pricing that has since changed, and episode 1 is five weeks old.

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 15:10 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:22 | TikTok, Instagram Reels, YouTube Shorts |

Both deliverables carry the AI disclosure card described in section 8. Neither ships without it.

Audio: single narration track per deliverable, no background music bed unless a stage render shows the pacing needs one. If music is added, use a royalty-free track - do not use Lyria output for this episode, since the episode itself discusses Lyria and using it would need its own disclosure.

---

## 2. ElevenLabs voiceover

```
voice_id:        P1LmKcX63Ihgqy11sVRt   (Andrew, South African male)
model_id:        eleven_multilingual_v2
stability:       0.60
similarity_boost: 0.75
style:           0.15
use_speaker_boost: true
output_format:   mp3_44100_128
```

**Render one API call per segment.** Seventeen calls for deliverable A, five for deliverable B. Do not batch the full script into a single request - a single mispronunciation then costs one segment to redo, not the whole episode.

Name the files `seg01.mp3` through `seg17.mp3` for A and `short01.mp3` through `short05.mp3` for B, in an `audio/` subdirectory.

**Pronunciation guide is in the script header.** Read it before rendering. This week's high-risk tokens are `n8n` (say en-EIGHT-en), `POPIA` (poh-PEE-uh), `Tadata` (tah-DAH-tah), `Syspro` (SIS-pro), `Tajima` (tah-JEE-mah), `isiZulu` (iss-ee-ZOO-loo), `Vulavula` (voo-lah-VOO-lah) and `MagiCrew` (MAJ-ee-crew).

**Numbers are written longhand in the narration deliberately** so the model reads them correctly, and as digits in the overlay text. Do not reconcile the two. If you "fix" the narration to use digits, the voice model will read R15.97 as something unusable.

After rendering, listen to segments 2, 5, 11, 13 and 14 specifically - those carry the highest density of awkward tokens.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers. The ratio is what keeps the cost down.

**Layer 1 - Kling motion clips, 5 seconds each.** Five clips this episode. Episode 4 used only three and the stage render read as static in the middle third; the series lesson is that argument-driven episodes need three to five and product tours need more. This episode is a product tour with an argument running through it, so five is correct. Use them at segments 1, 4, 5, 6 and 8.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images. Do not regenerate them.

**Layer 3 - Shotstack motion graphics.** This carries the bulk of the runtime, and it is the cheapest layer. Every pricing table, comparison bar, checklist and map graphic is built here from text and shapes, not generated.

Rough split by runtime: Kling about 25 seconds total, Soul stills about 2 minutes, Shotstack graphics the remaining 12-plus minutes.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** These live in `assets/ai-tools-drop/`:

- `B1` - abstract data-flow field, dark, amber accents
- `B2` - desk workspace, low light, screens
- `B3` - abstract network mesh
- `B6` - dusk cityscape, warm
- `A16` - Johannesburg skyline

**This is the fifth brief that has asked for this caching.** If the directory is empty or the files are missing, regenerate once and commit them so the sixth brief does not have to ask again.

Assignments this episode:

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 3 (Gemini) | Slow push in |
| A16 | 5 (Syspro, Johannesburg) | Slow pull back |
| B3 | 10 (AI Toolbox) | Slow drift left |
| B2 | 15 (What I would try) | Static, no motion - let the text carry it |
| B6 | 17 (Close) | Slow Ken Burns push |

If a new still is genuinely needed, the endpoint is:

```
POST https://platform.higgsfield.ai/v1/text2image/soul
Header: hf-api-key: ${HF_API_KEY}
Body:  width_and_height: "2048x1152"   (or "1152x2048" for vertical)
       quality: "1080p"
       enhance_prompt: true
```

Poll `GET https://platform.higgsfield.ai/v1/jobs/{id}` until complete.

Style direction for any new still: documentary realism, low-key lighting, no text in frame, no logos, no recognisable faces, no on-screen readable UI. Palette biased to `#111111` with `#F5C542` accents so it composites cleanly against the overlay layer.

---

## 5. Higgsfield Kling - image to video

```
POST https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video
Header: Authorization: Key ${HF_API_KEY}:${HF_SECRET}
Duration: 5 seconds per clip
```

Five clips. Prompts:

| Clip | Segment | Prompt direction |
| --- | --- | --- |
| K1 | 1 - Cold open | Slow dolly push down a dark server aisle, a single amber indicator light pulsing. No text, no people. Cold, controlled, slightly ominous. |
| K2 | 4 - ThunderPhone | An empty reception desk in low evening light, a desk phone ringing, nobody present. Static camera, subtle handset vibration. |
| K3 | 5 - Syspro Torque | Industrial factory floor at working pace, machinery in motion, mid-shot, no readable branding, no faces. |
| K4 | 6 - Stitch AI | Close macro on an embroidery machine head moving quickly across stretched fabric, thread feeding. Shallow depth of field. |
| K5 | 8 - GPT-6 Astra | A padlock form assembling from geometric fragments then dissolving back apart. Abstract, dark background, amber and red accents. |

Negative direction on all five: no text, no watermarks, no logos, no identifiable faces, no fast camera whips.

Render each to stage quality first and inspect. K5 is the one most likely to come back looking like stock cliche - if it does, replace it with a Shotstack-built abstract rather than re-rolling Kling twice.

---

## 6. Shotstack composition

```
POST https://api.shotstack.io/edit/stage/render
Header: x-api-key: ${SHOTSTACK_API_KEY_STAGE}
```

**Stage endpoint only for this pass.** Production endpoint is gated behind human approval per section 0.

Palette:

```
background: #111111
text:       #FFFFFF
accent:     #F5C542
warning:    #E5533D
```

Overlay styles: use `style: "minimal"` for body overlays and `style: "future"` for full-frame title cards.

Composition rules:

- Overlay text enters on a 0.4 second fade, holds, exits on a 0.3 second fade. No slides, no bounces.
- Body overlay text sits in the lower third for 16:9 and in the middle band for 9:16, never within 12 percent of any edge.
- Any figure the script flags as uncertain gets the `warning` colour, not the accent. That covers the Fotor second-hand pricing, the ThunderPhone hosting line, the Tadata credit definition and the Syspro no-price line.
- The word CRITICAL in segments 1 and 8 renders in `warning` at full-frame scale, held with no motion behind it.
- Segment 8's `CRITICAL FOR CYBER` card holds four seconds static. Do not add motion to it.
- Segment 3's Gemini pricing table row holds four seconds. This is the single most important visual in the episode.

Two renders per deliverable minimum: one stage pass for inspection, one after any corrections.

---

## 7. ASCII-safe overlay text - mandatory

Every string that goes into a Shotstack payload must be plain ASCII. No em dashes, no en dashes, no curly quotes, no ellipsis characters, no arrows, no non-breaking spaces, no middots.

This is not a style preference. Non-ASCII characters in overlay payloads corrupt on Windows and PowerShell tooling and render as mojibake in the output video, which is only discovered after paying for the render.

Before building any payload, run:

```
python3 /home/user/workspace/ascii_fix.py script.md social.md article.md BRIEF.md
```

It prints `<file> OK` per file when clean. If it reports replacements, re-read the changed lines to confirm the substitution did not break meaning, then rebuild the payload.

The fenced ON-SCREEN TEXT blocks in `script.md` and `social.md` are already ASCII-clean and are the authoritative source for overlay strings. Copy from them. Do not retype overlay text from the narration.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 14:20 to 14:34. Static card, `#111111` background, white text, no motion.

**Deliverable B:** SHORT SEGMENT 5, from 1:10 to 1:22, disclosure card first, then the WhatsApp CTA.

Card text, exactly:

```
AI DISCLOSURE

Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**Minimum five seconds on screen in both deliverables. This segment must not be cut for runtime.** If the episode runs long, trim segment 13 or 14 instead.

**Platform declaration is separate and additional.** At upload, set the AI-generated content toggle on YouTube, TikTok and Instagram. The on-video card does not satisfy the platform requirement, and the platform toggle does not satisfy the on-video requirement. Both are needed.

---

## 9. Execution flow for Claude Code

1. Read `script.md` and `social.md` fully before touching an API.
2. Run `ascii_fix.py` across all four files in this directory. Confirm four `OK` lines.
3. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. If missing, generate once and commit.
4. Render narration: 17 ElevenLabs calls for A, 5 for B, one per segment, into `audio/`.
5. Listen to segments 2, 5, 11, 13, 14 and confirm the pronunciation guide held. Re-render individual segments as needed.
6. Measure actual audio durations per segment. **The timing table in `script.md` is a 160 wpm estimate. Rebuild the real timing table from the rendered audio** and use those numbers for YouTube chapters, not the estimate.
7. Render the five Kling clips to stage. Inspect each.
8. Build the Shotstack stage payload for deliverable A against the real audio durations.
9. Submit deliverable A to the Shotstack **stage** endpoint. Download and inspect end to end.
10. Repeat 8 and 9 for deliverable B.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then work through section 11.

Do not proceed past step 11 without approval, and do not batch steps 1 through 11 for all five queued episodes before reporting.

---

## 10. Cost breakdown

Stage-pass estimate for this episode only:

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 15,000 characters across both deliverables | $1.40 - $1.90 |
| Higgsfield Soul stills | 0 new if cache present, otherwise 5 | $0.00 - $1.50 |
| Higgsfield Kling clips | 5 clips at 5 seconds | $3.25 - $4.50 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 5 stage total** | | **$4.65 - $8.90** |

At R15.97 that is roughly **R74 to R142**.

Prior episodes for comparison: episode 1 $18-28, episode 2 $16.35-24.65, episode 3 $13.44-19.68, episode 4 $5.85-7.38. The downward trend is the hybrid approach and the image cache working as intended.

**Five-episode combined stage cost, if all five are rendered: approximately $58 to $88, or R930 to R1,405.** Production renders are additional. That number is the reason section 0 asks for a decision before anything runs.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in both deliverables
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge
- [ ] Audio levels consistent across all segments, no clipping, no dead air over two seconds
- [ ] All pronunciation-guide tokens read correctly on playback
- [ ] YouTube chapters rebuilt from rendered audio durations, not the estimate table
- [ ] Fotor pricing labelled second-hand and unconfirmed wherever it appears on screen
- [ ] Every uncertain figure rendered in the warning colour, not the accent
- [ ] WhatsApp broadcast confirmed under 700 characters (currently 686)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram
- [ ] Every claim in `social.md` section 9 re-confirmed against its source URL
- [ ] Section 14 updated with live post links

---

## 12. Series notes

Carry these forward.

- **Write the script lean from the start.** Episode 4 needed three trim passes from 18:37 down to 14:57. This episode was written to a budget of roughly 150 to 165 words per tool segment and needed two light passes to land at 15:10. Budget 150-165 words per tool, not 200.
- **Measure before writing the timing table.** Never put an estimated table in the script and leave it unsynced to the headings. Measure, then write the table and the headings in the same pass.
- **Kling clip count matters.** Three clips read as static in episode 4. Five is the right number for a ten-tool episode.
- **The image cache is the single biggest cost saver.** Protect it.
- **Uncertainty is content, not a defect.** This episode's strongest material is the FX spread, the zero POPIA mentions, the Fotor pricing page that renders no price and the privacy policy that 403s. Render those honestly rather than smoothing them over.
- **The unrendered backlog is now five episodes.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 5
week_of: 2026-09-07
window_covered: 2026-08-31 to 2026-09-07
tools_covered: 10
top_pick: Gemini 3.8 Flash
warning_item: GPT-6 Astra (first OpenAI model rated Critical for cyber)
best_free_item: Stitch AI by Dynamic Mockups
only_sa_launch: Syspro Torque (Johannesburg)
best_data_disclosure: AI Toolbox 3.0 (DigitalOcean, Frankfurt)
fx_rate_used: 15.97
fx_rate_date: 2026-09-06
fx_source_spread_pct: 11
long_form_runtime_estimate: "15:10"
long_form_words: 2420
short_runtime_estimate: "1:22"
short_words: 218
kling_clips: 5
soul_stills_new: 0
soul_stills_reused: 5
stage_cost_estimate_usd: "4.65 - 8.90"
stage_cost_estimate_zar: "74 - 142"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
backlog_episodes_unrendered: 5
popia_mentions_across_vendors: 0
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the list in episode 4's brief, which remains in force.

```
Gemini 3.8 Flash, Gemini 3.8 Flash Cyber, ThunderPhone, Syspro Torque,
Stitch AI, Dynamic Mockups, Claude Fable 5.1, Claude Mythos 5.1,
GPT-6 Astra, Tadata, AI Toolbox 3.0, MagiCrew, Video Agent by Fotor,
Dial, Lyria 3.5, n8n 2.37.x, n8n 2.38.x, CleanShot 5.0,
Anthropic ant CLI 1.30.0, Refiant Protea, Framer AI Agents
```

### Carried forward for future episodes

- **African compute, as a standalone segment.** Stratos Lab, ECOBLOX and Digital Parks Africa announced an African AI cloud on 26 August, five days outside this window. Given that nine of ten tools this week route data offshore, this deserves its own treatment rather than a footnote.
- **Lelapa AI and Vulavula.** South African multilingual speech. Surfaced again and could not be date-verified inside the window. The local story most worth covering properly.

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
