# Production Brief - AI Tools Drop, Week of 12 October 2026

**Episode 10.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 14:32 (measured, 2,309 narration words at 160 wpm)
- Short runtime target: 1:06 (measured, 176 narration words)

---

## 0. Read this before you spend anything

**Backlog warning. This is the tenth unrendered episode in `pending/`.**

Checked on 12 October: `pending/` holds nine earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 12 Oct | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 10 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 9 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 8 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 6 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 5 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 4 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 3 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 2 weeks | Not rendered. **1 October wording is stale.** |
| `ai-tools-drop-2026-10-05` | 5 October | 1 week | Not rendered. **Content expires today, 12 October** (Eleven v4 discount ends): segments 2, 3 and 17, short segment 3, the WhatsApp broadcast and all captions need edits. |
| `ai-tools-drop-2026-10-12` | 12 October | Current | This brief |

Four earlier episodes (6, 7, 8 and 9) now need content edits before they could be published. Michael has been asked whether to keep the series running, pause it or stop it. **No answer yet. Do not render any episode, including this one, without his written choice.**

**Time-limited items in this episode.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Eleven v4 discount mentioned as "ends today" | **12 October 2026** | Segment 14 and the WhatsApp broadcast line "Last call" become wrong from 13 October. Cut them, or change to "has ended". |
| Spira Maxima launch-month 50 percent discount | About **6 November 2026** (one month from launch; exact end date not published) | Segment 9 and the article pricing line. Restate list price only after that. |
| Gemini agent general availability | Expected end October or early November | If it opens before publication, segment 11 is out of date. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 14:32 | YouTube, Facebook native, WhatsApp channel |
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

**Render one API call per segment.** Seventeen calls for deliverable A, five for deliverable B. Do not batch.

Name the files `seg01.mp3` through `seg17.mp3` for A and `short01.mp3` through `short05.mp3` for B, in an `audio/` subdirectory.

**Voice direction.** Warm, measured, South African English. Conversational, not presenter-bright. No hype, no rising sales cadence. Slight slowdown on every caveat line ("Here is the honest part", "Two catches", "I could not confirm"). Those lines are the series' credibility and must not be rushed.

**Pronunciation guide is in the script header.** This week's high-risk tokens: `Haiku` (HY-koo), `SynthID` (SINTH-eye-dee), `Spira Maxima` (SPEER-ah MAX-ih-mah), `Vambo` (VAHM-boh), `MORENA` (moh-REH-nah), `Kasicoach` (KAH-see-coach), and the language names `isiZulu`, `isiXhosa`, `Setswana`, `isiNdebele`. Listen to segments 5, 9, 10 and 12 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Four clips this week, K1 to K4.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images once they exist.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime.

Rough split by runtime: Kling about 20 seconds, Soul stills about 2 minutes, Shotstack the remainder.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`: `B1` (abstract data-flow field), `B2` (desk workspace, low light), `B3` (abstract network mesh), `B6` (dusk cityscape, warm), `A16` (Johannesburg skyline).

**Tenth brief asking for this cache. Checked on 12 October: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 1, 11 and 14 (dimmed) | Slow push in |
| B2 | 3 and 7 (dimmed) | Ken Burns, slow push in |
| B3 | 4 and 8 | Kling source, slow parallax |
| B6 | 5, 9 and 15 (dimmed) | Ken Burns, warm |
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
| K1 | 4 - GPT-6 for everyone, and short segment 3 | Abstract blank panels unfolding into simple chart shapes on a dark background. No text, no logos. |
| K2 | 6 - Google AI Edge Foresight, and short segment 4 | A closed laptop opening on a quiet desk at night, a soft amber glow, no screen content readable. No people. |
| K3 | 8 - Nano Banana 2.1 | A blank product box on a plinth while lighting and background shift around it. No labels, no text. |
| K4 | 10 - SynthID Detector | A thin amber scan line passing over an abstract photo-like panel. No readable content, no faces. |

Negative direction on all four: no text, no watermarks, no logos, no identifiable faces, no fast camera whips.

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: "released in September" in segment 2; "Over 100K: 5x price" in segment 5; the POPIA consent line in segment 6; "Data residency: US and Europe only" in segment 7; "Small text can still fail" in segment 8; "No language list published" in segment 9; the last two lines of segment 10; "Private beta" and "US and Canada only" in segment 11; "Test before client use" in segment 12; the tall bar in segment 13; "ends TODAY, 12 Oct" in segment 14.
- **Segment 1:** a generic spreadsheet grid fills and a small chart rises. No Google or Anthropic marks. Built in Shotstack, not Kling.
- **Segment 3:** generic three-pane mock (document, sheet, slide) with an approval card. No product logos or readable UI.
- **Segment 7:** message cards sort into three bins labelled BOOKING, COMPLAINT, HUMAN.
- **Segment 13:** a plain bar chart with ASCII labels only. Label it "ROUGH EXAMPLE (MY MATHS)" so it is never read as a vendor figure.
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

**Protected strings.** `isiZulu` and `isiXhosa` keep their lowercase prefixes - correct orthography, not typos. `"Ask before edits"` in segment 17 and the social captions is quoted product copy and keeps its quote marks.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 13:12 to 13:37. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:06, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

Card text for deliverable A, exactly:

```
AI DISCLOSURE
Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**Minimum five seconds on screen. Never cut for runtime.** If the episode runs long, trim segment 15 first, then 14, then 13.

**Platform declaration is separate and additional.** At upload, set the AI-generated content toggle on YouTube, TikTok, Instagram and Facebook.

---

## 9. Execution flow for Claude Code

1. **Confirm Michael has chosen to continue the series.** If not, stop here.
2. Read `script.md` and `social.md` fully before touching an API.
3. **Check the date.** From 13 October 2026, edit segment 14 and the WhatsApp "Last call" line as listed in section 0.
4. Run `ascii_fix.py` across all four files. Confirm four `OK` lines.
5. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 12 October.** Generate once and commit.
6. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
7. Listen to segments 5, 9, 10 and 12 first for names. Re-render individual segments as needed.
8. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters from rendered audio.**
9. Render the four Kling clips to stage and inspect each.
10. Build and submit the Shotstack **stage** payload for A, then B.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then section 11.

---

## 10. Cost breakdown

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 14,500 characters across both deliverables | $1.30 - $1.85 |
| Higgsfield Soul stills | 5 new (cache absent), 0 thereafter | $0.00 - $1.50 |
| Higgsfield Kling clips | 4 clips at 5 seconds | $2.60 - $3.60 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 10 stage total** | | **$3.90 - $7.95** |

At R16.55 that is roughly **R65 to R132**.

**Ten-episode combined stage cost, if all ten are rendered: approximately $80.60 to $132.25, or about R1,334 to R2,189 at R16.55.** Production renders are additional, typically two to three times stage cost.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] `isiZulu`, `isiXhosa` and `isiNdebele` render with correct lowercase prefixes on screen
- [ ] No OpenAI, Anthropic, Google, Meta, Spira or ElevenLabs logos in any generated footage
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] YouTube chapters rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] Segment 13 labelled as my own rough example, never as a vendor figure
- [ ] **12 October wording** correct for the publication date (section 9 step 3)
- [ ] `[LINK]` placeholder replaced, broadcast re-counted, still under 700 characters (currently 439 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **Release date beats press date.** Vambo AI's MORENA was widely reported on 7 October, but its model page says it was released on 18 September. It went in the SA corner with the real date stated on air, not in the main list.
- **Reshared old news was the trap this week.** Four "new" stories (WhatsApp agent tools, Canva, ChatGPT checkout, Framer agents) were older than seven days and are named on air as left out.
- **Follow-ups kept.** The Decisions API was re-covered only because its price was published, per last week's exception rule.
- **Eight items, not nine or ten.** The week did not support more without padding.
- **The unrendered backlog is now ten episodes, four need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 10
week_of: 2026-10-12
window_covered: 2026-10-05 to 2026-10-12
tools_covered: 8
top_pick: Claude for Google Workspace
second_pick: Google AI Edge Foresight
action_item: Check suspicious images with SynthID Detector; a clean result is not proof
not_available_in_sa: Gemini agent (private beta), Meta Muse (US and Canada)
sa_story: Vambo AI MORENA (released 18 Sep 2026, press 7 Oct)
content_expiry_date: 2026-10-12
content_expiry_reason: "Eleven v4 discount ends today" line in segment 14 and WhatsApp broadcast
secondary_expiry_date: about 2026-11-06
secondary_expiry_reason: Spira Maxima launch-month discount (exact end not published)
fx_rate_used: 16.55
fx_rate_date: 2026-10-12
fx_sources: 3
long_form_runtime_estimate: "14:32"
long_form_words: 2309
long_form_segments: 17
short_runtime_estimate: "1:06"
short_words: 176
short_segments: 5
whatsapp_broadcast_chars: 439
kling_clips: 4
soul_stills_new: 5 (cache absent in repo)
stage_cost_estimate_usd: "3.90 - 7.95"
stage_cost_estimate_zar: "65 - 132"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
series_decision_pending: true
backlog_episodes_unrendered: 10
backlog_episodes_needing_edits: 4 (episodes 6, 7, 8, 9)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 9, which remain in force.

```
Claude for Google Workspace, Claude Dashboards, Claude Motion, GPT-6 for everyone,
Intelligent UI, Claude Haiku 5.5, Google AI Edge Foresight, OpenAI Decisions API,
Nano Banana 2.1, Spira Maxima, SynthID Detector, Gemini agent, Meta Muse on iPad,
Vambo AI MORENA, Google for Startups Accelerator SA 2026 cohort,
WhatsApp Business Tools MCP server, Canva 2.0, ChatGPT Instant Checkout, Framer 3.0
```

Exceptions: re-cover Gemini agent when small businesses can sign up with a price; re-cover Muse when it is available in South Africa; re-cover MORENA if Vambo publishes a hosted API price.

### Carried forward for future episodes

- **Meta smart glasses in South Africa.** Cover when a date and a rand price are official.
- **WhatsApp South African rate.** Find Meta's official South Africa rate card for service messages.
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
