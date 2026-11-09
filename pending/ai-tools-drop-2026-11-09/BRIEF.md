# Production Brief - AI Tools Drop, Week of 9 November 2026

**Episode 14.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 13:22 (measured, 2,131 narration words at 160 wpm)
- Short runtime target: 1:06 (measured, 176 narration words)
- 17 segments this week (eight tools).

---

## 0. Read this before you spend anything

**Backlog warning. This is the fourteenth unrendered episode in `pending/`.**

Checked on 9 November: `pending/` holds thirteen earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 9 Nov | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 14 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 13 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 12 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 10 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 9 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 8 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 7 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 6 weeks | Not rendered. **1 October wording is stale.** |
| `ai-tools-drop-2026-10-05` | 5 October | 5 weeks | Not rendered. **Content expired 12 October.** |
| `ai-tools-drop-2026-10-12` | 12 October | 4 weeks | Not rendered. **Eleven v4 line expired 13 October.** |
| `ai-tools-drop-2026-10-19` | 19 October | 3 weeks | Not rendered. **AI Expo Africa "upcoming" line expired 28 October.** |
| `ai-tools-drop-2026-10-26` | 26 October | 2 weeks | Not rendered. **Segment 11 "tomorrow" and "Friday" lines expired 27 to 30 October.** |
| `ai-tools-drop-2026-11-02` | 2 November | 1 week | Not rendered. **Meta AI Academy "winners not published" line needs a recheck; Gemini Slides promo limits end 1 December.** |
| `ai-tools-drop-2026-11-09` | 9 November | Current | This brief |

Eight earlier episodes (6 to 13) now need content edits before they could be published. Michael has been asked whether to keep the series running, pause it or stop it. **No answer yet. Do not render any episode, including this one, without his written choice.**

**Time-limited items in this episode.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Gemini in Google Forms Scheduled Release start | **19 November 2026** | Segment 4 says "from 19 Nov". After that, reword to "rolling out". |
| Afda + ZenRobot course start | **24 November 2026** | Segment 12. After that date the course line is stale. |
| Meta AI Academy SA winners "not published yet"; Istanbul summit | **24 and 25 November 2026** | Segment 12 and the article. Recheck before render. |
| ChatGPT Dots admin preview | **18 November 2026** | Article follow-ups only. |
| OpusClip 40 percent first-month discount | No end date stated | Article only; not in the script. |
| Gemini Omni 1.1 routes to 1.2 | **3 December 2026** | Article only. |
| Synthesia in ChatGPT public beta | Any day | Segment 6 says "public beta". Recheck pricing before render. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**Editorial note.** This episode covers other AI video tools (Gemini Omni, Synthesia, OpusClip, ChatGPT GIFs). That is editorial content, not a pipeline instruction. **Keep the Kling v2.1 endpoint in section 5 for this episode.** Any model or vendor change is Michael's decision, and would need its own stage test and cost check.

**Self-disclosure note.** Segment 15 mentions Perplexity Teammates and says this series is researched with Perplexity. Do not cut that sentence for time.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 13:22 | YouTube, Facebook native, WhatsApp channel |
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

**Pronunciation guide is in the script header.** This week's high-risk tokens: `Synthesia` (sin-THEE-zee-uh), `OpusClip` (OH-pus-klip), `Floot` (rhymes with boot), `Omni` (OM-nee), `Acrobat` (AK-roh-bat), `SCOUT` (skowt), `isiZulu` and `isiXhosa`, `Absa` (AB-suh), `Paystack` (PAY-stak), and the spelled-out web address in segment 10. Listen to segments 6, 7, 9, 10 and 12 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Three clips this week, K1 to K3.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images once they exist. One new still (B7) this week.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime.

Rough split by runtime: Kling about 15 seconds, Soul stills about 2.5 minutes, Shotstack the remainder.

**Third-party product footage.** Where the script asks for a screen recording of ChatGPT, Synthesia or Google Vids, record it yourself or use a Shotstack mock-up. Never use the vendors' marketing videos.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`: `B1` (abstract data-flow field), `B2` (desk workspace, low light), `B3` (abstract network mesh), `B6` (dusk cityscape, warm), `A16` (Johannesburg skyline).

