# Production Brief - AI Tools Drop, Week of 14 September 2026

**Episode 6.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 15:12 (measured, 2,411 narration words at 160 wpm)
- Short runtime target: 1:19 (measured, 212 narration words)

---

## 0. Read this before you spend anything

**Backlog warning. This is the sixth unrendered episode in `pending/`.**

Queued and not yet rendered:

| Directory | Week | Age at 14 Sept | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 6 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 5 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 4 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 2 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 1 week | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | Current | This brief |

Episodes 3, 4 and 5 each carried an escalation asking for a direction on the backlog. None was answered. Four of these six are now unpublishable as weekly news: the pricing, promo codes and expiry dates in episodes 1 through 4 have moved on, and episode 1 is six weeks old.

**This episode has a hard deadline attached to its content.** The Typewise Nova launch gift expires on **20 September 2026**. If episode 6 renders after that date, segments 6 and 15 and three of the five social cuts all state an offer that no longer exists. Either render and publish episode 6 before 20 September, or expect to edit those segments.

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem. Six episodes rendered blind is six times the cost of one wrong decision.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 15:12 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:19 | TikTok, Instagram Reels, YouTube Shorts |

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

**Render one API call per segment.** Seventeen calls for deliverable A, six for deliverable B. Do not batch the full script into a single request - a single mispronunciation then costs one segment to redo, not the whole episode.

Name the files `seg01.mp3` through `seg17.mp3` for A and `short01.mp3` through `short06.mp3` for B, in an `audio/` subdirectory.

**Pronunciation guide is in the script header.** Read it before rendering. This week's high-risk tokens are `Relaticle` (rel-AT-i-kul), `Widgo` (WIJ-oh), `n8n` (en-EIGHT-en), `Loqua` (LOH-kwah), `Subanana` (soo-bah-NAH-nah), `POPIA` (poh-PEE-uh), `AGPL` (ay-gee-pee-EL), `Samrand` (SAM-rand), `AfriSLM` (AF-ree-slim), `Injini` (in-JEE-nee) and `Vulavula` (voo-lah-VOO-lah).

**Numbers are written longhand in the narration deliberately** so the model reads them correctly, and as digits in the overlay text. Do not reconcile the two. If you "fix" the narration to use digits, the voice model will read R16.11 as something unusable.

After rendering, listen to segments 4, 7, 10, 11 and 13 specifically. Segment 13 carries five South African language names in a row and segment 11 carries the same four again as negatives - those are the highest-risk reads in the episode.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers. The ratio is what keeps the cost down.

**Layer 1 - Kling motion clips, 5 seconds each.** Five clips this episode, at segments 1, 6, 9, 15 and 17. Episode 4 used three and the stage render read as static through the middle third. Five is the established number.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images. Do not regenerate them.

**Layer 3 - Shotstack motion graphics.** This carries the bulk of the runtime and it is the cheapest layer. Every pricing table, comparison bar, checklist, language grid and map graphic is built here from text and shapes, not generated.

Rough split by runtime: Kling about 25 seconds total, Soul stills about 2 minutes, Shotstack graphics the remaining 12-plus minutes.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** These live in `assets/ai-tools-drop/`:

- `B1` - abstract data-flow field, dark, amber accents
- `B2` - desk workspace, low light, screens
- `B3` - abstract network mesh
- `B6` - dusk cityscape, warm
- `A16` - Johannesburg skyline

**This is the sixth brief that has asked for this caching.** If the directory is empty or the files are missing, regenerate once and commit them so the seventh brief does not have to ask again.

Assignments this episode:

| Asset | Segment | Motion |
| --- | --- | --- |
| B2 | 3 (Desert Ant Labs) | Slow push in |
| B6 | 5 (Widgo) | Slow drift right |
| B3 | 7 (n8n) | Slow drift left |
| A16 | 12 (African compute) | Slow pull back |
| B1 | 14 (POPIA count) | Static, no motion - let the six zeros carry it |

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
| K1 | 1 - Cold open | Slow dolly push in on a dark server rack, one amber status light pulsing, a city skyline soft-focus through a window behind it. No text, no people. Cold and controlled. |
| K2 | 6 - Typewise Nova | A dim, empty support desk at night, one monitor glowing, a chair slightly turned. Static camera, faint screen flicker. Sense of a clock running. |
| K3 | 9 - Cognition SWE-2 | Code scrolling on a dark monitor, then the frame slowly washing with a deep red vignette from the edges inward. Abstract, no readable text. |
| K4 | 15 - What I would try | A hand placing a phone face down on a wooden desk, slow and deliberate, warm side light. No faces, no branding. |
| K5 | 17 - Close | Slow pull back from a city skyline at dusk, lights coming on across the buildings. Calm, resolved. |

Negative direction on all five: no text, no watermarks, no logos, no identifiable faces, no fast camera whips.

Render each to stage quality first and inspect. K3 is the one most likely to come back looking like a stock security cliche. If it does, replace it with a Shotstack-built abstract rather than re-rolling Kling twice.

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
- Any figure the script flags as uncertain gets the `warning` colour, not the accent. This episode that covers: Desert Ant's absent paid price, Relaticle's unnamed cloud location, GoodLads' unnamed country, Loqua's absent prices, and the two claims marked NOT VERIFIED in `social.md` section 9 (which must not appear on screen at all).
- **Segment 9's locked-toggle card is the episode's warning beat.** Hold it four seconds static, `warning` colour, no motion. Do not undercut it with animation.
- **Segment 11's language grid holds four seconds.** The four struck-through South African language names are the strongest single visual in the episode. Let them sit.
- **Segment 14's six zeros animate in sequence, one per week, then hold three seconds all together.** No sound effect, no flourish.
- Segment 6's `EXPIRES 20 SEPT` pulses exactly once in `warning`, then holds static in accent. One pulse, not a loop.

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

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 14:11 to 14:36. Static card, `#111111` background, white text, no motion.

**Deliverable B:** the short is too tight for a dedicated disclosure segment, so the disclosure runs as a **persistent corner caption for the full 1:19**, reading exactly `AI VOICE + AI VISUALS`. Bottom-right, minimum 3 percent of frame height, always legible against the underlying footage.

Card text for deliverable A, exactly:

```
AI DISCLOSURE

Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**Minimum five seconds on screen. This segment must not be cut for runtime.** If the episode runs long, trim segment 12 or segment 13 instead.

**Platform declaration is separate and additional.** At upload, set the AI-generated content toggle on YouTube, TikTok, Instagram and Facebook. The on-video card does not satisfy the platform requirement, and the platform toggle does not satisfy the on-video requirement. Both are needed.

---

## 9. Execution flow for Claude Code

1. Read `script.md` and `social.md` fully before touching an API.
2. Run `ascii_fix.py` across all four files in this directory. Confirm four `OK` lines.
3. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. If missing, generate once and commit.
4. Render narration: 17 ElevenLabs calls for A, 6 for B, one per segment, into `audio/`.
5. Listen to segments 4, 7, 10, 11 and 13 and confirm the pronunciation guide held. Re-render individual segments as needed.
6. Measure actual audio durations per segment. **The timing table in `script.md` is a 160 wpm estimate. Rebuild the real timing table from the rendered audio** and use those numbers for YouTube chapters, not the estimate.
7. Render the five Kling clips to stage. Inspect each.
8. Build the Shotstack stage payload for deliverable A against the real audio durations.
9. Submit deliverable A to the Shotstack **stage** endpoint. Download and inspect end to end.
10. Repeat 8 and 9 for deliverable B, including the persistent disclosure caption.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then work through section 11.

Do not proceed past step 11 without approval, and do not batch steps 1 through 11 for all six queued episodes before reporting.

---

## 10. Cost breakdown

Stage-pass estimate for this episode only:

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 14,800 characters across both deliverables | $1.35 - $1.85 |
| Higgsfield Soul stills | 0 new if cache present, otherwise 5 | $0.00 - $1.50 |
| Higgsfield Kling clips | 5 clips at 5 seconds | $3.25 - $4.50 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 6 stage total** | | **$4.60 - $8.85** |

At R16.11 that is roughly **R74 to R143**.

Prior episodes for comparison: episode 1 $18-28, episode 2 $16.35-24.65, episode 3 $13.44-19.68, episode 4 $5.85-7.38, episode 5 $4.65-8.90. The downward trend is the hybrid approach and the image cache working as intended, and it has now flattened - episode 6 is level with episode 5, which is what a stable pipeline looks like.

**Six-episode combined stage cost, if all six are rendered: approximately $62 to $97, or R999 to R1,563.** Production renders are additional and are typically two to three times the stage cost. That number is the reason section 0 asks for a decision before anything runs.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge
- [ ] Audio levels consistent across all segments, no clipping, no dead air over two seconds
- [ ] All pronunciation-guide tokens read correctly on playback, especially the five language names in segment 13
- [ ] YouTube chapters rebuilt from rendered audio durations, not the estimate table
- [ ] Every uncertain figure rendered in the warning colour, not the accent
- [ ] The two NOT VERIFIED claims in `social.md` section 9 appear nowhere in either video or any caption
- [ ] Typewise 20 September date correct everywhere, and publication scheduled before it
- [ ] WhatsApp broadcast confirmed under 700 characters (currently 688)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Every claim in `social.md` section 9 re-confirmed against its source URL
- [ ] Section 14 updated with live post links

---

## 12. Series notes

Carry these forward.

- **Write the script lean from the start.** Episode 4 needed three trim passes from 18:37 to 14:57. Episode 5 landed at 15:10 with two light passes. Episode 6 was written at roughly 180 words per tool segment, came in at 17:49, and needed two structural trim passes to reach 15:12. **The working budget is 145 to 155 narration words per tool segment, not 180.** Nine tools at 150 words is 1,350 words, which leaves about 1,000 for the framing, structural and closing segments.
- **Measure before writing the timing table.** Never put an estimated table in the script and leave it unsynced to the headings. Measure, then write the table and the headings in the same pass.
- **When you trim a narration block, re-check its overlay.** Episode 6's segment 12 overlay still referenced a GPU price after the narration line was cut. Caught on review, but it would have rendered.
- **Kling clip count matters.** Three clips read as static in episode 4. Five is the right number for a nine or ten tool episode.
- **The image cache is the single biggest cost saver.** Protect it.
- **Uncertainty is content, not a defect.** This episode's strongest material is the vendor with no pricing page, the pricing page with no prices, the marketing that contradicts its own privacy policy, the 52-language product with one African language, and six consecutive weeks of zero POPIA mentions. Render those honestly rather than smoothing them over.
- **Time-limited offers need a publication deadline in the brief, not just in the script.** Episode 6 is the first episode whose content expires. Note the expiry in section 0 of any future brief that carries one.
- **The unrendered backlog is now six episodes.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 6
week_of: 2026-09-14
window_covered: 2026-09-07 to 2026-09-14
tools_covered: 9
top_pick: Desert Ant Labs (Redact)
second_pick: Typewise Nova
warning_item: Cognition SWE-2 in Devin (free tier may train on your code, opt-out is paid-only)
best_free_item: Desert Ant Labs (free to 100,000 monthly active devices per platform)
best_data_disclosure: Widgo (regions and subprocessors named, no foundation-model training)
strongest_written_data_commitment: Typewise Nova (EU or US hosting, zero LLM retention, AWS Frankfurt)
worst_data_default: Devin free tier
only_sa_launch: none - no date-verifiable South African AI product launch in window
african_data_residency_offered_by_any_tool: false
episode_thesis: "No vendor offers African data residency. Self-host or on-device are the only answers."
content_expiry_date: 2026-09-20
content_expiry_reason: Typewise Nova launch gift expires
fx_rate_used: 16.11
fx_rate_date: 2026-09-13
fx_source_spread_pct: 0.37
fx_sources: 4
long_form_runtime_estimate: "15:12"
long_form_words: 2411
short_runtime_estimate: "1:19"
short_words: 212
kling_clips: 5
soul_stills_new: 0
soul_stills_reused: 5
stage_cost_estimate_usd: "4.60 - 8.85"
stage_cost_estimate_zar: "74 - 143"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
backlog_episodes_unrendered: 6
popia_mentions_across_vendors: 0
popia_zero_streak_weeks: 6
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the list in episode 5's brief, which remains in force.

```
Desert Ant Labs, Redact, Relaticle, Widgo, Typewise Nova, Typewise,
n8n 2.39.x, GoodLads, Cognition SWE-2, Devin, Loqua,
Live Captions by Subanana, Subanana, Meta Muse, Anysite.io,
Dictantor, Epilude Notetaker, Raycast 2.0, Cline Desktop,
Mastra Factory, Harden, ChatGPT Images 2.5, Suno v6, Youkti,
Cortex, Resurf, Digital Parks Africa NDC1,
Cassava Vodafone Egypt AI factory, Tether TranslatePsy AfriSLM,
Perplexity Hybrid Compute, Injini AI for Education
```

### Carried forward for future episodes

- **Lelapa AI and Vulavula. Sixth consecutive week unresolved.** Voice generation was covered on 5 September, two days outside the window, and the Vulavula release notes still stop at 12 August. This is the local story most worth covering properly and the date rule keeps blocking it. Consider a one-off out-of-window feature rather than waiting for a qualifying week.
- **Tether TranslatePsy AfriSLM.** Offline open-source models for 19 African languages including Zulu, Xhosa, Afrikaans, Tswana and Sotho, released 2 September. Missed the window by five days. It is the direct answer to the language gap in every tool covered this week and deserves a proper standalone treatment.
- **South African data centre policy as a segment.** Nigeria's CBN localisation mandate created a market that a South African operator went to Lagos to serve. There is a real episode in why no equivalent mandate exists here.
- **Undated South African tech press.** TechCentral's AI section and TechCabal's AI category both render without dates, which makes them unusable against a seven-day rule. This is the largest recurring gap in research coverage. Worth solving with a different access method rather than accepting it a seventh time.

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
