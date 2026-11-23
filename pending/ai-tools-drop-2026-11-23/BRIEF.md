# Production Brief - AI Tools Drop, Week of 23 November 2026

**Episode 16.** Prepared for Claude Code. Do not begin a full production render until section 0 is satisfied.

- Source content: `script.md`, `social.md`, `article.md` in this directory
- Long-form runtime target: 12:40 (measured, 2,018 narration words at 160 wpm)
- Short runtime target: 1:03 (measured, 167 narration words)
- 17 segments this week (eight tools, plus a "where your data lives" checklist in segment 13).

---

## 0. Read this before you spend anything

**Backlog warning. This is the sixteenth unrendered episode in `pending/`.**

Checked on 23 November: `pending/` holds fifteen earlier AI Tools Drop directories. `approved/` and `published/` are empty, and `assets/` holds only `brand/`, so `assets/ai-tools-drop/` still does not exist.

| Directory | Week | Age at 23 Nov | Status |
| --- | --- | --- | --- |
| `ai-tools-drop-2026-08-03` | 3 August | 16 weeks | Not rendered |
| `ai-tools-drop-2026-08-10` | 10 August | 15 weeks | Not rendered |
| `ai-tools-drop-2026-08-17` | 17 August | 14 weeks | Not rendered |
| `ai-tools-drop-2026-08-31` | 31 August | 12 weeks | Not rendered |
| `ai-tools-drop-2026-09-07` | 7 September | 11 weeks | Not rendered |
| `ai-tools-drop-2026-09-14` | 14 September | 10 weeks | Not rendered. **Content expired 20 September.** |
| `ai-tools-drop-2026-09-21` | 21 September | 9 weeks | Not rendered. **Content expired 29 September.** |
| `ai-tools-drop-2026-09-28` | 28 September | 8 weeks | Not rendered. **1 October wording is stale.** |
| `ai-tools-drop-2026-10-05` | 5 October | 7 weeks | Not rendered. **Content expired 12 October.** |
| `ai-tools-drop-2026-10-12` | 12 October | 6 weeks | Not rendered. **Eleven v4 line expired 13 October.** |
| `ai-tools-drop-2026-10-19` | 19 October | 5 weeks | Not rendered. **AI Expo Africa "upcoming" line expired 28 October.** |
| `ai-tools-drop-2026-10-26` | 26 October | 4 weeks | Not rendered. **Segment 11 "tomorrow" and "Friday" lines expired 27 to 30 October.** |
| `ai-tools-drop-2026-11-02` | 2 November | 3 weeks | Not rendered. **Meta AI Academy line needs a recheck; Gemini Slides promo limits end 1 December.** |
| `ai-tools-drop-2026-11-09` | 9 November | 2 weeks | Not rendered. **Forms line expired 19 November; Afda course and Meta AI Academy summit lines expire 24 November.** |
| `ai-tools-drop-2026-11-16` | 16 November | 1 week | Not rendered. **Africa Tech Festival and Forms lines expired 19 November; SA AI Index "lands on the twenty-third" expires today; Meta summit 24 to 25 November; Skills Scheduled Release 30 November.** |
| `ai-tools-drop-2026-11-23` | 23 November | Current | This brief |

Ten earlier episodes (6 to 15) now need content edits before they could be published. Michael has been asked whether to keep the series running, pause it or stop it. **No answer yet. Do not render any episode, including this one, without his written choice.**

**Time-limited items in this episode.**

| Item | Date | Consequence if publication slips past it |
| --- | --- | --- |
| Creatify Max "before Black Friday" | **27 November 2026** | Segment 8 opening line. After that, cut "before Black Friday". |
| Google Vids Assets Scheduled Release start | **2 December 2026** | Article only. |
| ChatGPT Standard and Advanced voice retire | **11 December 2026** | Segment 14. After that, cut the line. |
| Gems to skills, Business and Enterprise | **No sooner than 1 March 2027** | Segment 14. |
| HCode launch code HCODEFREE2026 | No end date published | Segments 3 and 17, short segment 2, WhatsApp post. Recheck the code still works before render. |
| ChatGPT Space reaching Plus accounts; pricing page still showed "not on Plus" | Any day | Segment 10. Recheck before render; if the pricing page now lists Space on Plus, cut that sentence. |
| Live Dictation "rolling out gradually" | Any day | Segment 4. |
| R100m AI fund, proposal only | Any day | Segment 12. If an application process is announced, update the line. |

**Stage-first production gate.** Every render in this brief goes to the Shotstack **stage** endpoint first. A human inspects the stage output. Only after written approval does anything go to a production render. This applies per episode, not once for the series.

