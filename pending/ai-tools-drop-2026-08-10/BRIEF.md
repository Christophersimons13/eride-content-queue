# AI Tools Drop - Production Brief, Week of 4 to 10 August 2026

**Brief ID:** `2026-08-10-ai-tools-drop`
**Product:** AI Tools Drop (weekly series, Eride Technologies)
**Format:** Fully-AI long-form video plus vertical short (Higgsfield Soul -> Kling -> ElevenLabs -> Shotstack)
**Status:** pending - ready for Claude Code execution
**Created by:** Perplexity Computer, scheduled Monday task
**Created at:** 2026-08-10T11:00:00+02:00
**Episode:** 2 of the series

---

## 0. Read this before you spend anything

This is episode 2. Episode 1 is at `pending/ai-tools-drop-2026-08-03/` and its brief is the template. Read section 12 of that brief before starting, because several assets from it are reusable and regenerating them wastes money.

**Section 3 sets out the hybrid visual approach that keeps this under about 25 US dollars an episode.** Do not fill thirteen minutes with animated AI clips. Read section 3 before touching a paid endpoint.

**Stage-first gate applies.** Every Shotstack render goes to `stage` first. Nothing renders on `v1` production until Michael has watched the stage output and approved it. Do not skip this. Do not batch a production render to save a round trip.

**Two open items carried over from episode 1:**
1. The voice decision in section 2 was never answered. Ask again before generating.
2. If episode 1 has not yet rendered, resolve it before starting episode 2. Two half-finished episodes is worse than one finished one.

---

## 1. Deliverables

| # | Deliverable | Aspect | Resolution | Duration | Purpose |
|---|---|---|---|---|---|
| A | Long-form episode | 16:9 | 1920x1080, 30fps | 12:30 to 13:00 | YouTube, Facebook, WhatsApp channel |
| B | Vertical short | 9:16 | 1080x1920, 30fps | 75 seconds | TikTok, Reels, Shorts |

Source content in this folder:

- `script.md` - full narration for deliverable A, segmented with timestamps, on-screen text and b-roll direction. Includes a pronunciation guide.
- `social.md` - narration and overlays for deliverable B, plus all platform captions and the WhatsApp broadcast copy.
- `article.md` - the written companion piece. Not needed for the render. Use it only if you need to verify a figure.

---

## 2. ElevenLabs voiceover

**Deliverable A narration:** approximately 1,950 words, roughly 11,000 characters. Concatenate the NARRATION blocks from `script.md` in segment order. Do not include the ON-SCREEN TEXT or B-ROLL blocks. Do not include the pronunciation guide table.

**Deliverable B narration:** the NARRATION blocks from section 1 of `social.md`.

**Voice ID:** `P1LmKcX63Ihgqy11sVRt` (Andrew, SA male) - same voice as the EMA Reels.

> **Decision still outstanding from episode 1.** Does this series share the EMA voice, or does the AI Tools Drop get its own distinct voice so the two brands do not blur? Ask Michael before generating. If he does not answer, default to the ID above and note in your handoff that the decision is still open.

**Model:** `eleven_multilingual_v2`
**Voice settings:** `stability=0.60, similarity_boost=0.75, style=0.15, use_speaker_boost=true`

**Output:** `mp3_44100_128`

**Pronunciation overrides:** `script.md` contains a pronunciation table. Apply it. This week `Aveiro`, `Rindler`, `Wispr`, `Qwen`, `n8n` and `POPIA` all get mangled without it. If your API path does not support phonetic overrides, substitute the phonetic spelling directly into the text input for those tokens only.

**Pacing check:** target roughly 150 words per minute. If the generated audio comes back shorter than 12:00 or longer than 13:30, stop and report the actual duration rather than adjusting the script yourself.

**Delivery note specific to this episode.** The Meta Muse Code segment at 9:45 contains a hard warning about data use. Do not let the voice race through it. If ElevenLabs delivers it flat, regenerate that segment alone with `style` raised to 0.25 and splice it. That is the one moment in the episode that must land.

---

