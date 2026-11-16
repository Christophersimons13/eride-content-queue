# Production Brief - AI Tools Drop, Week of 16 November 2026

**Episode 15.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 12:53 (measured, 2,045 narration words at 160 wpm)
- Short runtime target: 1:06 (measured, 175 narration words)
- 17 segments this week (eight tools, plus a "get found by AI" checklist in segment 13).

---

## 0. Read this before you spend anything

**Backlog warning. This is the fifteenth unrendered episode in `pending/`.**

Checked on 16 November: `pending/` holds fourteen earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 16 Nov | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 15 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 14 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 13 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 11 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 10 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 9 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 8 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 7 weeks | Not rendered. **1 October wording is stale.** |
| `ai-tools-drop-2026-10-05` | 5 October | 6 weeks | Not rendered. **Content expired 12 October.** |
| `ai-tools-drop-2026-10-12` | 12 October | 5 weeks | Not rendered. **Eleven v4 line expired 13 October.** |
| `ai-tools-drop-2026-10-19` | 19 October | 4 weeks | Not rendered. **AI Expo Africa "upcoming" line expired 28 October.** |
| `ai-tools-drop-2026-10-26` | 26 October | 3 weeks | Not rendered. **Segment 11 "tomorrow" and "Friday" lines expired 27 to 30 October.** |
| `ai-tools-drop-2026-11-02` | 2 November | 2 weeks | Not rendered. **Meta AI Academy "winners not published" line needs a recheck; Gemini Slides promo limits end 1 December.** |
| `ai-tools-drop-2026-11-09` | 9 November | 1 week | Not rendered. **Forms "from 19 Nov" line expires 19 November; Afda course and Meta AI Academy summit lines expire 24 November.** |
| `ai-tools-drop-2026-11-16` | 16 November | Current | This brief |

Nine earlier episodes (6 to 14) now need content edits before they could be published. Michael has been asked whether to keep the series running, pause it or stop it. **No answer yet. Do not render any episode, including this one, without his written choice.**

**Time-limited items in this episode.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Africa Tech Festival, CTICC | **17 to 19 November 2026** | Segment 12. After 19 November, reword to past tense or cut. |
| Gemini in Google Forms Scheduled Release start | **19 November 2026** | Segment 14. After that, reword to "rolling out". |
| Claude Data on by default for Enterprise | **20 November 2026** | Article only. |
| SA AI Index full report | **23 November 2026** | Segment 12 says it "lands on the twenty-third". After that, reword and check the final figures. |
| Meta AI Academy summit; winners still unpublished | **24 and 25 November 2026** | Article only. Recheck before render. |
| Skills in Workspace Scheduled Release start | **30 November 2026** | Segment 4. After that, reword to "rolling out". |
| Sheets canvas link Scheduled Release start | **2 December 2026** | Segment 14. |
| ChatGPT Standard and Advanced voice retire | **11 December 2026** | Segment 14. After that, cut the line. |
| Fireflies Clips and Scheduler "rolling out over the next couple of weeks" | Any day | Segment 8 and short segment 4. Recheck before render. |
| Businesses in ChatGPT beta; local listings US-only | Any day | Segment 3, short segment 2, WhatsApp post. Recheck eligibility before render. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**Editorial note.** Segment 15 mentions Higgsfield Miracle, a new video editor from the vendor that makes this series' visuals. That is editorial content, not a pipeline instruction. **Keep the Kling v2.1 endpoint in section 5 for this episode.** Any model or vendor change is Michael's decision, and would need its own stage test and cost check.

**Self-disclosure notes.** Segment 6 says the writing pipeline uses Claude models, and segment 15 says Higgsfield makes the visuals. Do not cut either sentence for time.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 12:53 | YouTube, Facebook native, WhatsApp channel |
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

**Pronunciation guide is in the script header.** This week's high-risk tokens: `Dageno` (duh-JEN-oh), `Persona` (per-SOH-nuh), `CIPC` (see-eye-pee-see), `Fireflies` and `Firefly` (keep them distinct), `Anthropic` (an-THROP-ik), `Altron` (AL-tron), `World Wide Worx` (said "works"), `CTICC` (letters), `Shariah` (shuh-REE-uh) and `Gemini four Hydrogen`. Listen to segments 3, 8, 9, 10 and 12 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Three clips this week, K1 to K3.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images once they exist. No new stills this week.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime.

Rough split by runtime: Kling about 15 seconds, Soul stills about 2.5 minutes, Shotstack the remainder.