**Do not skip the gate to clear the backlog faster.** The backlog is a decision problem, not a throughput problem.

**Editorial note.** Segment 15 mentions Kling Image 4.0, a new model from the vendor that makes this series' animated clips. That is editorial content, not a pipeline instruction. **Keep the Kling v2.1 endpoint in section 5 for this episode.** Any model or vendor change is Michael's decision, and would need its own stage test and cost check.

**Self-disclosure notes.** Segment 3 says the writing pipeline uses Claude models (HCode's instructions use Claude as the example). Segment 15 says Kling makes the clips and Anthropic makes Claude. Do not cut any of these sentences for time. Segment 7's consent sentence also stays.

---

## 1. Deliverables

| ID | Format | Spec | Runtime | Destination |
| --- | --- | --- | --- | --- |
| A | Long form 16:9 | 1920x1080, 30fps, H.264, AAC | 12:40 | YouTube, Facebook native, WhatsApp channel |
| B | Vertical short 9:16 | 1080x1920, 30fps, H.264, AAC | 1:03 | TikTok, Instagram Reels, YouTube Shorts |

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

**Voice direction.** Warm, measured, South African English. Conversational, not presenter-bright. No hype, no rising sales cadence. Slight slowdown on every caveat line ("The catches", "What I could not confirm", "The asterisk"). Those lines are the series' credibility and must not be rushed.

**Pronunciation guide is in the script header.** This week's high-risk tokens: `HCode` (aitch-code), `HOSTAFRICA` (host-AF-rih-kuh), `Xero` (ZEER-oh), `SARS` (said as a word), `Creatify` (kree-AT-ih-fy), `Bluedot`, `Zoho` (ZOH-hoh), `Ramaphosa` (rah-mah-POH-sah), `CAPEability` (cape-uh-BIL-ih-tee), `eCentres`, `POPIA` (poh-PEE-uh) and `Gemini four Neon`. Listen to segments 3, 5, 8, 11 and 12 first. If a name fails twice, use the respelling in the narration text for that segment only and flag it in the stage report.

**Numbers are written longhand in the narration deliberately** and as digits in the overlays. Do not reconcile the two.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers.

**Layer 1 - Kling motion clips, 5 seconds each.** Three clips this week, K1 to K3.

**Layer 2 - Higgsfield Soul stills with Ken Burns motion.** Reuse the cached images once they exist. No new stills this week.

**Layer 3 - Shotstack motion graphics.** The bulk of the runtime.

Rough split by runtime: Kling about 15 seconds, Soul stills about 2.5 minutes, Shotstack the remainder.

**Third-party product footage.** Where the script asks for a screen recording of HCode, ChatGPT, Canva, Bluedot, Creatify or Gemini, record it yourself or use a Shotstack mock-up. Never use the vendors' marketing videos. Do not show any real client data, bank statements or phone numbers.

---

## 4. Higgsfield Soul - image generation

**Cached assets. Reuse, do not regenerate.** Expected in `assets/ai-tools-drop/`: `B1` (abstract data-flow field), `B2` (desk workspace, low light), `B3` (abstract network mesh), `B6` (dusk cityscape, warm), `A16` (Johannesburg skyline).

**Sixteenth brief asking for this cache. Checked on 23 November: it does not exist.** Generate the five stills once, commit them to that path, and every later episode stops paying for them.

| Asset | Segment | Motion |
| --- | --- | --- |
| B1 | 2 (dimmed), 14 (dimmed) | Slow push in |
| B2 | 4, 8 (dimmed), 10 | Ken Burns, slow push in |
| B3 | 5, 13 (dimmed) | Ken Burns, slow drift, cool grade |
| B6 | 6, 12 (library item) | Ken Burns, warm |
| A16 | 12 (fund item), 17 (Close), short segment 5 | Slow push in; push out and fade on the close |

The script text names some stills by subject; the cached B-series are abstract. Use the cached asset regardless. Do not generate new stills to match the script wording.

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
| K1 | 1 - Cold open, short segment 2 | A laptop on a kitchen table in warm morning light, an abstract app layout on screen, slow push in. No readable text, no logos, no people. |
| K2 | 4 - Live Dictation, short segment 3 | A person walking on a seaside promenade, talking into a phone, seen from behind, abstract text shapes on screen. No readable text, no logos, no identifiable face. |
| K3 | 7 - Bluedot | A person on a phone call at a desk, seen from behind, abstract note shapes appearing on a second screen. No readable text, no logos, no identifiable face. |

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
- **Uncertain or negative items render in `warning`, not accent.** This episode: "Announcement issued by HOSTAFRICA" in segment 3; "Test it with your own accent" in segment 4; "Sage: not listed" in segment 5; "Outgoing only. SA numbers: test first" and "Turn the consent message ON" in segment 7; "Viewers need a paid account" and "No public links yet" in segment 10; all four lines in segment 11; "proposed, no process yet" and "under half see measurable returns" in segment 12; "No answer? Keep client data out." in segment 13.
- **Segment 3:** the chat and published-page screens are our own recording or a mock-up. No HOSTAFRICA logo unless taken from our own screen recording.
- **Segment 5:** the reconciliation table is a generic mock-up with invented figures. No real bank, client or company names.
- **Segment 13:** a four-line numbered checklist, ASCII only. Align with spaces, not tabs. No arrow glyphs.
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

**Protected strings.** `R50/month`, `HCODEFREE2026`, `$14 (about R246)`, `$10/month (about R176)`, `R100m`, `83 eCentres, 375 libraries`, `18+`, `11 Dec`, `1 Mar 2027`, `Profile > Settings > Permissions` and `R17.56 / USD` must survive exactly. The `>` characters in the Canva path are plain greater-than signs, not arrows. `+` in `AI VOICE + AI VISUALS` is a plain plus sign.

---

## 8. AI disclosure - mandatory, both deliverables

**Deliverable A:** SEGMENT 16, from 11:22 to 11:48. Static card, `#111111` background, white text, no motion.

**Deliverable B:** persistent corner caption for the full 1:03, reading exactly `AI VOICE + AI VISUALS`. Top-right, 60 percent opacity, minimum 3 percent of frame height, never inside 12 percent of any edge.

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
3. **Check the date** against the section 0 table, and recheck the HCode launch code, ChatGPT Space on Plus and the R100m fund status. Edit before rendering.
4. Run `ascii_fix.py` across all four files. Confirm four `OK` lines and that the protected strings in section 7 survived.
5. Confirm `assets/ai-tools-drop/` contains B1, B2, B3, B6 and A16. **It did not exist on 23 November.** Generate once and commit.
6. Render narration: 17 ElevenLabs calls for A, 5 for B, into `audio/`.
7. Listen to segments 3, 5, 8, 11 and 12 first for names and figures. Re-render individual segments as needed.
8. Measure actual audio durations. **Rebuild the timing table and the YouTube chapters from rendered audio.**
9. Render the three Kling clips to stage and inspect each.
10. Build and submit the Shotstack **stage** payload for A, then B.
11. **Stop. Report both stage URLs and the recomputed cost. Wait for written approval before any production render.**
12. On approval: production render, then section 11.

---

## 10. Cost breakdown

| Item | Quantity | Estimate USD |
| --- | --- | --- |
| ElevenLabs narration | approx 12,200 characters across both deliverables | $1.25 - $1.80 |
| Higgsfield Soul stills | 5 cached-set stills (cache absent) | $0.00 - $1.50 |
| Higgsfield Kling clips | 3 clips at 5 seconds | $1.95 - $2.70 |
| Shotstack stage renders | 4 (two per deliverable) | $0.00 - $1.00 |
| **Episode 16 stage total** | | **$3.20 - $7.00** |

At R17.56 that is roughly **R56 to R123**.

**Sixteen-episode combined stage cost, if all sixteen are rendered: approximately $99.80 to $174.25, or about R1,753 to R3,060 at R17.56.** Production renders are additional, typically two to three times stage cost. The weaker rand adds about R64 to R112 to the backlog's rand cost compared with last week's rate.

---

## 11. Post-render checklist

- [ ] Disclosure card visible and legible for at least five seconds in deliverable A
- [ ] Persistent `AI VOICE + AI VISUALS` caption legible for the full duration of deliverable B
- [ ] No mojibake or replacement characters anywhere in either video
- [ ] Protected strings in section 7 render correctly on screen
- [ ] No HOSTAFRICA, OpenAI, Canva, Bluedot, Creatify, Google, Xero, Zoho, Microsoft or WhatsApp logos in any generated footage
- [ ] Any screen recording of a third-party product is our own recording, with no real client data
- [ ] No overlay text clipped, wrapped mid-word, or inside 12 percent of any edge, checked on the 9:16 crop specifically
- [ ] Audio levels consistent, no clipping, no dead air over two seconds
- [ ] Short is at least 60 seconds as rendered (measured 1:03, so check it carefully)
- [ ] YouTube chapters rebuilt from rendered audio durations
- [ ] Every uncertain or negative item in the warning colour per section 6
- [ ] Section 0 dated items still accurate
- [ ] `[LINK]` placeholder replaced, broadcast re-counted, still under 700 characters (currently 413 with the placeholder)
- [ ] Platform AI-generated toggle set at upload on YouTube, TikTok, Instagram, Facebook
- [ ] Section 14 updated with live post links

---

## 12. Series notes

- **A rare local top pick.** HCode is South African, billed in rand and hosts in South Africa by default. The announcement was issued by HOSTAFRICA itself; the script says so.
- **A data-handling thread.** The accounting plugin, Bluedot call recording and self-built apps all touch client personal information. Segment 13 turns that into three POPIA-minded questions rather than a pitch for any tool.
- **Three vendor disclosures.** Claude (segment 3, via HCode's instructions), Kling (segment 15) and Anthropic (segment 15). All are disclosed on air.
- **Old or thin launches rejected.** Gemini brand styles (Google post dated 20 October) is outside the window; Office in Copilot has no plans or prices; Claude computer use is Team and Enterprise only.
- **The unrendered backlog is now sixteen episodes, ten need edits.** Raise it every episode until it is answered.

---

## 13. Metadata

```yaml
series: AI Tools Drop
episode: 16
week_of: 2026-11-23
window_covered: 2026-11-16 to 2026-11-23
tools_covered: 8
top_pick: HCode by HOSTAFRICA
second_pick: ChatGPT Live Dictation
action_item: Publish one internal tool on HCode with the free two months and no client data; dictate one long brief with Live Dictation and count corrections
not_available_in_sa: Free Tasks in Gemini (6 countries), Zoho Desk Blended Agents, ChatGPT Health (US), Gemini Mac computer use (US first), Gemini GIFs
watch_items: HCode launch code; ChatGPT Space on Plus; Bluedot country support; Xero ChatGPT integration outside the US; R100m fund application process
sa_story: Proposed R100m AI venture fund; CAPEability AI in Western Cape libraries and eCentres; SA AI Index coverage
content_expiry_date: 2026-11-27
content_expiry_reason: Black Friday reference in segment 8
secondary_expiry_reason: ChatGPT voice retirement on 11 December
fx_rate_used: 17.56
fx_rate_date: 2026-11-23
fx_sources: 3
long_form_runtime_estimate: "12:40"
long_form_words: 2018
long_form_segments: 17
short_runtime_estimate: "1:03"
short_words: 167
short_segments: 5
whatsapp_broadcast_chars: 413
kling_clips: 3
soul_stills_new: 5 (cache absent in repo)
stage_cost_estimate_usd: "3.20 - 7.00"
stage_cost_estimate_zar: "56 - 123"
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
render_status: not_started
production_gate: stage_render_requires_human_approval
series_decision_pending: true
backlog_episodes_unrendered: 16
backlog_episodes_needing_edits: 10 (episodes 6 to 15)
```

### Exclusion list for next week

Do not re-cover any of the following. This extends the lists in episodes 5 to 15, which remain in force.

```
HCode, ChatGPT Live Dictation, ChatGPT Accounting plugin, Xero ChatGPT integration,
Canva AI controls, Bluedot phone calls, Bluedot 2.2, Creatify Max,
Gemini Notebook interactive sites, ChatGPT Space, Tasks in Gemini free tier,
Zoho Desk Blended Agents, ChatGPT Health, Gemini Mac computer use, Gemini GIFs,
R100m AI venture fund, CAPEability AI, Gems to skills transition, Google Vids Assets,
Gemini 4 Neon, Kling Image 4.0, Anthropic IPO, Office in Copilot,
Gemini business tools and brand styles, Claude computer use, GPT-6.2 Astra and Sol
```

Exceptions: re-cover Tasks in Gemini or Zoho Blended Agents if either reaches South Africa; re-cover the R100m fund when an application process is published; re-cover ChatGPT Space when public links or free viewing arrive; re-cover Office in Copilot when Microsoft publishes plan names and prices; cover the Meta AI Academy SA pitch winners when announced; cover the SA AI Index full report if it adds small-business findings.

### Carried forward for future episodes

- **Claude Duet and 1Password for Agents.** Re-cover if either opens to South Africa or to business accounts.
- **Meta Muse Wonder, Spaces and phone calls.** Re-cover if Meta confirms availability in South Africa.
- **Gemini agent.** Re-cover when small businesses can sign up with a price.
- **ChatGPT Dots texting and Gemini 4 Carbon.** Re-cover when they reach South Africa or businesses.
- **SalesCloser (including its 17 November Shopify live video agent) and Empacer.** Re-cover once a standard price is published.
- **ElevenLabs ElevenAI notes and dictation app, and ElevenLabs video ad variants.** ElevenLabs is this series' voice vendor; disclose that if either is covered.
- **Wills & Trust.** Re-cover when pricing and launch date are published.
- **HighLevel AI visibility tool and Meeting AI notetaker.** Private beta this week; re-cover at general release with a price.

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
