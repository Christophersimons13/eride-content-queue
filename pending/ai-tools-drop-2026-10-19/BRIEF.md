# Production Brief - AI Tools Drop, Week of 19 October 2026

**Episode 11.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 14:00 (measured, 2,232 narration words at 160 wpm)
- Short runtime target: 1:01 (measured, 162 narration words)

---

## 0. Read this before you spend anything

**Backlog warning. This is the eleventh unrendered episode in `pending/`.**

Checked on 19 October: `pending/` holds ten earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 19 Oct | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 11 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 10 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 9 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 7 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 6 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 5 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 4 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 3 weeks | Not rendered. **1 October wording is stale.** |
| `ai-tools-drop-2026-10-05` | 5 October | 2 weeks | Not rendered. **Content expired 12 October.** |
| `ai-tools-drop-2026-10-12` | 12 October | 1 week | Not rendered. **"Ends today" Eleven v4 line expired 13 October**; Gemini agent and Muse lines may also date. |
| `ai-tools-drop-2026-10-19` | 19 October | Current | This brief |

Five earlier episodes (6 to 10) now need content edits before they could be published. Michael has been asked whether to keep the series running, pause it or stop it. **No answer yet. Do not render any episode, including this one, without his written choice.**

**Time-limited items in this episode.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Fish Audio Drama 3 launch price (USD 10 per 1M characters) | **12 November 2026** | Segment 8 and the article pricing line. Restate list price only after that. |
| Gemini 4 Argon introductory API price | **30 November 2026** | Segment 5 and the article. After that, the price is USD 4 / USD 20. |
| AI Expo Africa, Sandton | **28 and 29 October 2026** | Segment 12 and the YouTube description refer to it as upcoming. |
| Gemini agent general availability | Expected end October or early November | Segment 14 may be out of date. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**Editorial note.** Segments 8 and 9 cover Fish Audio Drama 3 and ElevenLabs Instant Soundtracks. That is editorial content, not a pipeline instruction. **Do not switch voice vendors, add music or change models for this episode.** Any change is Michael's decision.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 14:00 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:01 | TikTok, Instagram Reels, YouTube Shorts |

Both deliverables carry the AI disclosure described in section 8. Neither ships without it.

Audio: single narration track per deliverable, no background music bed unless a stage render shows the pacing needs one. If music is added, use a royalty-free track.

**Short runtime note.** The short measures 1:01 at 160 wpm, just over the 60-second floor. If the rendered narration lands under 60 seconds, hold the CTA card for two extra seconds rather than adding words.

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

**Pronunciation guide is in the script header.** This week's high-risk tokens: `llama.cpp` (LAH-mah dot see-pee-pee), `Indra` (IN-drah), `OCR` (spelled out, oh-see-AR), `xAI` (ex-ay-EYE), `Argon` (AR-gon), `Funda Nam` (FOON-dah NAHM), `ORT` (spelled out), and the language names `isiZulu` and `isiXhosa`. Listen to segments 3, 4, 7 and 12 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Three clips this week, K1 to K3.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images once they exist.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime.

Rough split by runtime: Kling about 15 seconds, Soul stills about 2 minutes, Shotstack the remainder.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`: `B1` (abstract data-flow field), `B2` (desk workspace, low light), `B3` (abstract network mesh), `B6` (dusk cityscape, warm), `A16` (Johannesburg skyline).

**Eleventh brief asking for this cache. Checked on 19 October: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 9, 11 and 14 (dimmed) | Slow push in |
| B2 | 1 and 6 | Ken Burns, slow push in |
| B3 | 5, and short segment 4 | Ken Burns, slow drift, cool grade |
| B6 | 7 and 15 (dimmed) | Ken Burns, warm |
| A16 | 12 (SA corner) and 17 (Close) | Slow push in; push out and fade on the close |

If a new still is genuinely needed:

```
POST https://platform.higgsfield.ai/v1/text2image/soul
Header: hf-api-key: ${HF_API_KEY}
Body:  width_and_height: "2048x1152"   (or "1152x2048" for vertical)
       quality: "1080p"
       enhance_prompt: true
```

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
| K1 | 3 - Llama Windows, and short segment 2 | A laptop on a desk at night, screen glowing softly, a small light pulsing near the bottom edge of the screen. No readable UI, no logos, no people. |
| K2 | 4 - Indra OCR, and short segment 3 | Blank paper pages fanning out across a desk under warm light, faint abstract lines of text forming on them. No readable text, no ID documents. |
| K3 | 8 - Fish Audio Drama 3 | An abstract waveform changing colour and shape in a dark studio, amber edge light. No microphones with brand marks, no people. |

Negative direction on all three: no text, no watermarks, no logos, no identifiable faces, no fast camera whips.

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: the last two lines of segments 3, 4 and 7; "From 1 Dec: price doubles" in segment 5; "SA languages: not mentioned" in segment 8; the last line of segment 10; "US + Canada", "1 TB of RAM" and "US universities only" in segment 11; "stolen laptop = breach" in segment 13; "ended 12 Oct" in segment 14.
- **Segment 1:** a generic laptop with a cloud icon fading out above it. No Microsoft, Hugging Face or Google marks. Built in Shotstack, not Kling.
- **Segment 4:** generic blank document pages only. No real IDs, passports or readable personal data, even fake ones.
- **Segment 13:** a plain diagram with drawn lines and ASCII labels only. No arrow glyphs.
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

**Protected strings.** `isiZulu` and `isiXhosa` keep their lowercase prefixes - correct orthography, not typos. `llama.cpp` keeps its lowercase spelling and dot. `isiZulu` and `isiXhosa` keep their lowercase prefixes.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 12:37 to 13:02. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:01, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

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

1. **Confirm Michael has chosen to continue the series.** If not, stop here.
2. Read `script.md` and `social.md` fully before touching an API.
3. **Check the date** against the section 0 table and edit any expired lines before rendering.
4. Run `ascii_fix.py` across all four files. Confirm four `OK` lines and that the protected strings in section 7 survived.
5. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 19 October.** Generate once and commit.
6. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
7. Listen to segments 3, 4, 7 and 12 first for names. Re-render individual segments as needed.
8. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters from rendered audio.**
9. Render the three Kling clips to stage and inspect each.
10. Build and submit the Shotstack **stage** payload for A, then B.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then section 11.

---

## 10. Cost breakdown

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 14,000 characters across both deliverables | $1.25 - $1.80 |
| Higgsfield Soul stills | 5 new (cache absent), 0 thereafter | $0.00 - $1.50 |
| Higgsfield Kling clips | 3 clips at 5 seconds | $1.95 - $2.70 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 11 stage total** | | **$3.20 - $7.00** |

At R16.47 that is roughly **R53 to R115**.

**Eleven-episode combined stage cost, if all eleven are rendered: approximately $83.80 to $139.25, or about R1,380 to R2,293 at R16.47.** Production renders are additional, typically two to three times stage cost.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] `isiZulu`, `isiXhosa` and `llama.cpp` render correctly on screen
- [ ] No Hugging Face, Microsoft, Google, OpenAI, xAI, Fish Audio, ElevenLabs or Meta logos in any generated footage
- [ ] No real or realistic ID documents in segment 4 or short segment 3
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] Short is at least 60 seconds as rendered (see section 1)
- [ ] YouTube chapters rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] Time-limited lines correct for the publication date (section 0)
- [ ] `[LINK]` placeholder replaced, broadcast re-counted, still under 700 characters (currently 403 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **Restricted launches come back.** Gemini 4 Argon moved from "not for us yet" to the main list within two weeks. Keep the separate section.
- **Local AI got its own segment.** Two tools ran entirely on-device, so segment 13 explains what that does and does not change under POPIA rather than overselling privacy.
- **Vendor claims labelled.** Indra's 49 pages per second is shown as a vendor claim on screen.
- **Reshared old news again.** Canva AI 2.0 (April) appeared as new for the second week running.
- **The unrendered backlog is now eleven episodes, five need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 11
week_of: 2026-10-19
window_covered: 2026-10-12 to 2026-10-19
tools_covered: 8
top_pick: Llama Windows
second_pick: Indra OCR
action_item: Google AI Pro subscribers check the Gemini app for Gemini 4 Argon
not_available_in_sa: Meta Muse Wonder (countries not stated), Muse Spark Open (1 TB RAM), OpenAI Rosalind Academic Plan (US only)
sa_story: ORT SA Funda Nam (English, isiZulu, isiXhosa); Vodacom and UJ hackathon
content_expiry_date: 2026-10-28
content_expiry_reason: AI Expo Africa referred to as upcoming
secondary_expiry_date: 2026-11-12
secondary_expiry_reason: Fish Audio Drama 3 launch price ends
tertiary_expiry_date: 2026-11-30
tertiary_expiry_reason: Gemini 4 Argon introductory API price ends
fx_rate_used: 16.47
fx_rate_date: 2026-10-19
fx_sources: 3
long_form_runtime_estimate: "14:00"
long_form_words: 2232
long_form_segments: 17
short_runtime_estimate: "1:01"
short_words: 162
short_segments: 5
whatsapp_broadcast_chars: 403
kling_clips: 3
soul_stills_new: 5 (cache absent in repo)
stage_cost_estimate_usd: "3.20 - 7.00"
stage_cost_estimate_zar: "53 - 115"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
series_decision_pending: true
backlog_episodes_unrendered: 11
backlog_episodes_needing_edits: 5 (episodes 6 to 10)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 10, which remain in force.

```
Llama Windows, Indra OCR, Gemini 4 Argon, ChatGPT Slides, GPT-6 Pro update,
GPT-Live-1.1, Grok Voice 3.0, Fish Audio Drama 3, ElevenLabs Instant Soundtracks,
Microsoft Copilot for legal, Meta Muse Wonder, Muse Spark Open,
OpenAI Rosalind Academic Plan, Funda Nam, Vodacom UJ AI hackathon,
Canva AI 2.0, Shopify agent checkout, Microsoft-Decision-1, Mistral Large 4,
Claude Code Review
```

Exceptions: re-cover Muse Wonder if Meta confirms availability in South Africa; re-cover Gemini agent when small businesses can sign up with a price; cover AI Expo Africa outcomes after 29 October if a usable tool is announced there.

### Carried forward for future episodes

- **Meta smart glasses in South Africa.** Cover when a date and a rand price are official.
- **WhatsApp South African rate.** Find Meta's official South Africa rate card for service messages.
- **Exten AI.** Cover when it opens publicly with pricing.
- **Vambo AI MORENA.** Re-cover if a hosted API price is published.

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