**Third-party product footage.** Where the script asks for a screen recording of ChatGPT, Gmail, Claude, Fireflies, Firefly or Dageno, record it yourself or use a Shotstack mock-up. Never use the vendors' marketing videos. Blur any real business names in Business Hub recordings.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`: `B1` (abstract data-flow field), `B2` (desk workspace, low light), `B3` (abstract network mesh), `B6` (dusk cityscape, warm), `A16` (Johannesburg skyline).

**Fifteenth brief asking for this cache. Checked on 16 November: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 2 (dimmed) | Slow push in |
| B2 | 3 (fallback if no screen recording) | Ken Burns, slow push in |
| B3 | 5 (fallback if no screen recording) | Ken Burns, slow drift, cool grade |
| B6 | 8 (fallback) | Ken Burns, warm |
| A16 | 12 (SA corner), 17 (Close), short segment 5 | Slow push in; push out and fade on the close |

The script text names the stills by subject; the cached B-series are abstract. Use the cached asset regardless. Do not generate new stills to match the script wording.

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
| K1 | 1 - Cold open, 13 (dimmed), short segment 2 | A phone lying on a shop counter, screen glowing with abstract chat-bubble shapes, slow push in, warm light. No readable text, no app UI, no people. |
| K2 | 4 - Skills fallback, 9 - Firefly fallback, short segment 3 | Hands typing at a laptop, an abstract document layout on screen, slow pan. No readable text, no logos, no faces. |
| K3 | 6 - Claude Whiteboards fallback, short segment 4 | Blank sticky notes appearing on a whiteboard in time-lapse in a small office. No readable writing, no logos, no faces. |

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: "Local shops: US listings only, for now" and "Business Agents: US only" in segment 3; "English only. 18+." in segment 4; "Data: GA, needs a connector" in segment 6; "Zoom and Teams: not yet" in segment 7; "Clips + Scheduler: rolling out" in segment 8; "Credits per action: not stated" in segment 9; "South Africa coverage: not confirmed" in segment 10; all four lines in segment 11; "73% cannot measure value" and "0 SA startups" in segment 12; "Local shops: US only, for now" in short segment 2.
- **Segment 7:** the video-call grid is AI-generated. No Google Meet logo, no real faces.
- **Segment 10:** the visibility dashboard is a generic mock-up. No real brand names.
- **Segment 13:** a five-line numbered checklist, ASCII only. Align with spaces, not tabs. No arrow glyphs.
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

**Protected strings.** `$20/mo = approx R338`, `$10/seat/mo yearly = approx R169`, `$49/mo = approx R829`, `93%`, `73%`, `1%`, `17-19 Nov`, `.xlsx`, `JP, UK, IN`, `Std/Plus` and `R16.92 / USD` must survive exactly. `+` in `AI VOICE + AI VISUALS`, `Workspace + personal` and `summaries + drafts` is a plain plus sign.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 11:39 to 12:04. Static card, `#111111` background, white text, no motion.

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
3. **Check the date** against the section 0 table, and recheck Businesses in ChatGPT eligibility, Fireflies Clips status and Dageno coverage. Edit before rendering.
4. Run `ascii_fix.py` across all four files. Confirm four `OK` lines and that the protected strings in section 7 survived.
5. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 16 November.** Generate once and commit.
6. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
7. Listen to segments 3, 8, 9, 10 and 12 first for names and figures. Re-render individual segments as needed.
8. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters from rendered audio.**
9. Render the three Kling clips to stage and inspect each.
10. Build and submit the Shotstack **stage** payload for A, then B.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then section 11.

---

## 10. Cost breakdown

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 13,200 characters across both deliverables | $1.25 - $1.80 |
| Higgsfield Soul stills | 5 cached-set stills (cache absent) | $0.00 - $1.50 |
| Higgsfield Kling clips | 3 clips at 5 seconds | $1.95 - $2.70 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 15 stage total** | | **$3.20 - $7.00** |

At R16.92 that is roughly **R54 to R118**.

