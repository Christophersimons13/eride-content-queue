# Production Brief - AI Tools Drop, Week of 28 September 2026

**Episode 8.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 15:05 (measured, 2,414 narration words at 160 wpm)
- Short runtime target: 1:10 (measured, 187 narration words)

---

## 0. Read this before you spend anything

**Backlog warning. This is the eighth unrendered episode in `pending/`.**

Checked on 28 September: `pending/` holds seven AI Tools Drop directories, nothing has moved to `in-progress/`, `approved/` or `published/`, and `assets/ai-tools-drop/` does not exist in the repository.

| Directory | Week | Age at 28 Sept | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 8 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 7 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 6 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 4 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 3 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 2 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 1 week | Not rendered. **Content expires 29 September - tomorrow.** |
| `ai-tools-drop-2026-09-28` | 28 September | Current | This brief |

Episodes 3 to 7 each carried an escalation asking for a direction on the backlog. None was answered.

**Episode 7 expires tomorrow.** Its short opens on the 29 September StackBlitz opt-out and its long-form segment 5 is built around it. From 29 September it opens on dead advice. Its secondary date, the Bolt Forge preview ending 14 October, follows two weeks later. After tomorrow, six of the eight queued episodes are unpublishable as weekly news without editing.

**This episode carries four time-limited items.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Microsoft 5% CSP uplift on annual-term subscriptions billed monthly | **1 October 2026** | Short segment 3 and long-form segment 4 say "from the first of October". After that date, change to "since" or cut the line. Three days out from this brief. |
| Copilot Business usage-based billing default | **2 November 2026** | Segment 4, segment 17 and short segment 3 are built on it as a future date. |
| Gemini TTS promotional pricing | **31 December 2026** | All per-minute rand figures double from 1 January 2027. |
| Copilot Business first-year promo | **31 December 2026** | The $18 figure in segment 4 lapses. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**One note on this episode's top pick, so nobody acts on it by accident.** Segment 3 covers Gemini 3.8 Flash TTS, a text-to-speech model that competes with the ElevenLabs step in this pipeline. That is editorial content, not a pipeline instruction. **Do not switch voice providers or generate test clips in South African languages for this episode.** Any pipeline change is Michael's decision.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 15:05 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:10 | TikTok, Instagram Reels, YouTube Shorts |

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

**Pronunciation guide is in the script header.** This week's high-risk tokens are the South African language names: `isiZulu` (ee-see-ZOO-loo), `isiXhosa` (ee-see-KOH-sah), `siSwati` (see-SWAH-tee), `Sepedi` (seh-PEH-dee), `Sesotho` (seh-SOO-too), `Setswana` (seh-TSWAH-nah), `Xitsonga` (shee-TSONG-gah), `Tshivenda` (chee-VEN-dah) and `isiNdebele` (ee-see-n-deh-BEH-leh). Also `ZakaChat` (ZAH-kah-chat), `Hemory` (HEM-oh-ree), `Lelapa` (leh-LAH-pah), `Vulavula` (voo-lah-VOO-lah), `POPIA` (poh-PEE-uh) and `FAIS` (fayce).

**Segment 1 and segment 3 are the highest risk in the series so far.** They list our languages by name, to a South African audience, in a segment praising a model for naming them. A mangled isiXhosa in that context is worse than in any other episode. Listen to segments 1, 3 and 14 first. If the voice cannot render a name acceptably after two attempts, use the respelling from the pronunciation guide in the narration text for that segment only, and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Five clips, named in the script's B-ROLL notes this time (K1 to K5), as episode 7's series note asked.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime. Every pricing table, bar chart, date card and checklist is built here.