**Fourteenth brief asking for this cache. Checked on 9 November: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 2 (dimmed) | Slow push in |
| B2 | 4 | Ken Burns, slow push in |
| B3 | 6 (fallback if no screen recording) | Ken Burns, slow drift, cool grade |
| B6 | 8 | Ken Burns, warm |
| B7 (new) | 10 - Skilling Africa | Ken Burns, slow push in |
| A16 | 12 (SA corner), 17 (Close), short segment 5; fallback for 10 | Slow push in; push out and fade on the close |

The script text for segments 2, 4, 6 and 8 names the stills by subject; the cached B-series are abstract. Use the cached asset regardless. Do not generate new stills to match the script wording, except B7.

**B7 prompt direction:** a young person studying on a phone in a quiet, empty salon after hours, warm practical light, phone screen glow, face turned away or out of focus. No readable screen, no logos.

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
| K1 | 1 - Cold open, 3 - ChatGPT Images, short segment 2 | A phone lying on a salon counter, screen glowing with abstract looping colour shapes, slow push in, warm light. No readable text, no app UI, no people. |
| K2 | 5 - Gemini Omni, short segment 3 | An empty, unbranded living room; a band of light sweeps across a sofa as the camera dollies slowly. No logos, no text, no people. |
| K3 | 7 - OpusClip, short segment 4 | A phone on a small tripod in a home office facing an empty chair, camera slowly orbits. No readable screen, no logos, no faces. |

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: "Limits per plan: not published" in segment 3; "Not on Business Starter" in segment 4; "Label AI video on social" in segment 5; "Public beta" in segment 6; "Free: no editing, watermark" in segment 7; "SA price: check your account" in segment 8; the last two lines of segment 9; all three restriction lines in segment 11; "(vendor figure)" and "not yet published" in segment 12; "Texting: US only" in segment 14.
- **Segment 9:** a generic chat-to-app-to-card-machine diagram with a warning triangle on the Stripe step. No Stripe, Paystack, Payfast, Yoco or Peach logos.
- **Segment 13:** a four-branch decision tree, ASCII only. Align with spaces, not tabs. No arrow glyphs.
- **Segment 3:** if a WhatsApp Status mock-up is used, it must be generic. **No WhatsApp logo, no WhatsApp green.**
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

**Protected strings.** `$0.07/sec`, `$1.04 (R17)`, `$14.50/mo`, `R4,500`, `42% to 67%`, `4 days to 1`, `15+ programmes`, `ChatGPT/Claude`, `skillingafrica.withgoogle.com` and `"Extended network"` (straight ASCII quotes) must survive exactly. `+` in `Afda + ZenRobot` and `isiZulu + isiXhosa` is a plain plus sign.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 12:09 to 12:34. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:06, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

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
3. **Check the date** against the section 0 table, and recheck the Meta AI Academy winners line and Synthesia pricing. Edit before rendering.
4. Run `ascii_fix.py` across all four files. Confirm four `OK` lines and that the protected strings in section 7 survived.
5. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 9 November.** Generate once and commit. Generate B7.
6. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
7. Listen to segments 6, 7, 9, 10 and 12 first for names and figures. Re-render individual segments as needed.
8. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters from rendered audio.**
9. Render the three Kling clips to stage and inspect each.
10. Build and submit the Shotstack **stage** payload for A, then B.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then section 11.

---

## 10. Cost breakdown

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 13,600 characters across both deliverables | $1.25 - $1.80 |
| Higgsfield Soul stills | 5 cached-set stills (cache absent) plus B7 | $0.00 - $1.50 |
| Higgsfield Kling clips | 3 clips at 5 seconds | $1.95 - $2.70 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 14 stage total** | | **$3.20 - $7.00** |

At R16.48 that is roughly **R53 to R115**.