**Fifteen-episode combined stage cost, if all fifteen are rendered: approximately $96.60 to $167.25, or about R1,634 to R2,830 at R16.92.** Production renders are additional, typically two to three times stage cost. The weaker rand adds about R95 to R160 to the backlog's rand cost compared with last week's rate.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] Protected strings in section 7 render correctly on screen
- [ ] No OpenAI, Google, Anthropic, Fireflies, Adobe, Dageno, Shopify, Meta, Altron or WhatsApp logos in any generated footage
- [ ] Any screen recording of a third-party product is our own recording, with real business names blurred
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] Short is at least 60 seconds as rendered
- [ ] YouTube chapters rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] Section 0 dated items still accurate
- [ ] `[LINK]` placeholder replaced, broadcast re-counted, still under 700 characters (currently 428 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **An office week with one practical thread.** Businesses in ChatGPT and Dageno both address how AI assistants describe a business. Segment 13 turns that into a five-step checklist rather than a pitch for either tool.
- **The ChatGPT eligibility caveat is stated plainly.** OpenAI's help page says local stores and restaurants can only claim existing US listings. The script says so in segment 3, the short and the WhatsApp post.
- **Two vendor disclosures.** Claude (segments 6 and 7) is used in this series' writing pipeline, and Higgsfield (segment 15) makes its visuals. Both are disclosed on air.
- **Old or thin launches rejected.** Canva Craft (22 October) is outside the window; Higgsfield Miracle is a waitlist; Alsona has no public prices.
- **The unrendered backlog is now fifteen episodes, nine need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 15
week_of: 2026-11-16
window_covered: 2026-11-09 to 2026-11-16
tools_covered: 8
top_pick: Businesses in ChatGPT
second_pick: Gemini in Gmail
action_item: Claim the business in ChatGPT Business Hub if eligible and record what ChatGPT says today; check Gemini summaries on three long email threads
not_available_in_sa: ChatGPT Wallet (US Pro, US cards), ChatGPT Business Agents (US), Meta Muse phone calls (US paid), Gemini task automation on Pixel 10 (Japan, UK, India)
watch_items: Businesses in ChatGPT local listings outside the US; Fireflies Clips and Scheduler rollout; Dageno South Africa coverage
sa_story: SA AI Index 2026 (93% use, 73% cannot measure value); Google Africa AI lab cohort without an SA startup; Wills & Trust angel round; Africa Tech Festival
content_expiry_date: 2026-11-19
content_expiry_reason: Africa Tech Festival ends and Gemini in Forms reaches Scheduled Release domains
secondary_expiry_reason: SA AI Index full report on 23 November; Skills Scheduled Release on 30 November
fx_rate_used: 16.92
fx_rate_date: 2026-11-16
fx_sources: 3
long_form_runtime_estimate: "12:53"
long_form_words: 2045
long_form_segments: 17
short_runtime_estimate: "1:06"
short_words: 175
short_segments: 5
whatsapp_broadcast_chars: 428
kling_clips: 3
soul_stills_new: 5 (cache absent in repo)
stage_cost_estimate_usd: "3.20 - 7.00"
stage_cost_estimate_zar: "54 - 118"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
series_decision_pending: true
backlog_episodes_unrendered: 15
backlog_episodes_needing_edits: 9 (episodes 6 to 14)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 14, which remain in force.

```
Businesses in ChatGPT and Business Hub, Skills in Google Workspace,
Gemini in Gmail AI Overview and Help me write, Claude Sheets, Claude Whiteboards,
Claude Data, Claude interactive connectors, Claude Meetings, Fireflies Fred,
Fireflies Talk, Fireflies Clips, Fireflies Scheduler, Adobe Firefly Quick Actions,
Build Product Ad, Dageno AI 2.0, ChatGPT Wallet, ChatGPT Business Agents,
Meta Muse phone calls, Gemini Intelligence on Pixel 10, Gemini 4 Hydrogen,
Sheets canvas standalone link, SA AI Index 2026, Google Africa AI lab cohort,
Wills & Trust, Higgsfield Miracle, Alsona, Product Hunt MCP, Databox CLI,
Claude Fable 5.2 allowance offer, Canva Craft
```

Exceptions: re-cover Businesses in ChatGPT if local South African listings open or Business Agents reach South Africa; re-cover ChatGPT Wallet or Meta Muse calls if either reaches South Africa; cover the SA AI Index full report on 23 November if it adds small-business findings; cover the Meta AI Academy SA pitch winners when announced; cover Fireflies Fly when it ships with a price.

### Carried forward for future episodes

- **Claude Duet and 1Password for Agents.** Re-cover if either opens to South Africa or to business accounts.
- **Meta Muse Wonder, Spaces and phone calls.** Re-cover if Meta confirms availability in South Africa.
- **Gemini agent.** Re-cover when small businesses can sign up with a price.
- **ChatGPT Dots texting and Gemini 4 Carbon.** Re-cover when they reach South Africa or businesses.
- **SalesCloser and Empacer.** Re-cover once a standard price is published.
- **ElevenLabs ElevenAI notes and dictation app.** Preview only this week. ElevenLabs is this series' voice vendor; disclose that if it is covered.
- **Wills & Trust.** Re-cover when pricing and launch date are published.

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
