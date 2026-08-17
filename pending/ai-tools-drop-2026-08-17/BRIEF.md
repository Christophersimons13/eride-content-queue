# AI Tools Drop - Production Brief, Week of 10 to 17 August 2026

**Brief ID:** `2026-08-17-ai-tools-drop`
**Product:** AI Tools Drop (weekly series, Eride Technologies)
**Format:** Fully-AI long-form video plus vertical short (Higgsfield Soul -> Kling -> ElevenLabs -> Shotstack)
**Status:** pending - ready for Claude Code execution
**Created by:** Perplexity Computer, scheduled Monday task
**Created at:** 2026-08-17T11:00:00+02:00
**Episode:** 3 of the series

---

## 0. Read this before you spend anything

### THREE UNRENDERED EPISODES ARE NOW STACKED

This is the third brief in a row that has been queued without the previous one rendering.

- `pending/ai-tools-drop-2026-08-03/` - episode 1, not rendered
- `pending/ai-tools-drop-2026-08-10/` - episode 2, not rendered
- `pending/ai-tools-drop-2026-08-17/` - episode 3, this brief

**Do not start episode 3 by default.** Raise the backlog with Michael first and get a direction. The realistic options are:

**A.** Render episode 3 only, and archive episodes 1 and 2 unrendered. The content in them is now one and two weeks stale, and a weekly series that opens with old news reads worse than a series that starts this week.
**B.** Render episode 1 first as the series opener, since it establishes the watermark, end card, disclosure lower-third and palette fragments that every later episode reuses, then decide on 2 and 3.
**C.** Render all three back to back. Roughly R750 to R1,100 in stage costs across the three, and three unpublished episodes to review in one sitting.
**D.** Pause the series render entirely and keep queueing briefs until Michael has a publishing slot. The written article and social pack are already delivered each week and have standalone value.

The reusable-fragment argument favours B. The freshness argument favours A. This is Michael's call, not yours.

### Everything else in this section still applies

**Section 3 sets out the hybrid visual approach that keeps this under about 20 US dollars an episode.** Do not fill fourteen minutes with animated AI clips. Read section 3 before touching a paid endpoint.

**Stage-first gate applies.** Every Shotstack render goes to `stage` first. Nothing renders on `v1` production until Michael has watched the stage output and approved it. Do not skip this. Do not batch a production render to save a round trip.

**The voice decision in section 2 has now gone unanswered for three weeks.** Ask again before generating.

---

## 1. Deliverables

| # | Deliverable | Aspect | Resolution | Duration | Purpose |
|---|---|---|---|---|---|
| A | Long-form episode | 16:9 | 1920x1080, 30fps | 14:00 to 14:30 | YouTube, Facebook, WhatsApp channel |
| B | Vertical short | 9:16 | 1080x1920, 30fps | 75 seconds | TikTok, Reels, Shorts |

**Note the runtime change.** Episodes 1 and 2 targeted 12:30 to 13:00. This week is 14:00 to 14:30 because the week was thin on products, so the script goes deeper on fewer tools rather than padding with irrelevant launches. That is deliberate editorial policy, stated in the cron instruction. Do not trim the script to match the old runtime.

Source content in this folder:

- `script.md` - full narration for deliverable A, segmented with timestamps, on-screen text and b-roll direction. Includes a pronunciation guide and a segment timing table derived from actual word counts.
- `social.md` - narration and overlays for deliverable B, plus all platform captions, the WhatsApp broadcast copy, and a pre-publication fact-check list in section 8.
- `article.md` - the written companion piece. Not needed for the render. Use it only if you need to verify a figure.

---

## 2. ElevenLabs voiceover

**Deliverable A narration:** 2,295 words, roughly 13,000 characters. Concatenate the NARRATION blocks from `script.md` in segment order. Do not include the ON-SCREEN TEXT or B-ROLL blocks. Do not include the pronunciation guide table or the timing table.

**Deliverable B narration:** the NARRATION blocks from section 1 of `social.md`, approximately 195 words.

**Voice ID:** `P1LmKcX63Ihgqy11sVRt` (Andrew, SA male) - same voice as the EMA Reels.