Rough split by runtime: Kling about 25 seconds, Soul stills about 2 minutes, Shotstack the remaining 12-plus minutes.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`:

- `B1` - abstract data-flow field, dark, amber accents
- `B2` - desk workspace, low light, screens
- `B3` - abstract network mesh
- `B6` - dusk cityscape, warm (used this week as warehouse-adjacent context in segment 7; if it reads wrong, fall back to a Shotstack card)
- `A16` - Johannesburg skyline

**This is the eighth brief asking for this cache, and it was checked this time: `assets/ai-tools-drop/` does not exist in the repository on 28 September.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

Assignments this episode:

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 1 (Cold open) and 14 (low opacity) | Slow push in |
| B2 | 4 (Microsoft) and 9 (Financial Cents, different crop) | Ken Burns, slow push in |
| B3 | 5 (GPT-6), short segment 4 | Ken Burns, slow drift left, cool grade |
| B6 | 7 (Amazon) | Ken Burns, warm |
| A16 | 11 (RelativityOne) and 17 (Close) | Slow push in; push out and fade on the close |

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
| K1 | 3 - Gemini TTS | An abstract animated waveform over a Johannesburg street at dusk, soft bokeh, warm light. No text, no people in focus. |
| K2 | 6 - Claude Opus 5.5 | A stack of blank paper documents slowly unfolding and fanning out on a dark desk. Abstract, no readable text. |
| K3 | 8 - ZakaChat | A phone held in a hand on a taxi rank bench in daylight, screen showing only generic blank chat bubbles. No logos, no readable text, face out of frame. |
| K4 | 10 - Hemory | Close-up of a smartwatch on a wrist, soft concentric sound-wave rings expanding outward. Calm, no text. |
| K5 | 12 - Claude plugin portal | Abstract puzzle pieces sliding together in slow motion against a dark background, amber edge light. |

Negative direction on all five: no text, no watermarks, no logos, no identifiable faces, no fast camera whips.

**K3 is the one most likely to fail.** Kling tends to put a recognisable messaging-app interface or a readable brand on phone screens. The brief is generic bubbles only. If it comes back with a WhatsApp logo or readable UI, replace K3 with a Shotstack-built chat-bubble animation rather than re-rolling twice. Old Mutual's and WhatsApp's marks must not appear.

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: the free-tier data line and the NOT LISTED column in segment 3; both date cards in segment 4; every NOT STATED / NOT CONFIRMED / NOT PUBLISHED line in segments 5, 7, 8, 10 and 12; "No SARS-specific support stated" in segment 9; "NOT NEW" in segment 11; "New African regions announced: 0" in segment 14; the CORRECTION header in segment 15.
- **Segment 1:** the six language names appear one at a time, about 0.5 seconds apart, white, centred. No other text until all six are on screen.
- **Segment 3:** split card. LISTED column in accent, NOT LISTED column in warning, side by side, equal weight. Do not make the listed column larger - the point is the gap as much as the list.
- **Segment 13:** four horizontal bars for output price per million tokens: Grok 4.7 $6, GPT-6 Sol $10, GPT-6 Luna $0.50, Opus 5.5 $20. Bars to scale. Luna's bar will be very short; that is the point.
- **Segment 14:** counters tick from 0 to 1 twice, in accent. The third line stays at 0 in warning.
- **Segment 15:** the CORRECTION block holds two full seconds before the filter list starts. It is a correction of our own prior claim and must be visible, not rushed.
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

**Two strings in this episode are quoted vendor copy and must survive verbatim.** In segment 8, `"not intended to replace personalised financial advice"`. In segment 3, the language names as written: `isiZulu`, `isiXhosa`, `siSwati` - the lowercase prefixes are correct orthography, not typos. Do not "fix" the capitalisation.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 13:33 to 14:02. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:10, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

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
2. **Check the date.** If it is on or after 1 October 2026, edit short segment 3 and long-form segment 4 ("from the first of October" to "since the first of October") before rendering. If it is on or after 2 November 2026, stop and report.
3. Run `ascii_fix.py` across all four files. Confirm four `OK` lines. Confirm the two protected strings in section 7 survived intact.
4. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 28 September.** Generate once and commit.
5. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
6. Listen to segments 1, 3 and 14 first for the language names, then 8 and 10. Re-render individual segments as needed.
7. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters in `social.md` section 3 from rendered audio**, not the 160 wpm estimate.
8. Render the five Kling clips to stage. Inspect each; K3 against the no-logo brief specifically.
9. Build the Shotstack stage payload for deliverable A against the real audio durations.
10. Submit deliverable A to the **stage** endpoint. Download and inspect end to end.
11. Repeat 9 and 10 for deliverable B, including the persistent disclosure caption.
12. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
13. On approval: production render, then section 11.

Do not proceed past step 12 without approval, and do not batch steps 1 to 12 across all eight queued episodes before reporting.

---

## 10. Cost breakdown

Stage-pass estimate for this episode only:

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 15,000 characters across both deliverables | $1.35 - $1.90 |
| Higgsfield Soul stills | 5 new (cache absent), 0 thereafter | $0.00 - $1.50 |
| Higgsfield Kling clips | 5 clips at 5 seconds | $3.25 - $4.50 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 8 stage total** | | **$4.60 - $8.90** |

At R16.43 that is roughly **R76 to R146**.

Prior episodes: episode 1 $18-28, episode 2 $16.35-24.65, episode 3 $13.44-19.68, episode 4 $5.85-7.38, episode 5 $4.65-8.90, episode 6 $4.60-8.85, episode 7 $4.65-8.95. Four episodes now sit in the same band.

**Eight-episode combined stage cost, if all eight are rendered: approximately $72.10 to $115.40, or about R1,185 to R1,896 at R16.43.** Production renders are additional, typically two to three times stage cost, which puts the full eight-episode production run at roughly R3,550 to R7,600 all in.

Three of those eight episodes (6, 7 and, after 1 October, parts of 8) need content edits before they can be published.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] `isiZulu`, `isiXhosa` and `siSwati` render with correct lowercase prefixes on screen
- [ ] Every South African language name reads acceptably on playback in segments 1, 3, 14 and short segment 2
- [ ] No WhatsApp, Old Mutual, Google, Microsoft, OpenAI, Anthropic or Amazon logos in any generated footage
- [ ] No generated South African language audio samples anywhere in either video
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] Segment 15's CORRECTION block holds two full seconds
- [ ] YouTube chapters in `social.md` rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] NOT VERIFIED rows in `social.md` section 8 appear nowhere as positive statements - especially Seller Assistant on amazon.co.za, any ZakaChat phone number, and the quality of isiZulu or isiXhosa output
- [ ] **1 October wording** correct for the publication date (see section 9 step 2)
- [ ] 2 November still in the future on the publication date
- [ ] `[LINK]` placeholder in the WhatsApp broadcast replaced with the real video URL
- [ ] WhatsApp broadcast re-counted after the link is inserted, still under 700 characters (currently 626 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

Carry these forward.

- **Writing lean worked.** Episode 7 came in at 18:58 and needed three passes. Episode 8 was written at the 145 to 155 words per tool budget and measured 15:05 on the first pass, with no trim needed. Keep the budget.
- **Platform weeks need a label.** Three entries this week are platform changes (GPT-6, Opus 5.5, the Claude plugin portal), and the script says so on air and in the overlays. When the frontier labs dominate a week, say it rather than dressing model releases as tools.
- **Correct prior episodes on air.** Episode 7 said Lelapa's release notes showed nothing between 14 and 21 September. An entry dated 16 September now appears. Segment 15 corrects it. Do the same whenever a previous claim turns out wrong.
- **Check the repository, not just the brief.** This is the first brief that looked: `assets/ai-tools-drop/` does not exist. Eight briefs had asked.
- **Uncertainty is content, not a defect.** A language list with no quality test, an agent with no confirmed South African marketplace, a hosting region that is real but three years old. Render those honestly.
- **Time-limited items go at the top of the brief.** This episode's first date is three days out.
- **The unrendered backlog is now eight episodes, one has expired and another expires tomorrow.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 8
week_of: 2026-09-28
window_covered: 2026-09-21 to 2026-09-28
tools_covered: 10
platform_changes_among_them: 3 (GPT-6 Sol and Luna, Claude Opus 5.5, Claude plugin portal)
top_pick: Gemini 3.8 Flash TTS
second_pick: GPT-6 Luna
action_item: Microsoft 365 CSP uplift 1 Oct 2026 and Copilot Business usage billing default 2 Nov 2026
biggest_story: First voice model in the series to publish South African languages (Afrikaans, isiZulu, isiXhosa, siSwati, Sepedi, Sesotho)
sa_languages_not_listed: Setswana, Xitsonga, Tshivenda, isiNdebele
sa_launch: Old Mutual ZakaChat (second SA launch in the series after KUMii)
warning_item: Hemory (always-on recording of other people; hosting, training and pricing unstated)
popia_vendor_references: 1 (Relativity press release, 23 Sep - first in 8 weeks)
sa_hosting_region_documented: RelativityOne South Africa (North), zano - dates to 2023, not new
new_african_regions_announced: 0
correction_issued: Lelapa Vulavula release dated 16 Sep 2026, contradicting episode 7
content_expiry_date: 2026-10-01
content_expiry_reason: Microsoft CSP uplift wording shifts from future to past tense
secondary_expiry_date: 2026-11-02
secondary_expiry_reason: Copilot Business usage-billing default takes effect
promo_expiry_date: 2026-12-31 (Gemini TTS pricing doubles, Copilot Business promo ends)
fx_rate_used: 16.43
fx_rate_date: 2026-09-28
fx_source_spread_pct: 0.25
fx_sources: 3
long_form_runtime_estimate: "15:05"
long_form_words: 2414
long_form_segments: 17
short_runtime_estimate: "1:10"
short_words: 187
short_segments: 5
kling_clips: 5
soul_stills_new: 5 (cache absent in repo)
soul_stills_reused: 0 until the cache is committed
stage_cost_estimate_usd: "4.60 - 8.90"
stage_cost_estimate_zar: "76 - 146"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
backlog_episodes_unrendered: 8
backlog_episodes_content_expired: 1 (episode 6), episode 7 expires 2026-09-29
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5, 6 and 7, which remain in force.

```
Gemini 3.8 Flash TTS, Gemini 3.8 Flash-Lite TTS, Microsoft Copilot Home,
Copilot Code, Copilot Autopilot, GPT-6 Sol, GPT-6 Luna, Claude Opus 5.5,
Claude plugin directory portal, Amazon Seller Assistant workflows,
Amazon Selling Partner plugin, Old Mutual ZakaChat, Financial Cents AI agents,
Hemory, RelativityOne South Africa, Grok 4.7, Base44 Superagent calls,
Reinventing.AI AI Employees, Jev, Solid, IntellAgents.io, Floot, Clueso,
WZRD, PixVerse R2, Google Call for Me
```

### Carried forward for future episodes

- **Gemini TTS in South African languages, tested.** Nobody has published a quality test. A follow-up with first-language speakers rating isiZulu, isiXhosa and Afrikaans output would be the most locally useful segment the series could run. Needs Michael's go-ahead and consenting reviewers; do not generate samples for this episode.
- **Lelapa AI and Vulavula.** The 16 September release is a bug fix. Lelapa is now a named member of the Gates Foundation 60-organisation language coalition. The standalone out-of-window feature recommended in episode 7 is still the right format.
- **Microsoft 365 billing for SA SMBs.** If the 2 November default generates reseller confusion, a short explainer on setting Copilot spending caps would be timely in episode 12 or 13.
- **Amazon Seller Assistant on amazon.co.za.** Re-check weekly; if the workflows reach the SA marketplace, it becomes a full entry.
- **Undated South African tech press remains the largest research gap.** This week's SA launch came through Bizcommunity and Sunday World, both dated.

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