## 3. Visual approach - the hybrid that makes this affordable

Three layers, same as episode 1:

**Layer 1 - AI b-roll, 16 Kling clips at 5 seconds each.** About 80 seconds of moving footage. Segment openings and the emotionally loaded moments only. Two fewer than episode 1 because this week leans harder on charts and comparison graphics.

**Layer 2 - Soul stills with slow Ken Burns motion, 6 images.** Shotstack handles pan and zoom, so these cost image generation only.

**Layer 3 - motion graphics and title compositions, generated entirely in Shotstack.** Carries the bulk of the runtime. Price cards, the USD to ZAR line chart, the permission-model animation, the pricing-contradiction comparison, the Rindler payback calculator. No AI generation cost.

Rough runtime split: 80 seconds Layer 1, 60 seconds Layer 2, 640 seconds Layer 3.

**Reuse from episode 1.** Group B images B1, B2, B3 and B6 from `pending/ai-tools-drop-2026-08-03/` are generic and reusable. Do not regenerate them. If they were cached to `assets/ai-tools-drop/` as section 12 of that brief recommended, pull from there. That drops this week's Soul count by four.

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

### Prompts - 18 new images, plus 4 reused

**Group A: to be animated by Kling (16 images)**

| # | Segment | Prompt |
|---|---|---|
| A1 | Cold open | Close-up of a laptop screen in a dim Johannesburg home office at dawn, a chat interface visible, warm lamp light on the keyboard, shallow depth of field, editorial photography, muted professional tones |
| A2 | Why this week | South African founder in their thirties at a kitchen table with a laptop and a coffee, early morning light through a window, unposed and authentic, editorial documentary photography |
| A3 | ChatGPT | Small office with three people at desks, one visibly waiting and looking at a stalled screen, natural daylight, editorial workplace photography, diverse South African team |
| A4 | ChatGPT | Close-up of a hand cancelling a subscription on a laptop screen, warm desk light, over-shoulder angle, shallow focus, editorial detail photography |
| A5 | ElevenLabs | Close-up of a professional microphone on a desk in a small home studio, acoustic foam softly out of focus behind, warm directional light, editorial product photography |
| A6 | ElevenLabs | Two people in conversation across a desk in a South African consulting office, one gesturing while explaining, warm natural light, editorial documentary style, authentic and diverse |
| A7 | Keystroke | Close-up of a code editor on a large monitor in a dark room, syntax highlighting visible, blue screen glow on the desk surface, editorial technology photography |
| A8 | Aveiro | Overhead of a desk with a printed newsletter, a laptop showing a blog layout and a coffee cup, warm morning light, editorial flat-lay photography |
| A9 | AdAnt | Smartphone on a tripod filming a cosmetic product on a small lit stand, behind-the-scenes content shoot, warm studio light, editorial photography |
| A10 | Wispr | Laptop open on a table during a video call, four participant tiles visible on screen, warm afternoon light through a window, over-shoulder angle, editorial photography |
| A11 | Cloudflare OS | Close-up of a series of physical locks on a steel door, shallow focus receding down the row, cool industrial light, conceptual editorial photography |
| A12 | Cloudflare OS | Server rack interior in a clean data centre, blue and white indicator lights, long corridor perspective, cool tones, architectural technology photography |
| A13 | Muse Code | Terminal window filling a large monitor in a dark room, dense scrolling text, green and white on black, close crop, editorial technology photography |
| A14 | Muse Code | Close-up of a printed confidentiality agreement on a desk with a pen resting on it, warm desk lamp light, shallow focus on the heading, editorial detail photography |
| A15 | Rindler | Close-up of a government service portal login page on a monitor in a busy office, fluorescent overhead light, slightly worn desk, editorial documentary photography |
| A16 | Closing | Wide shot of the Johannesburg skyline at golden hour from a rooftop, Sandton towers visible, warm light deepening, cinematic editorial cityscape |

**Group B: Ken Burns stills (2 new, 4 reused from episode 1)**

| # | Use | Prompt |
|---|---|---|
| B7 | Omniwork segment | Overhead of a cluttered desk with five different open notebooks and devices, warm daylight, deliberately busy composition, editorial photography |
| B8 | Local news section | Exterior of a modern Sandton corporate office tower, glass and steel, blue hour light, architectural photography |
| B1 | Segment divider | REUSE from episode 1. Do not regenerate. |
| B2 | Segment divider | REUSE from episode 1. Do not regenerate. |
| B3 | Left-out section | REUSE from episode 1. Do not regenerate. |
| B6 | End card backdrop | REUSE from episode 1. Do not regenerate. |

**Expected Soul cost:** 18 new images at roughly 0.09 to 0.15 USD each, so about 1.60 to 2.70 USD.

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
| A1 | slow push in on the laptop screen, dawn light strengthening across the keyboard |
| A2 | slow lateral drift past the founder at the kitchen table, steam rising from the coffee |
| A3 | subtle push in on the person waiting at the stalled screen, others working normally around them |
| A4 | slow push in on the hand and cursor completing the cancellation, deliberate movement |
| A5 | slow orbit around the microphone, directional light catching the grille |
| A6 | subtle push in on the two people in conversation, natural gestural movement |
| A7 | slow lateral drift across the code editor, text scrolling gently upward |
| A8 | slow overhead descent onto the desk, soft light shifting across the printed newsletter |
| A9 | slow orbit around the product on the lit stand, phone recording in frame |
| A10 | subtle push in on the video call grid, natural participant movement in the tiles |
| A11 | slow dolly along the row of locks, focus racking from the nearest to the furthest |
| A12 | slow dolly forward down the server corridor, indicator lights pulsing gently |
| A13 | slow push in on the terminal, text scrolling rapidly then slowing |
| A14 | slow push in onto the confidentiality agreement heading, warm light narrowing |
| A15 | slow push in on the portal login page, cursor moving into the username field |
| A16 | slow cinematic drone drift across the Johannesburg skyline, golden light deepening |

**Expected Kling cost:** 16 clips at roughly 0.75 to 1.20 USD each, so about 12.00 to 19.20 USD.

---

## 6. Shotstack composition

**Endpoint:** `POST https://api.shotstack.io/edit/stage/render`
**Header:** `x-api-key: ${SHOTSTACK_API_KEY_STAGE}`

### Structure for deliverable A

- **Track 1 (base):** the visual bed. Kling clips, Ken Burns stills and solid-colour cards, sequenced to the segment timings in `script.md`.
- **Track 2 (graphics):** charts, diagrams and comparison compositions. Carries most of the runtime.
- **Track 3 (overlays):** the ON-SCREEN TEXT blocks from `script.md`, timed to their segment ranges.
- **Track 4 (persistent):** series watermark, top-right, roughly 12 percent width, from 0:03 to the end card. Plus the AI disclosure lower-third, see section 8.
- **Soundtrack:** the ElevenLabs MP3, `fadeInFadeOut`.

### Motion graphics specific to this episode

Five graphics carry real explanatory weight this week. Build them properly rather than defaulting to a title card.

1. **1:00 - USD to ZAR line chart.** Simple line falling from 16.50 to 16.13 across the week. Label the two endpoints only. Four seconds.
2. **2:00 - the cap comparison.** A bar that fills and hits a hard ceiling labelled OLD, beside a bar that fills and keeps going labelled NEW. Six seconds.
3. **9:00 - the permission model.** A central agent node ringed by greyed-out capability tiles, each lighting up individually as a tick is applied. This is the clearest way to explain capability-based security. Eight seconds.
4. **11:00 - the pricing contradiction.** Two quoted strings side by side, both highlighted in accent yellow, a question mark between them. Five seconds.
5. **12:00 - the Rindler payback calculator.** Hours saved multiplied by an hourly rate, resolving against a horizontal R1620 line. Six seconds.

### Ken Burns on stills

Slow `zoom` or `pan`, 8 to 12 seconds each. Never hold a still frame motionless for more than two seconds.

### Music

Light bed at low mix, with two exceptions:

- **9:45 to 10:45** - the Meta Muse Code warning segment runs voice only. Drop the bed completely. Deliberate.
- **12:20 to 13:00** - bring the bed back up slightly under the close and CTA.

### Colour and type

- Background: `#111111`
- Primary text: `#FFFFFF`
- Accent, for prices and key numbers: `#F5C542`
- Negative or warning accent: `#E5533D`

Use `style: "minimal"` for body overlays and `style: "future"` for full-frame title cards.

The full-frame warning card at 10:20 uses `#E5533D` as the background with white text, held for two and a half seconds. It should be jarring. That is the intent.

### Deliverable B

Rebuild vertically at 1080x1920 using the section 1 narration and overlays from `social.md`. Reuse Kling clips A1, A4, A5 and A13. Try the crop before regenerating anything at 9:16.

---

## 7. ASCII-safe overlay text - mandatory

**Every string that goes into a Shotstack title asset must be ASCII only.**

- No em dashes or en dashes. Use a plain hyphen.
- No smart or curly quotes. Use straight quotes.
- No curly apostrophes. Use a straight apostrophe.
- No ellipsis character. Use three full stops.
- No emoji, anywhere, ever.
- No degree signs, no middle dots, no non-breaking spaces.

`script.md` and `social.md` are already written ASCII-clean. If you generate any additional overlay copy, hold it to the same rule.

**Verify before rendering.** Run the composed JSON through a check for any byte above 0x7F in the text fields and fail loudly if one appears. Non-ASCII characters corrupt in the PowerShell and Windows leg of this pipeline and surface as mojibake in the finished render, which means paying for the render twice.

Note one trap specific to this week. The narration says "sixty two percent" and the overlays say "62 pct". Do not let an editor helpfully convert "pct" to a percent sign in a context where the font may not carry it cleanly. Leave it as written.

---

## 8. AI disclosure - mandatory, both deliverables

**On-video:**
- A disclosure lower-third reading `AI-GENERATED VISUALS AND NARRATION` for the first 5 seconds of each deliverable, and again on the end card.
- On the long form, a small persistent corner mark reading `AI-GENERATED` alongside the series watermark.

**At upload:**
- YouTube: tick the altered or synthetic content disclosure in the upload flow.
- TikTok: enable the AI-generated content toggle.
- Instagram and Facebook: apply the AI label.

The caption copy in `social.md` already carries a written disclosure line. Keep it. Do not trim it for length.

---

## 9. Execution flow for Claude Code