> **Decision outstanding since episode 1, now three weeks old.** Does this series share the EMA voice, or does the AI Tools Drop get its own distinct voice so the two brands do not blur? Ask Michael before generating. If he does not answer, default to the ID above and note in your handoff that the decision is still open.

**Model:** `eleven_multilingual_v2`
**Voice settings:** `stability=0.60, similarity_boost=0.75, style=0.15, use_speaker_boost=true`

**Output:** `mp3_44100_128`

**Pronunciation overrides:** `script.md` contains a pronunciation table. Apply it. This week the tokens that get mangled without it are `Dograh`, `Lettertrace`, `Vizard`, `n8n`, `GLM-5.3`, `Z.ai`, `Zhipu`, `POPIA`, `Xneelo`, `Vapi` and `C2PA`. If your API path does not support phonetic overrides, substitute the phonetic spelling directly into the text input for those tokens only.

**Numbers are written out longhand in the narration on purpose.** The script says "two point three five point zero" rather than "2.35.0", and "twelve sixty" rather than "12.60". Do not convert them back to digits to look tidier. ElevenLabs reads the longhand correctly and mangles the numeric form.

**Pacing check:** target roughly 160 words per minute. If the generated audio comes back shorter than 13:30 or longer than 15:00, stop and report the actual duration rather than adjusting the script yourself. The script header lists the two approved cuts if it overruns 15:00, in order. Apply them only with Michael's go.

**Delivery notes specific to this episode.** Two moments carry the episode:

1. **The cold open, 0:00 to 0:40.** Three short declarative sentences about vendors who cannot price their own products. It must be dry and unhurried, not read as a list. If ElevenLabs rushes it, regenerate the cold open alone with `style` raised to 0.25 and splice.
2. **The Gemini POPIA line at roughly 3:00.** "The free tier is used to improve Google products" is the single most consequential sentence in the episode for a South African business handling client files. It cannot sound like a footnote.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers, same as episodes 1 and 2, but the ratio shifts further toward graphics this week because the episode's spine is a pricing argument rather than a product tour.

**Layer 1 - AI b-roll, 12 Kling clips at 5 seconds each.** About 60 seconds of moving footage. Segment openings and the emotionally loaded moments only. Four fewer than episode 2.

**Layer 2 - Soul stills with slow Ken Burns motion, 6 images.** Shotstack handles pan and zoom, so these cost image generation only.

**Layer 3 - motion graphics and title compositions, generated entirely in Shotstack.** Carries the bulk of the runtime, and more of it than in previous episodes. The three-broken-price-cards composition at 9:40, the mid-call language-switching waveform, the 25 percent adoption bar, the Gemini price-change table, the GitHub-versus-docs version split. No AI generation cost.

Rough runtime split: 60 seconds Layer 1, 60 seconds Layer 2, 740 seconds Layer 3.

**Reuse.** Group B images B1, B2, B3 and B6 from episode 1 are generic and reusable. Do not regenerate them. If they were cached to `assets/ai-tools-drop/` as instructed in episode 1 section 12, pull from there. Also check whether A16 from episode 2, the Johannesburg golden-hour skyline, was generated and cached. If it exists, reuse it for the close rather than generating a new one.

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

### Prompts - 14 new images, plus 4 or 5 reused

**Group A: to be animated by Kling (12 images)**