**Fourteen-episode combined stage cost, if all fourteen are rendered: approximately $93.40 to $160.25, or about R1,539 to R2,641 at R16.48.** Production renders are additional, typically two to three times stage cost.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] Protected strings in section 7 render correctly on screen
- [ ] No OpenAI, Google, Synthesia, OpusClip, Adobe, Floot, Stripe, Paystack, Payfast, Yoco, Peach, Absa, Meta, Amazon or WhatsApp logos in any generated footage
- [ ] Any screen recording of a third-party product is our own recording, not vendor marketing footage
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] Short is at least 60 seconds as rendered
- [ ] YouTube chapters rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] Section 0 dated items still accurate
- [ ] `[LINK]` placeholder replaced, broadcast re-counted, still under 700 characters (currently 424 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **A video week, handled as a choice.** Four of eight tools make video. Segment 13 gives owners a plain rule for choosing one, rather than four separate sales pitches.
- **A South African payments caveat stated plainly.** Floot depends on Stripe, which reaches South Africa only as an "Extended network" country via Paystack. The script tells builders to check first and names local gateways.
- **Old news rejected.** Tobira Site Agent (on sale in October) and Sunbird Sunflower v2 (24 September) were popular this week but are not new launches.
- **Absa framed as an update.** Absa first described its AI debt review system in August; this week's interview adds the onboarding pilot.
- **The unrendered backlog is now fourteen episodes, eight need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 14
week_of: 2026-11-09
window_covered: 2026-11-02 to 2026-11-09
tools_covered: 8
top_pick: ChatGPT Images 2.6
second_pick: Skilling Africa with Google
action_item: Make one AI GIF for WhatsApp Status and label it; put one staff member through one Skilling Africa module
not_available_in_sa: Claude Personal Finance (US only), Meta Muse Spaces (Muse markets only), Alexa for Shopping by SMS (US invite only)
watch_items: WhatsApp Expand (beta; Meta AI country-limited)
sa_story: Absa AI debt review 4 days to 1; Dell Forum SA AI adoption 42% to 67%; Afda + ZenRobot course
content_expiry_date: 2026-11-19
content_expiry_reason: Gemini in Google Forms reaches Scheduled Release domains
secondary_expiry_reason: Afda course starts and Meta AI Academy summit on 24 November
fx_rate_used: 16.48
fx_rate_date: 2026-11-09
fx_sources: 3
long_form_runtime_estimate: "13:22"
long_form_words: 2131
long_form_segments: 17
short_runtime_estimate: "1:06"
short_words: 176
short_segments: 5
whatsapp_broadcast_chars: 424
kling_clips: 3
soul_stills_new: 6 (cache absent in repo, plus B7)
stage_cost_estimate_usd: "3.20 - 7.00"
stage_cost_estimate_zar: "53 - 115"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
series_decision_pending: true
backlog_episodes_unrendered: 14
backlog_episodes_needing_edits: 8 (episodes 6 to 13)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 13, which remain in force.

```
ChatGPT Images 2.6, Gemini in Google Forms insights, Gemini Omni 1.2 Flash,
Google Vids 15-second clips, Synthesia in ChatGPT and Claude, OpusClip 4.0,
Acrobat AI Assistant web search, Floot Payments, Skilling Africa with Google,
Claude Personal Finance, Meta Muse Spaces, Alexa for Shopping by SMS,
Absa AI debt review, Dell Forum SA adoption figure, Afda + ZenRobot course,
Perplexity Teammates, Kimi K3.1 Pro, Inkling 2 Small, GPT-6 Cyber,
Tobira Site Agent, Sunbird Sunflower v2, Wanaka Studio, Glasshand
```

Exceptions: re-cover Claude Personal Finance or Meta Muse Spaces if either reaches South Africa; cover WhatsApp Expand if it is confirmed in South Africa; cover the Meta AI Academy SA pitch winners when announced; re-cover Floot if it adds a South African payment provider.

### Carried forward for future episodes

- **Claude Duet and 1Password for Agents.** Re-cover if either opens to South Africa or to business accounts.
- **Meta Muse Wonder and Spaces.** Re-cover if Meta confirms availability in South Africa.
- **Gemini agent.** Re-cover when small businesses can sign up with a price.
- **ChatGPT Dots texting and Gemini 4 Carbon.** Re-cover when they reach South Africa or businesses.
- **SalesCloser and Empacer.** Re-cover once a standard price is published.

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
