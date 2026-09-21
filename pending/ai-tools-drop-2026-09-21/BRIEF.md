# Production Brief - AI Tools Drop, Week of 21 September 2026

**Episode 7.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 15:44 (measured, 2,518 narration words at 160 wpm)
- Short runtime target: 1:28 (measured, 236 narration words)

---

## 0. Read this before you spend anything

**Backlog warning. This is the seventh unrendered episode in `pending/`.**

Queued and not yet rendered:

| Directory | Week | Age at 21 Sept | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 7 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 6 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 5 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 3 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 2 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 1 week | Not rendered. **Content already expired.** |
| `ai-tools-drop-2026-09-21` | 21 September | Current | This brief |

Episodes 3, 4, 5 and 6 each carried an escalation asking for a direction on the backlog. None was answered.

**Episode 6 has now expired.** Its content deadline was 20 September 2026, the Typewise Nova launch gift. That date has passed. If episode 6 renders as written, segment 6, segment 15 and three of its five social cuts all state an offer that no longer exists. Episode 6 cannot be published without editing those segments first. This is the exact failure section 0 of that brief warned about, one week later.

Five of the seven queued episodes are now unpublishable as weekly news without editing.

**This episode carries three time-limited items. Two are hard deadlines.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Bolt.new / StackBlitz opt-out window | **29 September 2026** | The short opens on it and segment 5 of the long form is built around it. Past that date the video opens on dead advice. Cut short segment 1 and re-record long-form segment 5. |
| Bolt Forge research preview ends | **14 October 2026** | The pricing and 50X usage claim in segment 5 stops being true. |
| Higgsfield launch discount lock-in | approx **23 September 2026** (inferred, vendor never printed a date) | Lower stakes. It is already hedged in the narration as "roughly" and "though they never print a date". Leave the hedge in. |

The 29 September date is eight days out from this brief. If the stage-approval cycle takes longer than that, this episode needs the edit before it ships, not after.

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem. Seven episodes rendered blind is seven times the cost of one wrong decision.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 15:44 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:28 | TikTok, Instagram Reels, YouTube Shorts |

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

**Render one API call per segment.** Seventeen calls for deliverable A, five for deliverable B. Do not batch the full script into a single request - a single mispronunciation then costs one segment to redo, not the whole episode.

Name the files `seg01.mp3` through `seg17.mp3` for A and `short01.mp3` through `short05.mp3` for B, in an `audio/` subdirectory.

**Pronunciation guide is in the script header.** Read it before rendering. This week's high-risk tokens are `tiun` (TEE-oon), `KUMii` (koo-MEE), `Axari` (ax-AR-ee), `AiSDR` (ay-eye-ess-dee-AR), `Creem` (kreem), `n8n` (en-EIGHT-en), `WIOCC` (wee-OCK), `Tlakula` (tlah-KOO-lah), `Vulavula` (voo-lah-VOO-lah), `POPIA` (poh-PEE-uh), `Seedance` (SEED-ance) and `Kakao` (kah-KAH-oh).

`tiun` is the single highest-risk token in the episode. It is lowercase in the brand, it is four letters, and the model will try to read it as an English word. Listen to segment 8 first.

**Numbers are written longhand in the narration deliberately** so the model reads them correctly, and as digits in the overlay text. Do not reconcile the two. If you "fix" the narration to use digits, the voice model will read R16.25 as something unusable.

After rendering, listen to segments 5, 8, 10, 11 and 15 specifically. Segment 5 carries the longest quoted legal passage in the series so far and must land as measured speech, not as a rush. Segment 11 is four repeated ERROR beats and needs the rhythm intact.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers. The ratio is what keeps the cost down.

**Layer 1 - Kling motion clips, 5 seconds each.** Five clips this episode. Episode 4 used three and the stage render read as static through the middle third. Five is the established number. **The script's B-ROLL notes only name two Kling clips. This brief is authoritative on clip count** - section 5 lists all five and where they go.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images. Do not regenerate them.

**Layer 3 - Shotstack motion graphics.** This carries the bulk of the runtime and it is the cheapest layer. Every pricing table, comparison bar, checklist, error stack and figure card is built here from text and shapes, not generated.

Rough split by runtime: Kling about 25 seconds total, Soul stills about 2 minutes, Shotstack graphics the remaining 13-plus minutes.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** These live in `assets/ai-tools-drop/`:

- `B1` - abstract data-flow field, dark, amber accents
- `B2` - desk workspace, low light, screens
- `B3` - abstract network mesh
- `B6` - dusk cityscape, warm
- `A16` - Johannesburg skyline

**This is the seventh brief that has asked for this caching.** If the directory is empty or the files are missing, generate them once and commit them so the eighth brief does not have to ask again. Seven briefs asking the same question is a signal that nobody has checked the directory.

Assignments this episode:

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 1 (Cold open) | Slow push in |
| B2 | 6 (Higgsfield API) | Ken Burns, slow push in |
| B3 | 8 (tiun) | Ken Burns, slow drift left, cool grade |
| A16 | 10 (KUMii) | Slow Ken Burns push in |
| B6 | 14 (WIOCC beat only) | Ken Burns, warm |
| A16 | 17 (Close) | Slow push out, fade to black |

A16 is used twice, at segment 10 and again on the close. That is intentional - it bookends the only two South African beats in the episode.

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

**Note the irony and do not let it change the pipeline.** Segment 6 of this episode reports that Higgsfield's own policy reserves the right to train on inputs and outputs, with deletion as the only remedy. That applies to the stills this pipeline generates. It is a reason to protect the cache and generate as little as possible, which is already the instruction. It is not a reason to switch providers mid-series without a decision from Michael.

---

## 5. Higgsfield Kling - image to video

```
POST https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video
Header: Authorization: Key ${HF_API_KEY}:${HF_SECRET}
Duration: 5 seconds per clip
```

Five clips. K1 and K2 match the script's B-ROLL notes. K3, K4 and K5 are additions from this brief to hold the clip count at five.

| Clip | Segment | Prompt direction |
| --- | --- | --- |
| K1 | 3 - Creem 2.0 | Slow dolly across a payment terminal on a counter in a warm-lit South African retail interior. Late afternoon light. No text on the terminal screen, no people in frame. |
| K2 | 5 - Bolt Forge | Code scrolling on a dark monitor, rack focus pulling from foreground to screen. Abstract, no readable text. Cool grade. |
| K3 | 11 - Axari Twin | A dark, empty operations room, several monitors off, one faint reflection on glass. Static camera. No text, no status lights, no people. Deliberately vacant. |
| K4 | 15 - What did not launch | A slow pan across an empty noticeboard or bare wall in soft daylight. Nothing pinned to it. Quiet, plain, unhurried. |
| K5 | 17 - Close | Slow pull back from a city skyline at dusk, lights coming on across the buildings. Calm, resolved. |

Negative direction on all five: no text, no watermarks, no logos, no identifiable faces, no fast camera whips.

Render each to stage quality first and inspect. **K3 is the one most likely to come back as a stock security-operations-centre cliche with glowing blue screens and a hooded figure.** The brief is the opposite of that: an empty room. If Kling will not give you empty, replace K3 with a Shotstack-built abstract rather than re-rolling twice. Segment 11's power is in the four ERROR lines, not in the footage behind them.

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
- Any figure the script flags as uncertain gets the `warning` colour, not the accent. This episode that covers: **every Higgsfield rate figure** in segment 6, because the currency is unlabelled on the vendor's own page; the approx **23 September** Higgsfield lock-in date, because it is inferred; the tiun **SA onboarding** line in segment 8; and Axari's absent prices in segment 11.
- **Segment 5 is the episode. Three beats, and the third must not move.** Beat one is K2 over the offer. Beat two is the offer card in accent colour. Beat three is the opt-out block in `warning` on near-black, **static, no Ken Burns, no motion of any kind**. The line `SOUTH AFRICA IS NOT IN THE CARVE-OUT` gets three full seconds alone on screen.
- **Segment 11's four ERROR lines animate in one at a time, 0.5 seconds apart, each in `warning`, monospace.** Let the repetition do the work. The final line holds five seconds. No Kling under the stack itself - K3 sits under the opening narration only.
- **Segment 14 opens on two large zeros**, accent-to-warning gradient, holding four seconds before any other text. The R2.5 billion WIOCC figure renders in **accent**, not warning, because it is a confirmed figure.
- **Segment 10's `FIRST SA AI LAUNCH IN 7 WEEKS` card gets three seconds alone**, accent colour, no other text on screen, then a hard cut to the `BUT` block in `warning`.
- Segment 3's `SA IS ON THE SUPPORTED LIST` line animates in last, accent colour, slight scale-up. It is the payoff line of the top pick.
- On deliverable B, short segment 1 is a **hard cut in on frame one, no fade**. The date is the largest element on screen.

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

Note that the tool converts em dashes to ` - ` with padding. Follow it with `sed -i 's/ - / - /g'` on any file it modified.

The fenced ON-SCREEN TEXT blocks in `script.md` and `social.md` are already ASCII-clean and are the authoritative source for overlay strings. Copy from them. Do not retype overlay text from the narration.

**Two strings in this episode are quoted vendor copy and must survive verbatim through the ASCII pass.** In segment 5, `license them, including for compensation, to third parties`. In segment 8, the paired quotes `"hosted in Europe"` and `"any country in Europe and the USA"`. If the ASCII pass alters a character inside any of those, fix it by hand rather than accepting the substitution. They are quotations and their exact wording is the point.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 13:51 to 14:20. Static card, `#111111` background, white text, no motion.

**Deliverable B:** the short is too tight for a dedicated disclosure segment, so the disclosure runs as a **persistent corner caption for the full 1:28**, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge, always legible against the underlying footage.

Card text for deliverable A, exactly:

```
AI DISCLOSURE

Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**Minimum five seconds on screen. This segment must not be cut for runtime.** If the episode runs long, trim segment 15 first, then 14, then 13.

**Platform declaration is separate and additional.** At upload, set the AI-generated content toggle on YouTube, TikTok, Instagram and Facebook. The on-video card does not satisfy the platform requirement, and the platform toggle does not satisfy the on-video requirement. Both are needed.

---

## 9. Execution flow for Claude Code

1. Read `script.md` and `social.md` fully before touching an API.
2. **Check the date.** If it is on or after 29 September 2026, stop and report. This episode needs an edit before it renders - see section 0.
3. Run `ascii_fix.py` across all four files in this directory. Confirm four `OK` lines. Then check the two quoted passages named in section 7 survived intact.
4. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. If missing, generate once and commit.
5. Render narration: 17 ElevenLabs calls for A, 5 for B, one per segment, into `audio/`.
6. Listen to segment 8 first for `tiun`, then segments 5, 10, 11 and 15. Re-render individual segments as needed.
7. Measure actual audio durations per segment. **The timing table in `script.md` is a 160 wpm estimate. Rebuild the real timing table from the rendered audio** and use those numbers for the YouTube chapters in `social.md` section 3, not the estimate.
8. Render the five Kling clips to stage. Inspect each. K3 against the empty-room brief specifically.
9. Build the Shotstack stage payload for deliverable A against the real audio durations.
10. Submit deliverable A to the Shotstack **stage** endpoint. Download and inspect end to end.
11. Repeat 9 and 10 for deliverable B, including the persistent disclosure caption.
12. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
13. On approval: production render, then work through section 11.

Do not proceed past step 12 without approval, and do not batch steps 1 through 12 for all seven queued episodes before reporting.

---

## 10. Cost breakdown

Stage-pass estimate for this episode only:

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 15,600 characters across both deliverables | $1.40 - $1.95 |
| Higgsfield Soul stills | 0 new if cache present, otherwise 5 | $0.00 - $1.50 |
| Higgsfield Kling clips | 5 clips at 5 seconds | $3.25 - $4.50 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 7 stage total** | | **$4.65 - $8.95** |

At R16.25 that is roughly **R76 to R146**.

Prior episodes for comparison: episode 1 $18-28, episode 2 $16.35-24.65, episode 3 $13.44-19.68, episode 4 $5.85-7.38, episode 5 $4.65-8.90, episode 6 $4.60-8.85. Three episodes now sitting inside the same band. The pipeline cost is stable and the image cache is doing the work.

**Seven-episode combined stage cost, if all seven are rendered: approximately $67.50 to $106.50, or R1,097 to R1,731.** Production renders are additional and are typically two to three times the stage cost, which puts the full seven-episode production run somewhere between roughly R3,300 and R6,900 all in.

That number is the reason section 0 asks for a decision before anything runs. Two of those seven episodes would need content edits before they could be published at all.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B, not just the opening frames
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] The two quoted vendor passages from section 7 render verbatim on screen
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent across all segments, no clipping, no dead air over two seconds
- [ ] `tiun` reads as TEE-oon on playback, in every segment it appears
- [ ] Segment 5 beat three is completely static - no Ken Burns leaked onto it
- [ ] Segment 11's four ERROR lines land 0.5 seconds apart and the final line holds five seconds
- [ ] YouTube chapters in `social.md` rebuilt from rendered audio durations, not the estimate table
- [ ] Every uncertain figure rendered in the warning colour, not the accent: Higgsfield rates, the 23 Sep lock-in date, the tiun onboarding line, Axari's absent prices
- [ ] The tiun SA-onboarding claim marked NOT VERIFIED in `social.md` section 9 appears nowhere in either video or any caption as a positive statement
- [ ] **29 September 2026 still in the future on the publication date.** If not, edit before shipping.
- [ ] 14 October Bolt Forge preview expiry still in the future on the publication date
- [ ] `[LINK]` placeholder in the WhatsApp broadcast replaced with the real video URL
- [ ] WhatsApp broadcast re-counted after the link is inserted, still under 700 characters (currently 659 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Every claim in `social.md` section 9 re-confirmed against its source URL
- [ ] Section 14 updated with live post links

---

## 12. Series notes

Carry these forward.

- **Write the script lean from the start.** Episode 4 needed three trim passes from 18:37 to 14:57. Episode 5 landed at 15:10 with two light passes. Episode 6 came in at 17:49 and needed two structural passes to reach 15:12. Episode 7 came in at **18:58** and needed **three** passes to reach 15:44 - the worst overshoot yet, on a ten-tool episode with unusually dense legal material. **The working budget is 145 to 155 narration words per tool segment.** Ten tools at 150 is 1,500 words, which leaves roughly 900 for framing, structural and closing segments. Write to that ceiling, do not trim down to it.
- **A long quoted legal passage costs more runtime than it looks like on the page.** Segment 5 of this episode is 260 words because the StackBlitz policy language cannot be paraphrased without losing the point. Budget for one such segment per episode and take the words off the other tools, not off segment 5.
- **Measure before writing the timing table.** Never put an estimated table in the script and leave it unsynced to the headings. Measure, then write the table and the headings in the same pass.
- **When you trim a narration block, re-check its overlay.** Episode 6's segment 12 overlay still referenced a GPU price after the narration line was cut. In episode 7 the reverse happened deliberately: several overlays retain figures the trimmed narration no longer speaks. That is fine when the overlay figure is still accurate. It is not fine when the narration and overlay now disagree. Check for disagreement, not for difference.
- **Kling clip count matters.** Three clips read as static in episode 4. Five is the right number for a nine or ten tool episode. Write the clip assignments into the script's B-ROLL notes next time rather than patching the count in the brief.
- **The image cache is the single biggest cost saver.** Protect it. Seven briefs have now asked for it to be verified.
- **Uncertainty is content, not a defect.** This episode's strongest material is a pricing page that loads with no prices on it, a security vendor whose four trust pages all error, eight of ten tools with a broken legal path, and seven consecutive weeks of zero POPIA mentions. Render those honestly rather than smoothing them over.
- **Time-limited offers need a publication deadline in the brief, not just in the script.** Episode 6 proved why: its content expired while it sat in the queue and the warning in its own section 0 went unread. Episode 7 carries two hard dates. Put them at the top, as this brief does.
- **The unrendered backlog is now seven episodes and one of them has already gone off.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 7
week_of: 2026-09-21
window_covered: 2026-09-14 to 2026-09-21
tools_covered: 10
top_pick: Creem 2.0
second_pick: VoiceCap
warning_item: Axari Twin (privacy, security, trust and pricing pages all error; unbacked no-training claim)
biggest_story: StackBlitz opt-out model training and dataset licensing, live 29 Sep, no SA carve-out
best_free_item: VoiceCap (300 minutes, 1 seat, no card)
best_data_disclosure: VoiceCap (EU hosting, no AI training, 13 named subprocessors, SCCs)
worst_data_default: Higgsfield API (trains on inputs and outputs, deletion-only remedy, no toggle)
only_sa_priced_tool: BrandAxis (mentioned, not covered - PR not launch)
only_sa_launch: KUMii by 22 On Sloane - first date-verifiable SA AI launch in 7 weeks
only_tool_naming_south_africa: Creem 2.0 (86-country supported merchant list, local bank transfer)
african_data_residency_offered_by_any_tool: false
broken_legal_or_pricing_paths: 8 of 10
episode_thesis: "Eight of ten vendors cannot keep a legal or pricing page online. Read the policy, not the marketing."
content_expiry_date: 2026-09-29
content_expiry_reason: StackBlitz opt-out window closes; short segment 1 and long-form segment 5 both built on it
secondary_expiry_date: 2026-10-14
secondary_expiry_reason: Bolt Forge research preview ends, 50X usage claim lapses
inferred_date_in_content: 2026-09-23 (Higgsfield discount lock-in, hedged on air)
fx_rate_used: 16.25
fx_rate_date: 2026-09-21
fx_source_spread_pct: 0.13
fx_sources: 5
fx_stale_outliers_excluded: 2 (Wise, Revolut - both approx 5 percent off, mentioned on air)
long_form_runtime_estimate: "15:44"
long_form_words: 2518
long_form_segments: 17
short_runtime_estimate: "1:28"
short_words: 236
short_segments: 5
kling_clips: 5
soul_stills_new: 0
soul_stills_reused: 5
stage_cost_estimate_usd: "4.65 - 8.95"
stage_cost_estimate_zar: "76 - 146"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
backlog_episodes_unrendered: 7
backlog_episodes_content_expired: 1 (episode 6, expired 2026-09-20)
popia_mentions_across_vendors: 0
popia_zero_streak_weeks: 7
african_residency_zero_streak_weeks: 7
relaunches_rejected: 5
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 and 6, which remain in force.

```
Creem 2.0, Creem, n8n 2.40, Bolt Forge, Bolt.new, StackBlitz,
Higgsfield API, VoiceCap, tiun, Appwrite 2.1, Appwrite 2.2,
KUMii, 22 On Sloane, Axari Twin, Axari, Ami AI, AiSDR,
Sider Omni Sidebar, Lumiko, Bitrise Remote Dev Environments,
AGROSYNC, DataSync Africa, Synapse Analytics, BIZOACH,
Claude Code Projects, Weave Router 2.0, Naoma, Oats,
ProductBridge, BrandAxis, WIOCC, Askya
```

### Carried forward for future episodes

- **Lelapa AI and Vulavula. Seventh consecutive week unresolved.** The Vulavula release notes still stop at 12 August 2026, and the only in-window Lelapa item was an ITWeb video package indexed 19 September that repackaged the 31 August to 5 September news week. Seven weeks of the date rule blocking the most locally relevant story in the series is no longer a scheduling accident. **Recommend a one-off out-of-window standalone feature** rather than an eighth week of waiting.
- **Tether TranslatePsy AfriSLM.** Offline open-source models for 19 African languages, released 2 September. Still the direct answer to the language gap in every notetaker and transcription tool covered since. Deserves a standalone treatment alongside the Lelapa feature.
- **BrandAxis as a South African pricing case study.** Not a launch, so not covered, but it is the only tool found in seven weeks priced in rand across all four tiers with a plain no-training statement. Worth a segment on why local vendors publish rand pricing and clear data terms while international ones do neither.
- **South African data centre policy as a segment.** The 17 September US DFC investment into WIOCC, Johannesburg-headquartered, up to roughly R2.5bn, is the strongest infrastructure story the series has found. Pair it with the absence of any South African data-localisation mandate.
- **Undated South African tech press.** TechCentral's AI section, TechCabal's AI category, Disrupt Africa, Techpoint, iAfrica and Ventureburn all render without dates, which makes them unusable against a seven-day rule. **Seventh consecutive episode this has been the largest research gap.** Worth solving with a different access method rather than accepting it an eighth time.
- **Relaunch rate is climbing.** Five rejected this week, the highest in the series: Appwrite 2.0, OpenAI Agents API, Weave Router 2.0, Naoma V2, Oats. Product Hunt's top slots increasingly carry products that shipped weeks earlier. The date check is now the most valuable step in the research pass.

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