| # | Segment | Prompt |
|---|---|---|
| A1 | Cold open | Extreme close-up of a laptop screen showing a pricing page in a dark room, the price field visibly blank, cool screen glow on the desk edge, shallow depth of field, editorial technology photography |
| A2 | Why this week | South African small business owner in their forties standing behind a service counter looking at a tablet, late afternoon light, unposed and authentic, editorial documentary photography, diverse |
| A3 | Gemini 3.7 Flash | Close-up of a thick stack of printed documents beside a laptop on a desk, one page lifted mid-turn, cool daylight from the side, editorial detail photography |
| A4 | Gemini POPIA line | Close-up of a manila client file on a desk with a hand resting protectively on the cover, warm desk lamp light, shallow focus on the hand, editorial detail photography |
| A5 | Dograh | Desk telephone handset on a wooden desk in a small South African office, mid-ring, warm morning light through a window, shallow focus, editorial product photography |
| A6 | Dograh SA languages | Two South African people mid-conversation across a reception counter, one gesturing while speaking, warm natural light, editorial documentary photography, authentic and diverse |
| A7 | Dograh use cases | Small beauty salon interior at opening time, one stylist checking a phone at the front desk, chairs empty, warm morning light, editorial documentary photography |
| A8 | BetterClaw | Close-up of a hand holding a bank card above a laptop keyboard, hesitating rather than typing, warm desk light, over-shoulder angle, editorial detail photography |
| A9 | n8n | Close-up of a small server tower under a desk in a home office, single indicator light, cool ambient light, cables neatly routed, editorial technology photography |
| A10 | Lettertrace | Close-up of a search field on a monitor with a cursor blinking in it, dark interface, cool screen glow, tight crop, editorial technology photography |
| A11 | Claude watermark | Close-up of a printed contract page under a raking desk lamp, faint texture visible across the paper grain, warm directional light, editorial detail photography |
| A12 | Close | Wide shot of the Johannesburg skyline at golden hour from a rooftop, Sandton towers visible, warm light deepening, cinematic editorial cityscape. CHECK CACHE FIRST - this may already exist as A16 from episode 2 |

**Group B: Ken Burns stills (2 new, 4 reused from episode 1)**

| # | Use | Prompt |
|---|---|---|
| B9 | Broken pricing pages segment | Overhead of three printed price sheets fanned out on a dark desk, deliberately mismatched layouts, hard directional light casting sharp shadows, editorial flat-lay photography |
| B10 | SA context section | Exterior of a small strip of Johannesburg shopfronts in late afternoon light, awnings and signage, street-level architectural documentary photography |
| B1 | Segment divider | REUSE from episode 1. Do not regenerate. |
| B2 | Segment divider | REUSE from episode 1. Do not regenerate. |
| B3 | Left-out section | REUSE from episode 1. Do not regenerate. |
| B6 | End card backdrop | REUSE from episode 1. Do not regenerate. |

**Expected Soul cost:** 14 new images at roughly 0.09 to 0.15 USD each, so about 1.26 to 2.10 USD. Drops to 13 images if A12 is found in cache.

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
| A1 | very slow push in on the blank price field, screen glow steady, no camera shake |
| A2 | subtle lateral drift past the owner at the counter, natural glance down at the tablet |
| A3 | slow push in on the document stack, the lifted page settling down onto the pile |
| A4 | slow push in on the hand resting on the file cover, light narrowing around it |
| A5 | slow orbit around the ringing handset, warm light sweeping across the receiver |
| A6 | subtle push in on the two people in conversation, natural gestural movement |
| A7 | slow lateral drift across the empty salon, stylist glancing up from the phone |
| A8 | slow push in on the hesitating hand and card above the keyboard, deliberate stillness then a slight withdrawal |
| A9 | slow push in on the server tower, indicator light pulsing gently |
| A10 | slow push in on the search field, cursor blinking, no text appearing |
| A11 | slow raking pass of light across the printed contract, faint pattern emerging then fading |
| A12 | slow cinematic drone drift across the Johannesburg skyline, golden light deepening |

**Expected Kling cost:** 12 clips at roughly 0.75 to 1.20 USD each, so about 9.00 to 14.40 USD.

---

## 6. Shotstack composition

**Endpoint:** `POST https://api.shotstack.io/edit/stage/render`
**Header:** `x-api-key: ${SHOTSTACK_API_KEY_STAGE}`

### Structure for deliverable A

- **Track 1 (base):** the visual bed. Kling clips, Ken Burns stills and solid-colour cards, sequenced to the segment timings in the timing table at the end of `script.md`.
- **Track 2 (graphics):** charts, diagrams and comparison compositions. Carries most of the runtime, and more of it this week than in previous episodes.
- **Track 3 (overlays):** the ON-SCREEN TEXT blocks from `script.md`, timed to their segment ranges.
- **Track 4 (persistent):** series watermark, top-right, roughly 12 percent width, from 0:03 to the end card. Plus the AI disclosure lower-third, see section 8.
- **Soundtrack:** the ElevenLabs MP3, `fadeInFadeOut`.

### Motion graphics specific to this episode

Six graphics carry real explanatory weight this week. Build them properly rather than defaulting to a title card.

1. **0:00 to 0:40 - the three failing price tags.** The cold open is the graphic. Three price tags fade in one at a time. The first collapses to a zero. The second flickers between two conflicting numbers. The third sits next to a get-started-for-free button. This sets up the whole episode and it is the first thing a viewer sees, so it has to be the best-built graphic in the edit.
2. **1:20 - the 25 percent adoption bar.** A horizontal bar filling to 25 percent in accent yellow, then a second muted-grey bar filling to 43 percent below it. Hold on both numbers. Four seconds.
3. **2:40 - the Gemini price-change table.** Two columns, now and from 1 January 2027, with the input and output prices per million tokens. The January column arrives in warning red. Five seconds.
4. **4:10 - the mid-call language switch.** A continuous waveform with a language label above it changing EN to ZU to AF part-way along, without the waveform breaking. This is the single clearest way to show what makes Dograh different, and it needs to be one unbroken waveform. Six seconds.
5. **7:40 - the version disagreement.** Split screen, `GITHUB: 2.35.0` against `DOCS: 2.34`, warning-red divider down the middle. Four seconds.
6. **9:40 to 11:35 - the three broken price cards.** Three cards side by side, each failing in a different way, matching the three tags from the cold open so the episode visually closes its own loop. Then the rule appears full-frame in `style: "future"` with accent yellow on the word RULE. This segment is almost entirely graphics, so budget build time for it.

### Ken Burns on stills

Slow `zoom` or `pan`, 8 to 12 seconds each. Never hold a still frame motionless for more than two seconds.

### Music

Light bed at low mix, with three exceptions:

- **0:00 to 0:40** - the cold open runs voice only. No bed. Let the three sentences sit in silence.
- **11:35 to 12:55** - the Claude watermarking segment runs voice only. Drop the bed completely. Deliberate.
- **13:50 to 14:30** - bring the bed back up slightly under the close and CTA.

### Colour and type

- Background: `#111111`
- Primary text: `#FFFFFF`
- Accent, for prices and key numbers: `#F5C542`
- Negative or warning accent: `#E5533D`

Use `style: "minimal"` for body overlays and `style: "future"` for full-frame title cards.

The Grok Bot cost card in the close segment uses `#E5533D` as the background with white text, held for two and a half seconds. It should be jarring. That is the intent.

### Deliverable B

Rebuild vertically at 1080x1920 using the section 1 narration and overlays from `social.md`. Reuse Kling clips A1, A5, A8 and A4. Try the crop before regenerating anything at 9:16.

The short's hook is a spoken sentence over the failing price tag, and it has to land inside two seconds. No intro card, no logo, no music build. Cut in hard on frame one.

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

Two traps specific to this week:

1. **Rand amounts.** The overlays write rand as `R3,240` and `R16.20`. Keep the plain `R` and the comma. Do not substitute a currency symbol from an extended character set.
2. **Version strings.** `2.35.0` and `2.34` appear in an overlay as digits. That is correct for the overlay. The narration writes them longhand. The two must not be reconciled to match each other.

---

## 8. AI disclosure - mandatory, both deliverables

**On-video:**
- A disclosure lower-third reading `AI-GENERATED VISUALS AND NARRATION` for the first 5 seconds of each deliverable, and again on the end card.
- On the long form, a small persistent corner mark reading `AI-GENERATED` alongside the series watermark.
- On the short, `social.md` calls for a persistent lower-third strip reading `AI-GENERATED VISUALS AND VOICE` for the full 75 seconds. Honour that.

**At upload:**
- YouTube: tick the altered or synthetic content disclosure in the upload flow.
- TikTok: enable the AI-generated content toggle.
- Instagram and Facebook: apply the AI label.

The caption copy in `social.md` already carries a written disclosure line on every platform. Keep it. Do not trim it for length.

**One extra reason to be careful this week.** This episode covers Anthropic's text watermarking and takes a position on AI provenance and client disclosure. An episode arguing that businesses should disclose AI assistance to their clients cannot itself be under-disclosed. Every disclosure element in this section is non-negotiable for this episode in particular.

---

## 9. Execution flow for Claude Code

```
1. Load env vars. Mask to last 4 characters when echoing anything.
   HF_API_KEY, HF_SECRET, ELEVENLABS_API_KEY, SHOTSTACK_API_KEY_STAGE

2. STOP. Read section 0. Three episodes are now queued unrendered.
   Present options A, B, C and D to Michael verbatim and get a direction
   before doing anything else. Do not default to rendering episode 3.

3. Read this brief plus script.md and social.md.
   Show Michael: section 0 (the backlog decision), section 2 (the
   outstanding voice decision, now three weeks old), section 3 (the hybrid
   approach and the reused images), and the cost table in section 10, verbatim.
   WAIT for explicit approval before calling any paid endpoint.

4. After approval, in this order:
   (a) Check assets/ai-tools-drop/ for cached B1, B2, B3, B6 from episode 1
       and A16 from episode 2. Only generate what is genuinely missing.
   (b) Higgsfield Soul: generate the new images. Parallel is fine. Poll each.
       Save all URLs to a manifest file in this folder.
   (c) Higgsfield Kling: animate the 12 Group A images with their matching
       motion prompts. Poll all. Save the 12 video URLs to the manifest.
   (d) ElevenLabs: generate the long-form voiceover from the concatenated
       NARRATION blocks in script.md. Report the actual duration.
       If it falls outside 13:30 to 15:00, STOP and report. Do not edit the
       script. The two approved cuts are listed in the script header and
       require Michael's go.
       Listen back to the cold open and the Gemini POPIA line specifically.
   (e) ElevenLabs: generate the short voiceover from social.md section 1.
   (f) Shotstack ingest: upload both MP3s, get public URLs.
   (g) Run the ASCII check from section 7 over the composed JSON. Fail loudly
       on any non-ASCII byte in a text field.
   (h) Shotstack STAGE render, deliverable A (16:9).
   (i) Shotstack STAGE render, deliverable B (9:16).
   (j) Poll both. Return both stage MP4 URLs to Michael.

5. STOP HERE. Do not render on v1 production.
   Michael watches both stage renders and approves or sends notes.
   Only after his explicit go, re-render both on v1 production.

6. On any Soul or Kling failure, STOP and ask before retrying.
   Do not silently regenerate. Do not alter narration text.
   Do not substitute a different model to work around a failure.
```

---

## 10. Cost breakdown

| Stage | Expected |
|---|---|
| Higgsfield Soul, 14 new images | 1.26 to 2.10 USD |
| Higgsfield Kling, 12 clips at 5s | 9.00 to 14.40 USD |
| ElevenLabs, approximately 13,000 chars long form | about 2.90 USD |
| ElevenLabs, approximately 1,200 chars short | about 0.28 USD |
| Shotstack stage, 2 renders | free within trial credits |
| **Stage total** | **about 13.44 to 19.68 USD** |
| Shotstack v1 production, 2 renders, after approval | per plan |

At roughly R16.20 to the dollar that is about **R218 to R319 per episode** before the production render. Cheaper than episode 2's R265 to R400, from cutting four Kling clips and shifting that runtime onto motion graphics, which suits an episode built around a pricing argument.

**If all three queued episodes are rendered back to back**, the combined stage cost is roughly 47 to 72 USD, about R760 to R1,170. That is the number behind option C in section 0. Show it to Michael before he chooses.

If Michael wants this cheaper still, the lever remains Layer 1. Cutting from 12 Kling clips to 8 saves about 3.50 USD an episode. It is a smaller lever now than it was in episode 2, because most of the fat has already come out. Raise it rather than deciding unilaterally.

---

## 11. Post-render checklist

- [ ] Long form runtime lands between 13:30 and 15:00
- [ ] Narration audio has no clipping, no mispronounced tool names - check `Dograh`, `Lettertrace`, `Vizard`, `n8n`, `GLM-5.3`, `Z.ai`, `Zhipu`, `POPIA`, `Vapi`, `C2PA` specifically
- [ ] Longhand numbers read correctly, particularly "two point three five point zero" and "twelve sixty"
- [ ] The cold open, 0:00 to 0:40, has no music bed and does not sound rushed
- [ ] The Gemini POPIA line at roughly 3:00 lands as a warning, not a footnote
- [ ] The Claude watermarking segment at 11:35 to 12:55 has no music bed
- [ ] The three failing price tags in the cold open visually match the three broken price cards at 9:40, so the loop closes
- [ ] The mid-call language switch waveform at 4:10 is one unbroken waveform, not three cuts
- [ ] The red Grok Bot cost card holds for at least 2 seconds and is legible on a phone
- [ ] All six motion graphics from section 6 are built as graphics, not as plain title cards
- [ ] Every overlay renders as clean ASCII, no mojibake, no missing glyphs
- [ ] Rand amounts render with a plain R and correct comma placement
- [ ] No text wraps mid-word or overflows the safe area
- [ ] Accent colour reads legibly against the dark background on a phone screen
- [ ] AI disclosure lower-third present at open and on the end card, both deliverables
- [ ] Persistent AI disclosure strip runs the full 75 seconds on the short
- [ ] Series watermark persistent on the long form
- [ ] End card holds at least 5 seconds with the WhatsApp channel details legible
- [ ] Short form hook lands inside the first 2 seconds, hard cut on frame one
- [ ] Short form is legible with sound off
- [ ] Michael approves -> move this folder to `approved/`
- [ ] Re-render both on Shotstack v1 production, no watermark
- [ ] Upload with the platform AI disclosure ticked on every platform
- [ ] After posting, move to `published/` with the post links appended below

---

## 12. Series notes

Carried forward and updated:

- The hybrid Layer 1 / 2 / 3 split is what makes weekly long-form economically sane. Do not drift back to fully-animated.
- Group B abstract dividers are reusable. This episode reuses four. Cache them properly in `assets/ai-tools-drop/` if that has still not been done, because three episodes in it would already have paid for itself.
- The palette, watermark, disclosure lower-third and end card should be built once as reusable Shotstack fragments. This is now the third brief to say so. Whichever episode renders first, build them as fragments.
- Segment count and runtime will vary week to week. Episode 3 is longer than 1 and 2 despite covering fewer tools, because a thin week gets depth instead of padding. The composition must tolerate both shapes.
- New note this week: the Kling clip count should follow the content. Product-tour weeks want more b-roll. Argument-driven weeks like this one want more graphics. Twelve is right for this episode and would be wrong for a ten-product week.
- New note this week: `social.md` now carries a section 8 fact-check list flagging the three highest-risk figures to re-verify at publication time. Vendor pricing pages move. Check those three before upload, not before render, because the gap between render and publication is where a figure goes stale.

---

## 13. Metadata

```yaml
brief_id: 2026-08-17-ai-tools-drop
series: ai-tools-drop
episode_number: 3
episode_week: 2026-W34
product: eride-technologies
format: fully_ai_pipeline_longform
backlog_warning: three_episodes_queued_unrendered
backlog_decision_required: true
pipeline_stages:
  - higgsfield_soul_text_to_image
  - higgsfield_kling_image_to_video
  - elevenlabs_tts
  - shotstack_edit_stitch
deliverables:
  - id: A
    aspect_ratio: "16:9"
    resolution: 1920x1080
    target_duration_seconds: 860
    platforms: [youtube, facebook, whatsapp-channel]
  - id: B
    aspect_ratio: "9:16"
    resolution: 1080x1920
    target_duration_seconds: 75
    platforms: [tiktok, instagram-reels, youtube-shorts]
soul_images_new: 14
soul_images_reused: 4
kling_animations: 12
kenburns_stills: 6
narration_words_longform: 2295
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
sa_specific_visuals: true
palette:
  background: "#111111"
  text: "#FFFFFF"
  accent: "#F5C542"
  warning: "#E5533D"
estimated_stage_cost_usd: "13.44-19.68"
estimated_stage_cost_all_three_episodes_usd: "47-72"
usd_zar_rate_used: 16.20
eur_zar_rate_used: 18.75
tools_verified_in_window: 9
top_pick: dograh
second_pick: betterclaw
one_to_avoid: grok-bot
status: pending
created_by: perplexity-computer-scheduled
created_at: 2026-08-17T11:00:00+02:00
```

---

## 14. Post links

Fill in after publishing.

- YouTube:
- Facebook:
- TikTok:
- Instagram Reels:
- WhatsApp channel broadcast sent:
