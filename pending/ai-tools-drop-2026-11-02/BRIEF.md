# Production Brief - AI Tools Drop, Week of 2 November 2026

**Episode 13.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 13:19 (measured, 2,122 narration words at 160 wpm)
- Short runtime target: 1:04 (measured, 172 narration words)
- 17 segments this week (eight tools).

---

## 0. Read this before you spend anything

**Backlog warning. This is the thirteenth unrendered episode in `pending/`.**

Checked on 2 November: `pending/` holds twelve earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 2 Nov | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 13 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 12 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 11 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 9 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 8 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 7 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 6 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 5 weeks | Not rendered. **1 October wording is stale.** |
| `ai-tools-drop-2026-10-05` | 5 October | 4 weeks | Not rendered. **Content expired 12 October.** |
| `ai-tools-drop-2026-10-12` | 12 October | 3 weeks | Not rendered. **Eleven v4 line expired 13 October.** |
| `ai-tools-drop-2026-10-19` | 19 October | 2 weeks | Not rendered. **AI Expo Africa "upcoming" line expired 28 October.** |
| `ai-tools-drop-2026-10-26` | 26 October | 1 week | Not rendered. **Segment 11 "tomorrow" and "Friday" lines expired 27 to 30 October.** |
| `ai-tools-drop-2026-11-02` | 2 November | Current | This brief |

Seven earlier episodes (6 to 12) now need content edits before they could be published. Michael has been asked whether to keep the series running, pause it or stop it. **No answer yet. Do not render any episode, including this one, without his written choice.**

**Time-limited items in this episode.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Meta AI Academy SA winners "not published yet" | Any day | Segment 12 and the article. Recheck before render; if winners are out, rewrite the line. |
| Gemini in Slides promotional limits | **1 December 2026** (at least) | Segment 4. After that, per-user limits apply. |
| Kling 4.0 launch discount on Higgsfield | No end date stated | Segment 14 says "launch discount". Recheck before render. |
| Empacer launch discount and trial terms | Unstated | Segment 8. Pricing may be published at any time. |
| Meta AI Academy masterclass enrolment | **January 2027** | Segment 12. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**Editorial note.** Segment 14 says Kling 4.0 is now on Higgsfield, which is the platform this pipeline uses. That is editorial content, not a pipeline instruction. **Keep the Kling v2.1 endpoint in section 5 for this episode.** Any model change is Michael's decision, and would need its own stage test and cost check.

**Self-disclosure note.** Segment 15 mentions Perplexity updates and says this series is made with Perplexity. Do not cut that sentence for time.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 13:19 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:04 | TikTok, Instagram Reels, YouTube Shorts |

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

**Pronunciation guide is in the script header.** This week's high-risk tokens: `Empacer` (em-PAY-ser), `SalesCloser` (SAYLZ-kloh-zer), `Higgsfield` (HIGZ-feeld), `LFM3` (el-ef-em-THREE), `SARS` (sahrz), `Gemini` (JEM-in-eye), and the figures `1.43 billion` and `4.8` in segment 12. Listen to segments 7, 8, 12 and 15 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Three clips this week, K1 to K3.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images once they exist.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime.

Rough split by runtime: Kling about 15 seconds, Soul stills about 2.5 minutes, Shotstack the remainder.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`: `B1` (abstract data-flow field), `B2` (desk workspace, low light), `B3` (abstract network mesh), `B6` (dusk cityscape, warm), `A16` (Johannesburg skyline).

**Thirteenth brief asking for this cache. Checked on 2 November: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 11 and 14 (dimmed) | Slow push in |
| B2 | 2, and 13 (dimmed) | Ken Burns, slow push in |
| B3 | 6, and short segment 4 | Ken Burns, slow drift, cool grade |
| B6 | 8, and 15 (dimmed) | Ken Burns, warm |
| A16 | 12 (SA corner), 17 (Close), short segment 5 | Slow push in; push out and fade on the close |

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
| K1 | 3 - Gemini app files, and short segment 3 | Blank pages and an empty grid of cells forming on a laptop screen in a dim office, soft glow. No readable text, no Google UI, no people. |
| K2 | 5 - Canva Brush | Blank menu boards on a cafe wall, abstract colour blocks shifting across them in sequence, warm light. No readable text, no logos, no people. |
| K3 | 10 - Shopify Fall Edition | Unbranded shopping bags and parcels on a packing table, soft daylight, slow camera slide. No logos, no labels, no faces. |

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: the last line of segment 2; the last two lines of segments 3, 5, 8 and 9; "English only" and "1 Dec" in segment 4; the last three lines of segment 7; "US or select countries" and "not mentioned" in segment 10; all three restriction lines in segment 11; "-8%" and "3.0" in segment 12; "still US waitlist" in segment 14; "CLICKED LESS" in short segment 1.
- **Segment 1 and short segment 2:** grey blocks standing in for a search results page, with a "SEEN" counter rising and a "CLICKED" counter falling. No Google marks. Built in Shotstack, not Kling.
- **Segment 7:** a generic chat thread in two colours with a "HANDED TO HUMAN" tag. **No WhatsApp logo, no WhatsApp green.**
- **Segment 9:** a generic spreadsheet grid with a "CHANGED BY" tag. No readable figures.
- **Segment 13:** a plain numbered list, ASCII only. No arrow glyphs.
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

**Protected strings.** `Fall '26` uses a straight ASCII apostrophe; confirm it was not converted to a curly quote. `+22%` and `-8%` keep their ASCII plus and hyphen-minus signs. `1-10` uses a hyphen, not an en dash.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 12:02 to 12:27. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:04, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

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
3. **Check the date** against the section 0 table, and recheck whether the Meta AI Academy SA winners have been announced. Edit before rendering.
4. Run `ascii_fix.py` across all four files. Confirm four `OK` lines and that the protected strings in section 7 survived.
5. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 2 November.** Generate once and commit.
6. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
7. Listen to segments 7, 8, 12 and 15 first for names and figures. Re-render individual segments as needed.
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
| **Episode 13 stage total** | | **$3.20 - $7.00** |

At R16.62 that is roughly **R53 to R116**.

**Thirteen-episode combined stage cost, if all thirteen are rendered: approximately $90.20 to $153.25, or about R1,499 to R2,547 at R16.62.** Production renders are additional, typically two to three times stage cost.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] `Fall '26`, `+22%`, `-8%` and `1-10` render correctly on screen
- [ ] No Google, Canva, Strawberry, SalesCloser, WhatsApp, Empacer, Microsoft, Shopify, OpenAI or Meta logos in any generated footage
- [ ] No WhatsApp green or logo in segment 7
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] Short is at least 60 seconds as rendered
- [ ] YouTube chapters rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] Meta AI Academy winners line still accurate (section 0)
- [ ] `[LINK]` placeholder replaced, broadcast re-counted, still under 700 characters (currently 411 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **A study led the episode.** The cold open, the analysis segment and the short are built around Algorithm's South African zero-click study, because it gives owners something to act on this week.
- **Price gaps stated plainly.** SalesCloser and Empacer publish no standard price. The script says so rather than guessing.
- **A reshared old story was caught.** A 2024 crop-drone story was republished on 30 October; it was rejected.
- **The pipeline's own vendor appeared in the news.** Kling 4.0 is on Higgsfield. It is reported as editorial only; the pipeline stays on v2.1.
- **The unrendered backlog is now thirteen episodes, seven need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 13
week_of: 2026-11-02
window_covered: 2026-10-26 to 2026-11-02
tools_covered: 8
top_pick: Gemini app file creation
second_pick: Strawberry 1.0 (free plan)
action_item: Check your Google Business Profile; try Gemini file creation on the web
not_available_in_sa: ChatGPT Dots by text (US Pro beta), Gemini 4 Carbon (cyber defenders only), Meta Style Sketch (Indonesia, Singapore, Thailand)
sa_story: Algorithm zero-click study of 110 SA websites; Meta AI Academy SA masterclass
content_expiry_date: 2026-12-01
content_expiry_reason: Gemini in Slides promotional limits end
secondary_expiry_reason: Meta AI Academy SA winners may be announced at any time
fx_rate_used: 16.62
fx_rate_date: 2026-11-02
fx_sources: 3
long_form_runtime_estimate: "13:19"
long_form_words: 2122
long_form_segments: 17
short_runtime_estimate: "1:04"
short_words: 172
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
backlog_episodes_unrendered: 13
backlog_episodes_needing_edits: 7 (episodes 6 to 12)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 12, which remain in force.

```
Gemini app file creation, Gemini in Google Slides whole-deck edits,
Fill with Gemini citations, Canva Brush, Strawberry 1.0, SalesCloser WhatsApp,
Empacer, Microsoft Copilot for finance, Shopify Fall '26 Edition,
ChatGPT Dots texting, Gemini 4 Carbon, Meta Style Sketch, Algorithm zero-click study,
Liquid AI LFM3, Genie 4, Perplexity Mac voice mode, Perplexity Deep Research skill,
Notion agents rebuild, Stripe Link balance for agents, Kling 4.0 on Higgsfield,
Mistral Large 4 open weights, Dell Moyo crop drone
```

Exceptions: re-cover Gemini 4 Carbon when businesses can get access; re-cover ChatGPT Dots texting if it reaches South Africa; re-cover SalesCloser or Empacer once a standard price is published; cover the Meta AI Academy SA pitch winners when announced.

### Carried forward for future episodes

- **Claude Duet and 1Password for Agents.** Re-cover if either opens to South Africa or to business accounts.
- **Meta Muse Wonder.** Re-cover if Meta confirms availability in South Africa.
- **Gemini agent.** Re-cover when small businesses can sign up with a price.
- **Shopify shop.md.** Re-cover if region availability is confirmed.

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