```
1. Load env vars. Mask to last 4 characters when echoing anything.
   HF_API_KEY, HF_SECRET, ELEVENLABS_API_KEY, SHOTSTACK_API_KEY_STAGE

2. Check whether episode 1 (pending/ai-tools-drop-2026-08-03) has rendered.
   If not, raise it with Michael before starting episode 2.

3. Read this brief plus script.md and social.md.
   Show Michael: section 2 (the outstanding voice decision), section 3
   (the hybrid approach and the four reused images), and the cost table
   in section 10, verbatim.
   WAIT for explicit approval before calling any paid endpoint.

4. After approval, in this order:
   (a) Check assets/ai-tools-drop/ for cached B1, B2, B3, B6 from episode 1.
       Only generate them if they are genuinely missing.
   (b) Higgsfield Soul: generate the 18 new images. Parallel is fine. Poll each.
       Save all URLs to a manifest file in this folder.
   (c) Higgsfield Kling: animate the 16 Group A images with their matching
       motion prompts. Poll all. Save the 16 video URLs to the manifest.
   (d) ElevenLabs: generate the long-form voiceover from the concatenated
       NARRATION blocks in script.md. Report the actual duration.
       If it falls outside 12:00 to 13:30, STOP and report. Do not edit the script.
       Listen back to the 9:45 to 10:45 warning segment specifically.
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
| Higgsfield Soul, 18 new images | 1.60 to 2.70 USD |
| Higgsfield Kling, 16 clips at 5s | 12.00 to 19.20 USD |
| ElevenLabs, approximately 11,000 chars long form | about 2.50 USD |
| ElevenLabs, approximately 1,100 chars short | about 0.25 USD |
| Shotstack stage, 2 renders | free within trial credits |
| **Stage total** | **about 16.35 to 24.65 USD** |
| Shotstack v1 production, 2 renders, after approval | per plan |

At roughly R16.20 to the dollar that is about **R265 to R400 per episode** before the production render. Slightly cheaper than episode 1, partly from reusing four images and cutting two Kling clips, and partly because the rand firmed over the week.

If Michael wants this cheaper still, the lever remains Layer 1. Cutting from 16 Kling clips to 10 saves about 6 USD an episode and shifts more runtime onto motion graphics, which suits chart-heavy content like this week's. Raise it with him rather than deciding unilaterally.

---

## 11. Post-render checklist

- [ ] Long form runtime lands between 12:00 and 13:30
- [ ] Narration audio has no clipping, no mispronounced tool names - check `Aveiro`, `Rindler`, `Wispr`, `Qwen`, `n8n`, `POPIA` specifically
- [ ] The Muse Code warning at 9:45 to 10:45 has no music bed and does not sound rushed
- [ ] The red warning card at 10:20 holds for at least 2 seconds and is legible on a phone
- [ ] All five motion graphics from section 6 are built as graphics, not as plain title cards
- [ ] Every overlay renders as clean ASCII, no mojibake, no missing glyphs
- [ ] No text wraps mid-word or overflows the safe area
- [ ] Accent colour reads legibly against the dark background on a phone screen
- [ ] AI disclosure lower-third present at open and on the end card, both deliverables
- [ ] Series watermark persistent on the long form
- [ ] End card holds at least 5 seconds with the WhatsApp channel details legible
- [ ] Short form hook lands inside the first 2 seconds
- [ ] Short form is legible with sound off
- [ ] Michael approves -> move this folder to `approved/`
- [ ] Re-render both on Shotstack v1 production, no watermark
- [ ] Upload with the platform AI disclosure ticked on every platform
- [ ] After posting, move to `published/` with the post links appended below

---

## 12. Series notes

Carried forward from episode 1 and updated:

- The hybrid Layer 1 / 2 / 3 split is what makes weekly long-form economically sane. Do not drift back to fully-animated.
- Group B abstract dividers are reusable. This episode reuses four of them. Cache them properly in `assets/ai-tools-drop/` if that has not been done yet, because it will keep paying off.
- The palette, watermark, disclosure lower-third and end card should be built once as reusable Shotstack fragments. If episode 1 built them, reuse rather than rebuild.
- Segment count will vary week to week. This week is ten tools again, but some weeks will have four. The composition must tolerate that.
- New note for this week: chart-heavy episodes need fewer Kling clips. Let the ratio follow the content rather than fixing it at 18 every time.

---

## 13. Metadata

```yaml
brief_id: 2026-08-10-ai-tools-drop
series: ai-tools-drop
episode_number: 2
episode_week: 2026-W33
product: eride-technologies
format: fully_ai_pipeline_longform
pipeline_stages:
  - higgsfield_soul_text_to_image
  - higgsfield_kling_image_to_video
  - elevenlabs_tts
  - shotstack_edit_stitch
deliverables:
  - id: A
    aspect_ratio: "16:9"
    resolution: 1920x1080
    target_duration_seconds: 780
    platforms: [youtube, facebook, whatsapp-channel]
  - id: B
    aspect_ratio: "9:16"
    resolution: 1080x1920
    target_duration_seconds: 75
    platforms: [tiktok, instagram-reels, youtube-shorts]
soul_images_new: 18
soul_images_reused: 4
kling_animations: 16
kenburns_stills: 6
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
estimated_stage_cost_usd: "16.35-24.65"
usd_zar_rate_used: 16.20
status: pending
created_by: perplexity-computer-scheduled
created_at: 2026-08-10T11:00:00+02:00
```

---

## 14. Post links

Fill in after publishing.

- YouTube:
- Facebook:
- TikTok:
- Instagram Reels:
- WhatsApp channel broadcast sent:
