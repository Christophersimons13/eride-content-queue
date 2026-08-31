# AI Tools Drop - Production Brief, Week of 24 to 31 August 2026

**Brief ID:** `2026-08-31-ai-tools-drop`
**Product:** AI Tools Drop (weekly series, Eride Technologies)
**Format:** Fully-AI long-form video plus vertical short (Higgsfield Soul -> Kling -> ElevenLabs -> Shotstack)
**Status:** pending - ready for Claude Code execution
**Created by:** Perplexity Computer, scheduled Monday task
**Created at:** 2026-08-31T11:00:00+02:00
**Episode:** 4 of the series

---

## 0. Read this before you spend anything

### FOUR UNRENDERED EPISODES ARE NOW STACKED

This is the fourth brief queued in a row without a single one rendering. The 24 August run did not produce a brief at all - the scheduled task failed twice on insufficient credits - so that week is uncovered and this episode absorbs it as a catch-up section.

- `pending/ai-tools-drop-2026-08-03/` - episode 1, not rendered
- `pending/ai-tools-drop-2026-08-10/` - episode 2, not rendered
- `pending/ai-tools-drop-2026-08-17/` - episode 3, not rendered
- `pending/ai-tools-drop-2026-08-31/` - episode 4, this brief

**Do not start episode 4 by default.** Raise the backlog with Michael and get a direction first. Episode 3's brief asked the same question and nothing came back, so ask plainly and wait.

**A.** Render episode 4 only, archive 1 to 3 unrendered. Episode 4 is the cheapest of the four to render, roughly 5.55 to 7.38 USD, and it is the only one whose content is current. Fastest path to a published first episode.
**B.** Render episode 1 first as the series opener, because it establishes the watermark, disclosure lower-third, end card and palette fragments every later episode reuses, then decide on the rest.
**C.** Render all four back to back. Roughly 53 to 80 USD in stage costs, about R862 to R1,289, and four unpublished episodes to review in one sitting.
**D.** Stop rendering entirely and keep queueing briefs. The article and social pack are delivered every week regardless and have standalone value.

The freshness argument now favours **A** more strongly than it did last week, because episode 1's content is four weeks old. The reusable-fragment argument still favours **B**, but those fragments can equally be built during episode 4 and then reused backwards if Michael ever wants the earlier episodes. This remains Michael's call, not yours.

### Everything else in this section still applies

**Section 3 sets out the hybrid visual approach.** This episode is the cheapest of the four because it is argument-driven rather than product-tour, so it only calls for three Kling clips. Do not add more. Read section 3 before touching a paid endpoint.

**Stage-first gate applies.** Every Shotstack render goes to `stage` first. Nothing renders on `v1` production until Michael has watched the stage output and approved it. Do not skip this. Do not batch a production render to save a round trip.

**The voice decision in section 2 has now gone unanswered for four weeks.** Ask again before generating.

---

## 1. Deliverables

| # | Deliverable | Aspect | Resolution | Duration | Purpose |
|---|---|---|---|---|---|
| A | Long-form episode | 16:9 | 1920x1080, 30fps | 14:57 measured | YouTube, Facebook, WhatsApp channel |
| B | Vertical short | 9:16 | 1080x1920, 30fps | 75 seconds | TikTok, Reels, Shorts |

**Runtime is measured, not targeted.** The timing table at the end of `script.md` was built from actual narration word counts at 160 words per minute and the segment headings are in sync with it. Total is 14:57. Do not trim to a rounder number.

Source content in this folder:

- `script.md` - full narration for deliverable A, 16 segments with timecodes, on-screen text and b-roll direction. Includes a pronunciation guide and the measured timing table.
- `social.md` - narration and overlays for deliverable B, plus all platform captions, the WhatsApp broadcast copy, the posting order, and a pre-publication fact-check table in section 8.
- `article.md` - the written companion piece. Not needed for the render. Use it only to verify a figure.

---

## 2. ElevenLabs voiceover

**Deliverable A narration:** 2,393 words, roughly 13,600 characters. Concatenate the NARRATION blocks from `script.md` in segment order. Do not include the ON-SCREEN TEXT or B-ROLL blocks, the pronunciation guide, or the timing table.

**Deliverable B narration:** the NARRATION blocks from section 1 of `social.md`, 196 words.

**Voice ID:** `P1LmKcX63Ihgqy11sVRt` (Andrew, SA male) - same voice as the EMA Reels.

> **Decision outstanding since episode 1, now four weeks old.** Does this series share the EMA voice, or does the AI Tools Drop get its own distinct voice so the two brands do not blur? Ask Michael before generating. If he does not answer, default to the ID above and note in your handoff that the decision is still open.

**Model:** `eleven_multilingual_v2`
**Voice settings:** `stability=0.60, similarity_boost=0.75, style=0.15, use_speaker_boost=true`

**Output:** `mp3_44100_128`

**Pronunciation overrides:** `script.md` carries a pronunciation table. Apply it. The tokens that get mangled without it this week are `Telviva`, `Viva`, `POPIA`, `Jotform`, `x1`, `Screenify`, `ify`, `MCP-Builder`, `Skydive`, `Speko`, `Helply`, `Lightfield`, `Qoder`, `n8n`, `diarization`, `Ling`, `Hy4`, `Expo Go`, `TestFlight` and `MEDDPICC`. If your API path does not support phonetic overrides, substitute the phonetic spelling directly into the text input for those tokens only.

**Two names carry real risk this week.** `ify` must read as "IF-ee" and not as a suffix; the narration deliberately spells it out as "i-f-y" on first mention, keep that. `x1` must read as "eks-ONE" and not as "ex one" or "x-one".

**Numbers are written out longhand in the narration on purpose.** The script says "three point five" rather than "3.5", "eight cents" rather than "R0.08", and "forty-eight thousand rand" rather than "R48,510". Do not convert them to digits to look tidier. ElevenLabs reads the longhand correctly and mangles the numeric form. The overlays use digits. The two must not be reconciled.

**Pacing check:** target roughly 160 words per minute. If the generated audio comes back shorter than 14:00 or longer than 15:45, stop and report the actual duration rather than adjusting the script yourself.

**Delivery notes specific to this episode.** Three moments carry it:

1. **The cold open, 0:00 to 0:28.** Short and declarative. The point is that the week's best launch was South African, not American. It must land flat and confident, not as a tease. If ElevenLabs rushes it, regenerate the cold open alone with `style` raised to 0.25 and splice.
2. **The Gemini free-tier line at roughly 3:20.** That the free tier is used to improve Google's products is the single most consequential sentence in the episode for any South African business handling client audio. It cannot sound like a footnote.
3. **The Helply floor at roughly 12:00.** Forty-eight thousand rand committed before any proof of value. Read it slowly. This is the episode's warning.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers, same structure as episodes 1 to 3, but the ratio shifts further toward graphics than any previous episode. This week's spine is a pricing-transparency argument, and seven of the sixteen segments are explicitly marked "Shotstack only, no Kling needed" in the script.

**Layer 1 - AI b-roll, 3 Kling clips at 5 seconds each.** About 15 seconds of moving footage, down from 12 clips in episode 3. The script calls for exactly three and names them. Do not add a fourth.

**Layer 2 - Soul stills with slow Ken Burns motion.** The script reuses B1, B2, B3 and B6 as segment dividers plus the Johannesburg skyline at open and close. Shotstack handles pan and zoom, so these cost image generation only, and most of them cost nothing because they are cached.

**Layer 3 - motion graphics and title compositions, generated entirely in Shotstack.** Carries the overwhelming bulk of the runtime. The FX-spread table, the Jotform split-screen contradiction, the on-device padlock, the budget bar hitting a hard cap, the 17x model-price bar chart, the ticket counter climbing to 250 against a pinned cost line, and the rapid-fire roundup cards. No AI generation cost.

Rough runtime split: 15 seconds Layer 1, about 70 seconds Layer 2, about 812 seconds Layer 3.

**Reuse - check cache before generating anything.** Group B images B1, B2, B3 and B6 from episode 1 are generic and reusable and are called for by name in the script. Do not regenerate them. If they were cached to `assets/ai-tools-drop/` as instructed in episode 1 section 12, pull from there. Also check for A16 from episode 2, the Johannesburg golden-hour skyline, which this episode uses at both the open and the close. If it exists, reuse it and derive the night variant by grading rather than generating.

**This is now the fourth brief to ask for those fragments to be cached.** If they are not on disk, cache them properly this time.

---

## 4. Higgsfield Soul - image generation

**Endpoint:** `POST https://platform.higgsfield.ai/v1/text2image/soul`
**Auth:** `hf-api-key: ${HF_API_KEY}`

**Body template for 16:9:**
```json
{
  "prompt": "[PROMPT_TEXT]",
  "width_and_height": "2048x1152",
  "quality": "1080p",
  "enhance_prompt": true,
  "batch_size": 1
}
```

For the vertical short, use `"width_and_height": "1152x2048"`.

Poll `GET https://platform.higgsfield.ai/v1/jobs/{id}` until complete.

### Prompts - 3 new images at most, 5 reused

**Group A: to be animated by Kling (3 images)**

| # | Segment | Prompt |
|---|---|---|
| A1 | Telviva Viva, 1:25 | Johannesburg office interior at dusk, a mobile phone face-up on a desk with the screen lighting up, city lights faintly visible through the window behind, shallow depth of field, editorial technology photography |
| A2 | x1, 5:00 | Close-up of two hands holding a phone at a desk, screen showing a partially assembled app interface, warm overhead light, over-shoulder angle, editorial detail photography |
| A3 | MCP-Builder, 8:18 | Close-up along a server rack in a small data centre, neatly routed cables in shallow focus receding into the frame, cool blue ambient light, single indicator light in focus, editorial technology photography |

**Group B: Ken Burns stills - all reused, generate nothing**

| # | Use | Status |
|---|---|---|
| A16 | Cold open and close, Joburg skyline | REUSE from episode 2 if cached. Derive the night variant at the close by grading, not by generating. Only generate fresh if the cache is empty. |
| B1 | Divider, Telviva segment | REUSE from episode 1. Do not regenerate. |
| B2 | Divider, Jotform segment | REUSE from episode 1. Do not regenerate. |
| B3 | Divider, Screenify segment | REUSE from episode 1. Do not regenerate. |
| B6 | Divider, Speko segment | REUSE from episode 1. Do not regenerate. |

**Expected Soul cost:** 3 new images at roughly 0.09 to 0.15 USD each, so about 0.27 to 0.45 USD. Rises to about 0.36 to 0.60 USD if A16 has to be generated because the cache is empty.

---

## 5. Higgsfield Kling - image to video

**Endpoint:** `POST https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video`
**Auth:** `Authorization: Key ${HF_API_KEY}:${HF_SECRET}`

**Body template:**
```json
{
  "image_url": "[SOUL_IMAGE_URL]",
  "prompt": "[MOTION_PROMPT]",
  "duration": 5,
  "aspect_ratio": "16:9"
}
```

**Motion prompts:**

| Image | Motion prompt |
|---|---|
| A1 | very slow push in on the phone as the screen brightens, city lights behind holding steady, no camera shake |
| A2 | slow push in on the hands and phone, interface elements settling into place on the screen, minimal hand movement |
| A3 | slow dolly forward past the server rack, indicator light pulsing gently, cables passing through frame |

**Expected Kling cost:** 3 clips at roughly 0.75 to 1.20 USD each, so about 2.25 to 3.60 USD. This is the cheapest Layer 1 in the series so far and it is correct for this episode. Do not pad it.

---

## 6. Shotstack composition

**Endpoint:** `POST https://api.shotstack.io/edit/stage/render`
**Header:** `x-api-key: ${SHOTSTACK_API_KEY_STAGE}`

### Structure for deliverable A

- **Track 1 (base):** the visual bed. Three Kling clips, Ken Burns stills and solid-colour cards, sequenced to the measured timing table at the end of `script.md`.
- **Track 2 (graphics):** charts, tables and comparison compositions. Carries most of the runtime, and more of it this week than in any previous episode.
- **Track 3 (overlays):** the ON-SCREEN TEXT blocks from `script.md`, timed to their segment ranges.
- **Track 4 (persistent):** series watermark, top-right, roughly 12 percent width, from 0:03 to the end card. Plus the AI disclosure lower-third, see section 8.
- **Soundtrack:** the ElevenLabs MP3, `fadeInFadeOut`.

### Motion graphics specific to this episode

Seven graphics carry real explanatory weight. Build them properly rather than defaulting to a title card.

1. **0:28 to 1:25 - the FX spread table.** The episode opens on an admission that the rand is being quoted four different ways. Build the table row by row, 0.4 seconds apart. XE and Investing.com rows highlight in accent `#F5C542` as they land, because those two agree. The Google Finance row flashes `#E5533D` once, because 17.7101 is the outlier. Final line, `This episode uses 16.17`, scales up 8 percent and holds. This is the first substantive graphic a viewer sees and it establishes that the series shows its working. Build it well.
2. **2:47 to 3:50 - the Gemini free-tier warning.** Waveform animation across the lower third while the price block builds, then the FREE TIER block in `#E5533D` with a 0.3 second shake on entry. VERDICT line holds two seconds.
3. **3:50 to 5:00 - the Jotform contradiction.** Split screen. Left panel labelled `jotform.com/pricing` showing amounts. Right panel labelled `jotform.com/pricing/` with the amounts struck through in `#E5533D`. Hold two seconds on the contradiction. The trailing slash is the whole point, so make it legible on a phone.
4. **6:08 to 7:15 - the double price.** Show `$149` and `$179` side by side, both in `#E5533D`, question mark between them. Hold two seconds. Same tier, two prices, same page.
5. **9:22 to 10:26 - the hard budget cap.** A budget bar filling to full and stopping dead at a cap line with a small `STOP` label. That single animation carries the whole Skydive segment.
6. **10:26 to 11:30 - the 17x model spread.** Two bars only, labelled with the rates, animating the price gap between the cheapest and most expensive model on Speko. Keep it simple. Two bars, not twelve.
7. **11:30 to 12:35 - the Helply floor.** A ticket counter climbing from 0 to 250 while the cost line stays pinned at `$250` the whole way up. This makes the floor obvious without the narration having to explain it twice, and it is the episode's warning graphic. It has to read clearly at phone size.

### Ken Burns on stills

Slow `zoom` or `pan`, 8 to 12 seconds each. Never hold a still frame motionless for more than two seconds.

### Music

Light bed at low mix, with three exceptions:

- **0:00 to 0:28** - the cold open runs voice only. No bed.
- **11:30 to 12:35** - the Helply segment runs voice only. Drop the bed completely. Deliberate.
- **14:42 to 14:57** - bring the bed back up slightly under the close and CTA.

### Colour and type

- Background: `#111111`
- Primary text: `#FFFFFF`
- Accent, for prices and key numbers: `#F5C542`
- Negative or warning accent: `#E5533D`

Use `style: "minimal"` for body overlays and `style: "future"` for full-frame title cards.

### Deliverable B

Rebuild vertically at 1080x1920 using the section 1 narration and overlays from `social.md`. Reuse Kling clips A1 and A2, and the A16 skyline still for the hook. Try the crop before regenerating anything at 9:16.

The short's hook is a spoken sentence over the skyline, and it has to land inside two seconds. No intro card, no logo, no music build. Hard cut on frame one, text on screen by 0:01.

---

## 7. ASCII-safe overlay text - mandatory

**Every string that goes into a Shotstack title asset must be ASCII only.**

- No em dashes or en dashes. Use a plain hyphen.
- No smart or curly quotes. Use straight quotes.
- No curly apostrophes. Use a straight apostrophe.
- No ellipsis character. Use three full stops.
- No emoji, anywhere, ever.
- No degree signs, no middle dots, no non-breaking spaces.

`script.md` and `social.md` are already written ASCII-clean and were checked before this brief was committed. If you generate any additional overlay copy, hold it to the same rule.

**Verify before rendering.** Run the composed JSON through a check for any byte above 0x7F in the text fields and fail loudly if one appears. Non-ASCII characters corrupt in the PowerShell and Windows leg of this pipeline and surface as mojibake in the finished render, which means paying for the render twice.

Three traps specific to this week:

1. **Rand amounts.** The overlays write rand as `R48,510`, `R2,409` and `R0.08`. Keep the plain `R` and the comma. Do not substitute a currency symbol from an extended character set.
2. **The Jotform URLs.** One overlay shows `jotform.com/pricing` against `jotform.com/pricing/`. The trailing slash is the entire content of that graphic. Do not let a linter or a formatter strip it.
3. **Version and model strings.** `2.0`, `3.5`, `3.0` and `x1` appear in overlays as written. The narration says them longhand. Do not reconcile the two.

---

## 8. AI disclosure - mandatory, both deliverables

**On-video:**
- A disclosure lower-third reading `AI-GENERATED VISUALS AND NARRATION` for the first 5 seconds of each deliverable, and again on the end card.
- On the long form, segment 15 is a dedicated full-frame disclosure card in `style: "future"`. It must be on screen for a minimum of five seconds and **must not be cut for runtime**. That instruction is in the script and it is not negotiable.
- On the long form, a small persistent corner mark reading `AI-GENERATED` alongside the series watermark.
- On the short, a persistent lower-third strip reading `AI-GENERATED VISUALS AND VOICE` for the full 75 seconds.

**At upload:**
- YouTube: tick the altered or synthetic content disclosure in the upload flow.
- TikTok: enable the AI-generated content toggle.
- Instagram and Facebook: apply the AI label.

The caption copy in `social.md` already carries a written disclosure line on every platform. Keep it. Do not trim it for length.

**One extra reason to be careful this week.** This episode's central argument is that vendors should publish their prices and state plainly what they do with your data. An episode built on that argument cannot itself be under-disclosed.

---

## 9. Execution flow for Claude Code

```
1. Load env vars. Mask to last 4 characters when echoing anything.
   HF_API_KEY, HF_SECRET, ELEVENLABS_API_KEY, SHOTSTACK_API_KEY_STAGE

2. STOP. Read section 0. FOUR episodes are now queued unrendered.
   Present options A, B, C and D to Michael verbatim and get a direction
   before doing anything else. Do not default to rendering episode 4.

3. Read this brief plus script.md and social.md.
   Show Michael verbatim: section 0 (the four-episode backlog decision),
   section 2 (the voice decision, now four weeks old), section 3 (the
   hybrid approach and the five reused images), and the cost table in
   section 10.
   WAIT for explicit approval before calling any paid endpoint.

4. Before generating anything, re-check the fact-check table in
   social.md section 8. Three entries are time-sensitive: the Vercel
   Ling 3.0 Flash Fin free offer expires 25 September, the Helply
   $250/mo floor and $3,000 annual minimum, and the USD/ZAR rate of
   16.17. If the FX rate has moved more than 3 percent, the rand
   figures in the narration are wrong and must be corrected BEFORE the
   voiceover is generated, not after. Report any change to Michael.

5. After approval, in this order:
   (a) Check assets/ai-tools-drop/ for cached B1, B2, B3, B6 from
       episode 1 and A16 from episode 2. Only generate what is
       genuinely missing. Expect to generate 3 images, not 8.
   (b) Higgsfield Soul: generate A1, A2, A3. Poll each.
       Save all URLs to a manifest file in this folder.
   (c) Higgsfield Kling: animate A1, A2, A3 with their matching motion
       prompts. Three clips only. Poll all. Save URLs to the manifest.
   (d) ElevenLabs: generate the long-form voiceover from the
       concatenated NARRATION blocks in script.md. Report the actual
       duration. If it falls outside 14:00 to 15:45, STOP and report.
       Do not edit the script.
       Listen back to the cold open, the Gemini free-tier line at about
       3:20, and the Helply floor at about 12:00.
       Verify "ify" reads as IF-ee and "x1" reads as eks-ONE.
   (e) ElevenLabs: generate the short voiceover from social.md section 1.
   (f) Shotstack ingest: upload both MP3s, get public URLs.
   (g) Run the ASCII check from section 7 over the composed JSON. Fail
       loudly on any non-ASCII byte in a text field. Confirm the
       jotform.com/pricing trailing slash survived.
   (h) Shotstack STAGE render, deliverable A (16:9).
   (i) Shotstack STAGE render, deliverable B (9:16).
   (j) Poll both. Return both stage MP4 URLs to Michael.

6. STOP HERE. Do not render on v1 production.
   Michael watches both stage renders and approves or sends notes.
   Only after his explicit go, re-render both on v1 production.

7. On any Soul or Kling failure, STOP and ask before retrying.
   Do not silently regenerate. Do not alter narration text.
   Do not substitute a different model to work around a failure.

8. Whatever else happens, cache B1, B2, B3, B6 and A16 to
   assets/ai-tools-drop/ before finishing. This is the fourth brief
   to ask.
```

---

## 10. Cost breakdown

| Stage | Expected |
|---|---|
| Higgsfield Soul, 3 new images | 0.27 to 0.45 USD |
| Higgsfield Kling, 3 clips at 5s | 2.25 to 3.60 USD |
| ElevenLabs, approximately 13,600 chars long form | about 3.05 USD |
| ElevenLabs, approximately 1,250 chars short | about 0.28 USD |
| Shotstack stage, 2 renders | free within trial credits |
| **Stage total** | **about 5.85 to 7.38 USD** |
| Shotstack v1 production, 2 renders, after approval | per plan |

At 16.17 to the dollar that is about **R95 to R119 per episode** before the production render. That is a large drop from episode 3's R218 to R319, and the reason is structural rather than a saving: this episode covers ten tools through pricing arguments and comparison graphics, so it needs three Kling clips instead of twelve and reuses five cached stills. An argument-driven episode is genuinely cheaper to make than a product tour. Worth noting as a series pattern.

**If all four queued episodes are rendered back to back**, the combined stage cost is roughly 53 to 80 USD, about **R862 to R1,289**. That is the number behind option C in section 0. Show it to Michael before he chooses.

There is no meaningful cost lever left to pull on this episode. Three Kling clips is close to the floor for a fourteen-minute video that is not entirely static cards. Do not cut further.

---

## 11. Post-render checklist

- [ ] Long form runtime lands between 14:00 and 15:45
- [ ] Narration audio has no clipping and no mispronounced tool names - check `Telviva`, `Viva`, `POPIA`, `Jotform`, `x1`, `Screenify`, `ify`, `MCP-Builder`, `Skydive`, `Speko`, `Helply`, `Lightfield`, `Qoder`, `n8n`, `diarization`, `Hy4`, `MEDDPICC` specifically
- [ ] `ify` reads as IF-ee, not as a suffix
- [ ] `x1` reads as eks-ONE
- [ ] Longhand numbers read correctly, particularly "three point five" and "forty-eight thousand rand"
- [ ] The cold open, 0:00 to 0:28, has no music bed and does not sound rushed
- [ ] The Gemini free-tier line at about 3:20 lands as a warning, not a footnote
- [ ] The Helply segment, 11:30 to 12:35, has no music bed
- [ ] The FX spread table at 0:28 highlights XE and Investing in accent and flashes Google Finance in warning red
- [ ] The Jotform split screen shows the trailing slash clearly and legibly at phone size
- [ ] The Helply ticket counter climbs to 250 while the cost stays pinned at $250
- [ ] All seven motion graphics from section 6 are built as graphics, not as plain title cards
- [ ] Only three Kling clips appear in the edit
- [ ] Every overlay renders as clean ASCII, no mojibake, no missing glyphs
- [ ] Rand amounts render with a plain R and correct comma placement
- [ ] No text wraps mid-word or overflows the safe area
- [ ] Accent colour reads legibly against the dark background on a phone screen
- [ ] Segment 15, the full-frame AI disclosure card, is present and holds at least 5 seconds
- [ ] AI disclosure lower-third present at open and on the end card, both deliverables
- [ ] Persistent AI disclosure strip runs the full 75 seconds on the short
- [ ] Series watermark persistent on the long form
- [ ] End card holds at least 6 seconds with the WhatsApp channel details legible
- [ ] Short form hook lands inside the first 2 seconds, hard cut on frame one
- [ ] Short form is legible with sound off
- [ ] B1, B2, B3, B6 and A16 cached to `assets/ai-tools-drop/`
- [ ] Fact-check table in `social.md` section 8 re-run immediately before upload, not before render
- [ ] Michael approves -> move this folder to `approved/`
- [ ] Re-render both on Shotstack v1 production, no watermark
- [ ] Upload with the platform AI disclosure ticked on every platform
- [ ] Publish in the order set out in `social.md` section 7: YouTube first, then WhatsApp channel, then Facebook, then TikTok and Reels
- [ ] After posting, move to `published/` with the post links appended below

---

## 12. Series notes

Carried forward and updated:

- The hybrid Layer 1 / 2 / 3 split is what makes weekly long-form economically sane. Do not drift back to fully-animated.
- Group B abstract dividers are reusable. This episode reuses four of them plus the skyline. This is the fourth brief to ask for them to be cached in `assets/ai-tools-drop/`. Four episodes in, that caching would have paid for itself several times over.
- The palette, watermark, disclosure lower-third and end card should be built once as reusable Shotstack fragments. Fourth brief to say so.
- **New note this week, and it is the most useful one so far:** Kling clip count should follow the episode's shape, and the effect on cost is much larger than expected. Episode 3 was argument-driven and used 12 clips at R218 to R319. Episode 4 is also argument-driven, used 3 clips, and costs R95 to R119. Same runtime, same tool count, less than half the cost, and the episode is arguably clearer because the graphics do the explaining. Treat 3 to 5 clips as the default for a pricing or comparison episode and reserve 10-plus for genuine product tours.
- **New note this week:** the fact-check table in `social.md` section 8 now flags time-sensitive items explicitly, including one expiring offer and the FX rate. The FX check moved earlier in the execution flow, to before voiceover generation, because a rand figure baked into narration cannot be corrected without regenerating the audio.
- **New note this week:** the 24 August run failed on insufficient credits and produced nothing. That week is covered as a catch-up section inside episode 4's article rather than as a separate episode. If a run fails again, the following week should absorb it the same way rather than back-filling a stale episode.

---

## 13. Metadata

```yaml
brief_id: 2026-08-31-ai-tools-drop
series: ai-tools-drop
episode_number: 4
episode_week: 2026-W36
product: eride-technologies
format: fully_ai_pipeline_longform
backlog_warning: four_episodes_queued_unrendered
backlog_decision_required: true
missed_run_absorbed: 2026-08-24
pipeline_stages:
  - higgsfield_soul_text_to_image
  - higgsfield_kling_image_to_video
  - elevenlabs_tts
  - shotstack_edit_stitch
deliverables:
  - id: A
    aspect_ratio: "16:9"
    resolution: 1920x1080
    measured_duration_seconds: 897
    platforms: [youtube, facebook, whatsapp-channel]
  - id: B
    aspect_ratio: "9:16"
    resolution: 1080x1920
    target_duration_seconds: 75
    platforms: [tiktok, instagram-reels, youtube-shorts]
soul_images_new: 3
soul_images_reused: 5
kling_animations: 3
narration_words_longform: 2393
narration_words_short: 196
narration_wpm_target: 160
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_voice_decision_pending: true
elevenlabs_settings:
  stability: 0.60
  similarity_boost: 0.75
  style: 0.15
  use_speaker_boost: true
shotstack_environment: stage
production_gate: stage_render_must_be_approved_before_v1
ascii_safe_overlays: required
ai_disclosure: on_video_and_at_upload
dedicated_disclosure_segment: 15
sa_specific_visuals: true
palette:
  background: "#111111"
  text: "#FFFFFF"
  accent: "#F5C542"
  warning: "#E5533D"
estimated_stage_cost_usd: "5.85-7.38"
estimated_stage_cost_all_four_episodes_usd: "53-80"
usd_zar_rate_used: 16.17
usd_zar_no_consensus: true
usd_zar_spread_percent: 9.7
tools_verified_in_window: 10
coverage_incomplete: product_hunt_boards_failed_4_of_7_days
top_pick: telviva-viva
second_pick: gemini-3-5-transcribe-paid-tier
one_to_avoid: helply
best_free_item: vercel-ling-3-0-flash-fin
status: pending
created_by: perplexity-computer-scheduled
created_at: 2026-08-31T11:00:00+02:00
```

---

## 14. Post links

Fill in after publishing.

- YouTube:
- Facebook:
- TikTok:
- Instagram Reels:
- WhatsApp channel broadcast sent:
