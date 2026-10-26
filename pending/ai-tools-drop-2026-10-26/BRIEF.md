# Production Brief - AI Tools Drop, Week of 26 October 2026

**Episode 12.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 13:25 (measured, 2,137 narration words at 160 wpm)
- Short runtime target: 1:06 (measured, 177 narration words)
- **16 segments this week, not 17.** Seven tools made the main list. Do not add a placeholder segment.

---

## 0. Read this before you spend anything

**Backlog warning. This is the twelfth unrendered episode in `pending/`.**

Checked on 26 October: `pending/` holds eleven earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 26 Oct | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 12 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 11 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 10 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 8 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 7 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 6 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 5 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 4 weeks | Not rendered. **1 October wording is stale.** |
| `ai-tools-drop-2026-10-05` | 5 October | 3 weeks | Not rendered. **Content expired 12 October.** |
| `ai-tools-drop-2026-10-12` | 12 October | 2 weeks | Not rendered. **Eleven v4 line expired 13 October.** |
| `ai-tools-drop-2026-10-19` | 19 October | 1 week | Not rendered. **AI Expo Africa "upcoming" line expires 28 October.** |
| `ai-tools-drop-2026-10-26` | 26 October | Current | This brief |

Six earlier episodes (6 to 11) need content edits before they could be published, or will by 28 October. Michael has been asked whether to keep the series running, pause it or stop it. **No answer yet. Do not render any episode, including this one, without his written choice.**

**Time-limited items in this episode. This episode dates fast.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| CAPES webinar, "tomorrow, Tuesday" | **27 October 2026** | Segment 11 narration says "tomorrow". Any render after 26 October needs that line rewritten. |
| AI Expo Africa, "Wednesday and Thursday" | **28 and 29 October 2026** | Segment 11 and the YouTube description refer to it as upcoming. |
| Meta AI Academy pitch finals, "on Friday" | **30 October 2026** | Segment 11 refers to Friday. |
| Gemini 4 Argon introductory API price | **30 November 2026** | Segment 13. |
| Meta AI Academy masterclass enrolment | **January 2027** | Segment 11, short and WhatsApp post. |

In practice, segment 11 is only correct if published on 26 October. If this episode is rendered later, rewrite segment 11's dates first.

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**Editorial note.** Segments 6 and 7 cover ElevenLabs and Mistral voice products, and segment 13 mentions Kling 4.0, which is newer than the Kling v2.1 endpoint this brief uses. That is editorial content, not a pipeline instruction. **Do not switch voice vendors, video models or settings for this episode.** Any change is Michael's decision.

**Self-disclosure note.** Segment 5 covers Perplexity Computer, which is the tool that researches and writes this series. The narration and overlay disclose that. Do not cut the disclosure line from segment 5 for time.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 13:25 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:06 | TikTok, Instagram Reels, YouTube Shorts |

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

**Render one API call per segment.** Sixteen calls for deliverable A, five for deliverable B. Do not batch.

Name the files `seg01.mp3` through `seg16.mp3` for A and `short01.mp3` through `short05.mp3` for B, in an `audio/` subdirectory.

**Voice direction.** Warm, measured, South African English. Conversational, not presenter-bright. No hype, no rising sales cadence. Slight slowdown on every caveat line ("Here is the honest part", "Two catches", "I could not confirm"). Those lines are the series' credibility and must not be rushed.

**Pronunciation guide is in the script header.** This week's high-risk tokens: `Voxtral` (VOKS-trahl), `Qwen` (chwen), `Klaviyo` (KLAY-vee-oh), `Claude Duet` (klohd dyoo-ET), `1Password` (one PASS-wurd), `DCDT` (spelled out), `CAPES` (kayps), `Afrikaans` (af-ri-KAHNS), and the language names `isiZulu` and `isiXhosa`. Listen to segments 4, 7, 10 and 11 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

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

**Twelfth brief asking for this cache. Checked on 26 October: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 10 and 13 (dimmed) | Slow push in |
| B2 | 2 and 5 | Ken Burns, slow push in; cool grade on 5 |
| B3 | 7 | Ken Burns, slow drift, cool grade |
| B6 | 14 (dimmed) | Ken Burns, warm |
| A16 | 11 (SA corner), 16 (Close), short segment 5 | Slow push in; push out and fade on the close |

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
| K1 | 3 - Canva Craft, and short segment 2 | Blank poster sheets on a studio table, abstract colour blocks arranging themselves into a layout. No readable text, no logos, no people. |
| K2 | 6 - ElevenLabs Realtime, and short segment 4 | An abstract waveform pulsing in a dark room, a generic desk phone silhouette at the frame edge, amber edge light. No brand marks, no people. |
| K3 | 9 - Octane AI Phoenix | Unbranded hair and skincare bottles on a bright bathroom shelf, soft morning light, slow camera slide. No labels, no faces. |

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: "US only" in segment 2; the last line of segment 3; the "Not included" line in segment 4; "36 GB memory" in segment 5; "not named" in segment 6; "not published" in segment 7; the last two lines of segment 8; the POPIA line in segment 9; "US Pro + Max only", "No business accounts" and "Enterprise alpha" in segment 10; "Tell callers it is an AI" in segment 12; "outside window" and "ends 30 Nov" in segment 13; "Not for isiZulu or isiXhosa yet" in segment 16.
- **Segment 1:** a generic poster layout assembling, with a price block reading "R250". No Canva marks. Built in Shotstack, not Kling.
- **Segment 4 and short segment 3:** two generic video-call tiles with abstract speech bubbles. No Google UI, no faces.
- **Segment 5:** the disclosure line "Disclosure: this series uses Perplexity" holds for the full segment.
- **Segment 8:** generic code-shaped colour blocks on a laptop outline. No readable code.
- **Segment 12:** a plain bar chart with ASCII labels only, labelled "ROUGH EXAMPLE (MY MATHS)", and two bins labelled AI and HUMAN. No arrow glyphs.
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

**Protected strings.** `isiZulu` and `isiXhosa` keep their lowercase prefixes - correct orthography, not typos. `1Password` keeps its leading digit. `shop.md` keeps its lowercase spelling and dot.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 15, from 12:01 to 12:26. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:06, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

Card text for deliverable A, exactly:

```
AI DISCLOSURE
Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**Minimum five seconds on screen. Never cut for runtime.** If the episode runs long, trim segment 14 first, then 13, then 12.

**Platform declaration is separate and additional.** At upload, set the AI-generated content toggle on YouTube, TikTok, Instagram and Facebook. Both the on-video card and the platform toggle are required.

---

## 9. Execution flow for Claude Code

1. **Confirm Michael has chosen to continue the series.** If not, stop here.
2. Read `script.md` and `social.md` fully before touching an API.
3. **Check the date** against the section 0 table. If it is after 26 October, rewrite segment 11's day references before rendering.
4. Run `ascii_fix.py` across all four files. Confirm four `OK` lines and that the protected strings in section 7 survived.
5. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 26 October.** Generate once and commit.
6. Render narration: 16 ElevenLabs calls for A, 5 for B, into `audio/`.
7. Listen to segments 4, 7, 10 and 11 first for names. Re-render individual segments as needed.
8. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters from rendered audio.**
9. Render the three Kling clips to stage and inspect each.
10. Build and submit the Shotstack **stage** payload for A, then B.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then section 11.

---

## 10. Cost breakdown

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 13,500 characters across both deliverables | $1.25 - $1.80 |
| Higgsfield Soul stills | 5 new (cache absent), 0 thereafter | $0.00 - $1.50 |
| Higgsfield Kling clips | 3 clips at 5 seconds | $1.95 - $2.70 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 12 stage total** | | **$3.20 - $7.00** |

At R16.57 that is roughly **R53 to R116**.

**Twelve-episode combined stage cost, if all twelve are rendered: approximately $87.00 to $146.25, or about R1,442 to R2,423 at R16.57.** Production renders are additional, typically two to three times stage cost.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] Segment 5 Perplexity disclosure line visible for the full segment
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] `isiZulu`, `isiXhosa` and `1Password` render correctly on screen
- [ ] No Canva, Google, Perplexity, ElevenLabs, Mistral, Shopify, Anthropic, 1Password or Meta logos in any generated footage
- [ ] No readable UI or faces in segments 4 and 5
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] Short is at least 60 seconds as rendered
- [ ] YouTube chapters rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] Segment 11 day references correct for the publication date (section 0)
- [ ] `[LINK]` placeholder replaced, broadcast re-counted, still under 700 characters (currently 411 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **Seven, not eight.** Several big launches (Kling 4.0, DeepSeek V4.1 Flash) fell outside the window, and the biggest one inside it (Claude Duet) is US only. The list was not padded.
- **Language checks matter.** Google Meet's 63 languages include Afrikaans but not isiZulu, isiXhosa, Sesotho or Setswana. This was confirmed from Google's own list and is said plainly in narration.
- **Self-disclosure.** Perplexity Computer was covered with an on-screen and spoken disclosure, because it is the tool producing this series.
- **Free-tier claims conflict.** Third-party guides misstate Canva's free Dream Lab allowance. The script uses Canva's own help page (20 lifetime uses on Free).
- **The unrendered backlog is now twelve episodes, six need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 12
week_of: 2026-10-26
window_covered: 2026-10-19 to 2026-10-26
tools_covered: 7
top_pick: Canva Craft
second_pick: Google Meet speech translation
action_item: Test Meet speech translation in Afrikaans before client use; enrol in Meta AI Academy SA masterclass
not_available_in_sa: Claude Duet (US waitlist), 1Password for Agents (Muse only), Eleven Realtime Translation (enterprise alpha)
sa_story: Meta and DCDT AI Academy South Africa; CAPES AI Action Plan webinar; AI Expo Africa
content_expiry_date: 2026-10-27
content_expiry_reason: Segment 11 says the CAPES webinar is tomorrow
secondary_expiry_date: 2026-10-28
secondary_expiry_reason: AI Expo Africa referred to as upcoming
tertiary_expiry_date: 2026-11-30
tertiary_expiry_reason: Gemini 4 Argon introductory API price ends
fx_rate_used: 16.57
fx_rate_date: 2026-10-26
fx_sources: 3
long_form_runtime_estimate: "13:25"
long_form_words: 2137
long_form_segments: 16
short_runtime_estimate: "1:06"
short_words: 177
short_segments: 5
whatsapp_broadcast_chars: 411
kling_clips: 3
soul_stills_new: 5 (cache absent in repo)
stage_cost_estimate_usd: "3.20 - 7.00"
stage_cost_estimate_zar: "53 - 116"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
series_decision_pending: true
backlog_episodes_unrendered: 12
backlog_episodes_needing_edits: 6 (episodes 6 to 11)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 11, which remain in force.

```
Canva Craft, Google Meet speech translation (63 languages), Perplexity Computer
local on Mac, Eleven Realtime v1 Mini and Max, Mistral Voxtral 3, Recursive Flint,
Octane AI Phoenix, Claude Duet, 1Password for Agents, Eleven Realtime Translation,
Meta AI Academy South Africa, CAPES AI Action Plan, Kling 4.0, OpenAI Decisions API GA,
Shopify shop.md and shop.dev, DeepSeek V4.1 Flash, Mercury 3, MiniMax M3.1 Flash,
FLUX 3 Max
```

Exceptions: re-cover Claude Duet or 1Password for Agents if either opens to South Africa or to business accounts; cover the Meta AI Academy pitch winners if announced; cover AI Expo Africa outcomes after 29 October if a usable tool is announced there; re-cover Shopify shop.md if region availability is confirmed.

### Carried forward for future episodes

- **Meta Muse Wonder.** Re-cover if Meta confirms availability in South Africa.
- **Gemini agent.** Re-cover when small businesses can sign up with a price.
- **Vambo AI MORENA.** Re-cover if a hosted API price is published.
- **WhatsApp South African rate.** Find Meta's official South Africa rate card for service messages.

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
