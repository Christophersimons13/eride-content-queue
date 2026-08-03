# AI Tools Drop - Production Brief, Week of 27 July to 3 August 2026

**Brief ID:** `2026-08-03-ai-tools-drop`
**Product:** AI Tools Drop (weekly series, Eride Technologies)
**Format:** Fully-AI long-form video plus vertical short (Higgsfield Soul -> Kling -> ElevenLabs -> Shotstack)
**Status:** pending - ready for Claude Code execution
**Created by:** Perplexity Computer, scheduled Monday task
**Created at:** 2026-08-03T11:00:00+02:00

---

## 0. Read this before you spend anything

This is the **first** brief in a new weekly series, and it is a different shape from the E-Migration Assist Reels. It is long-form. A naive read of the script would have you generating 156 five-second Kling clips, which is roughly 150 to 190 US dollars per episode. That is not viable weekly.

**Section 3 sets out the hybrid approach that keeps this under about 25 dollars an episode.** Read it before you touch a paid endpoint.

**Stage-first gate applies.** Every Shotstack render goes to `stage` first. Nothing renders on `v1` production until Michael has watched the stage output and approved it. Do not skip this. Do not batch a production render "to save a round trip."

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

> **Decision needed from Michael before render:** do you want this series to share the EMA voice, or should the AI Tools Drop have its own distinct voice so the two brands do not blur? Ask before generating. If he does not answer, default to the ID above.

**Model:** `eleven_multilingual_v2`
**Voice settings:** `stability=0.60, similarity_boost=0.75, style=0.15, use_speaker_boost=true`

Note the settings differ from the EMA Reels. Higher stability and lower style, because this is thirteen minutes of explanatory delivery rather than forty-five seconds of urgency. Do not carry the EMA settings across.

**Output:** `mp3_44100_128`

**Pronunciation overrides:** `script.md` contains a pronunciation table. Apply it. `ElevenAgents`, `Hailuo`, `Adomate` and `POPIA` all get mangled without it. If the API path you are using does not support phonetic overrides, substitute the phonetic spelling directly into the text input for those tokens only.

**Pacing check:** target roughly 150 words per minute. If the generated audio comes back shorter than 12:00 or longer than 13:30, stop and report the actual duration rather than adjusting the script yourself.

---

## 3. Visual approach - the hybrid that makes this affordable

Do not attempt to fill thirteen minutes with animated AI clips. The composition is three layers:

**Layer 1 - AI b-roll, 18 Kling clips at 5 seconds each.** About 90 seconds of moving footage total. Used at segment openings and for the emotionally loaded moments only. Clips may be reused across segments where the imagery is generic.

**Layer 2 - Soul stills with slow Ken Burns motion, 6 images.** Shotstack handles the pan and zoom, so these cost image generation only, no video generation. Used for mid-segment visual breathing room.

**Layer 3 - motion graphics and title compositions, generated entirely in Shotstack.** This carries the bulk of the runtime. Price charts, bar comparisons, channel diagrams, checklists, the rejected-logos sequence. No AI generation cost at all. This is the right call anyway, because the content is numbers and comparisons, and a chart communicates a price cut better than a stock shot of a laptop.

Rough runtime split: 90 seconds Layer 1, 60 seconds Layer 2, 630 seconds Layer 3.

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

### Prompts - 24 images total

**Group A: to be animated by Kling (18 images)**

| # | Segment | Prompt |
|---|---|---|
| A1 | Cold open | Extreme close-up of a laptop spreadsheet on a desk in a Johannesburg home office, warm morning light through a window, a single cell highlighted, shallow depth of field, editorial photography style, muted professional tones |
| A2 | Why this week | South African founder in their thirties working at a standing desk in a Braamfontein co-working space, natural morning light, laptop and notebook, editorial documentary style, authentic and unposed |
| A3 | ElevenAgents | Hands holding a smartphone showing a WhatsApp conversation thread, warm indoor light, close crop, editorial style, clean and modern |
| A4 | ElevenAgents | Interior of an upmarket Johannesburg hair salon, empty styling chairs, soft afternoon light through large windows, warm neutral palette, architectural photography style |
| A5 | ElevenAgents | Small clinic reception desk with a tablet and appointment diary, calm professional atmosphere, natural light, editorial interior photography |
| A6 | Model Council | Overhead shot of a boardroom table with eight identical notepads arranged in a circle, single pen on each, dramatic overhead light, conceptual editorial photography, high contrast |
| A7 | Model Council | Close-up of two documents side by side on a desk with contradictory figures visible, one line marked in red pen, warm desk lamp light, editorial detail shot |
| A8 | Workspace | Presentation slides fanned out as printed pages on a clean white desk, top-down view, minimal branded design visible, warm even light, editorial product photography |
| A9 | Workspace | Creative agency team of three reviewing a printed deck at a table in a Cape Town studio, natural light, editorial documentary style, diverse South African team |
| A10 | Price cuts | Close-up of a hand writing calculations in a notebook beside an open laptop, warm morning light, shallow focus on the pen tip, editorial photography |
| A11 | Price cuts | Server rack interior in a clean data centre, blue and white indicator lights, long corridor perspective, cool tones, architectural technology photography |
| A12 | Price cuts | Overhead of a desk with a calculator, printed invoice and coffee cup, warm morning light, South African context, editorial flat-lay photography |
| A13 | Gemini | Person dictating to a laptop at a desk, mid-speech, MacBook visible, warm natural window light, editorial candid photography, professional home office |
| A14 | Gemini | Antique brass globe on a wooden desk, southern Africa facing the camera, warm directional light, shallow depth of field, editorial still life |
| A15 | Notion | Close-up of a project board with sticky notes on a glass wall in a modern office, natural light, shallow depth of field, editorial workplace photography |
| A16 | NudgeForMe | Close-up of a laptop screen showing an email inbox, three threads visible, warm evening desk lamp light, over-shoulder angle, editorial photography |
| A17 | MiniMax | Product photography setup with a small studio light, seamless backdrop and a cosmetic product on a stand, warm studio light, behind-the-scenes editorial style |
| A18 | Closing | Wide shot of Johannesburg skyline at golden hour from a rooftop, Sandton towers visible, warm light, cinematic editorial cityscape |

**Group B: Ken Burns stills, no Kling animation (6 images)**

| # | Use | Prompt |
|---|---|---|
| B1 | Segment divider | Minimal abstract composition of layered paper in warm neutral tones, soft directional light, no text, editorial design photography |
| B2 | Segment divider | Overhead of an empty clean wooden desk with a single notebook, warm morning light, generous negative space, minimal editorial photography |
| B3 | Left-out section | Close-up of a printed page with a single line struck through in red pen, warm desk light, shallow focus, editorial detail |
| B4 | Local news section | Exterior of a modern South African corporate office building, glass and concrete, blue hour light, architectural photography |
| B5 | Local news section | Young South African developers at computers in a training centre classroom, natural light, editorial documentary style, authentic and diverse |
| B6 | End card backdrop | Dark neutral gradient backdrop with subtle texture, no subject, no text, deep charcoal tones, suitable as a title card background |

**Expected Soul cost:** 24 images at roughly 0.09 to 0.15 USD each, so about 2.20 to 3.60 USD.

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
| A1 | slow push in on the highlighted spreadsheet cell, subtle dust particles in the window light |
| A2 | slow lateral drift past the founder at the desk, natural unposed movement, documentary observation |
| A3 | subtle scroll movement on the phone screen, thumb entering frame, natural hand motion |
| A4 | slow drift through the empty salon, soft light shifting across the chairs, calm and still |
| A5 | gentle push in on the reception tablet, subtle ambient movement in the background |
| A6 | slow overhead rotation above the circle of notepads, dramatic light sweeping across |
| A7 | slow lateral drift between the two documents, settling on the red pen mark |
| A8 | slow overhead drift across the fanned slide pages, soft light shifting |
| A9 | subtle push in on the team reviewing the deck, natural conversational movement |
| A10 | slow motion of the pen completing a calculation, warm light, deliberate movement |
| A11 | slow dolly forward down the server corridor, indicator lights pulsing gently |
| A12 | slow overhead descent onto the desk, steam rising from the coffee cup |
| A13 | subtle push in on the person mid-speech, natural head movement, text appearing on screen |
| A14 | slow rotation of the globe bringing southern Africa fully into frame, warm light shifting |
| A15 | slow lateral drift across the project board, subtle depth parallax on the sticky notes |
| A16 | slow push in on the inbox screen, subtle scroll movement revealing the threads |
| A17 | slow orbit around the product on the stand, studio light catching the surface |
| A18 | slow cinematic drone drift across the Johannesburg skyline, golden light deepening |

**Expected Kling cost:** 18 clips at roughly 0.75 to 1.20 USD each, so about 13.50 to 21.60 USD.

---

## 6. Shotstack composition

**Endpoint:** `POST https://api.shotstack.io/edit/stage/render`
**Header:** `x-api-key: ${SHOTSTACK_API_KEY_STAGE}`

### Structure for deliverable A

- **Track 1 (base):** the visual bed. Kling clips, Ken Burns stills, and solid-colour cards, sequenced to the segment timings in `script.md`.
- **Track 2 (graphics):** charts, diagrams and comparison compositions. This carries most of the runtime. Build these as title and shape assets, layered.
- **Track 3 (overlays):** the ON-SCREEN TEXT blocks from `script.md`, timed to their segment ranges.
- **Track 4 (persistent):** series watermark, top-right, roughly 12 percent width, present from 0:03 to the end card. Plus the AI disclosure lower-third - see section 8.
- **Soundtrack:** the ElevenLabs MP3, `fadeInFadeOut`.

### Ken Burns on stills

Use image assets with a slow `zoom` or `pan` effect, 8 to 12 seconds each. Never hold a still frame motionless for more than two seconds.

### Music

Light bed at low mix, except **6:00 to 8:00**. The price-cut segment runs with voice only. Let the numbers land dry. This is a deliberate choice, not an oversight.

### Colour and type

Series palette, distinct from the EMA navy so the two brands stay separate:
- Background: `#111111`
- Primary text: `#FFFFFF`
- Accent, for prices and the key numbers: `#F5C542`
- Negative or warning accent: `#E5533D`

Use `style: "minimal"` for body overlays and `style: "future"` for full-frame title cards.

### Deliverable B

Rebuild vertically at 1080x1920 using the section 1 narration and overlays from `social.md`. Reuse Kling clips A1, A10, A11, A3 and A4 - regenerate them at 9:16 via Soul and Kling only if the crop genuinely fails. Try the crop first.

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

2. Read this brief plus script.md and social.md.
   Show Michael: section 2 (voice decision), section 3 (the hybrid approach),
   and the cost table in section 10, verbatim.
   WAIT for explicit approval before calling any paid endpoint.
   Also get his answer on the voice question in section 2.

3. After approval, in this order:
   (a) Higgsfield Soul: generate all 24 images. Parallel is fine. Poll each.
       Save the 24 URLs to a manifest file in this folder.
   (b) Higgsfield Kling: animate the 18 Group A images with their matching
       motion prompts. Poll all. Save the 18 video URLs to the manifest.
   (c) ElevenLabs: generate the long-form voiceover from the concatenated
       NARRATION blocks in script.md. Report the actual duration.
       If it falls outside 12:00 to 13:30, STOP and report. Do not edit the script.
   (d) ElevenLabs: generate the short voiceover from social.md section 1.
   (e) Shotstack ingest: upload both MP3s, get public URLs.
   (f) Run the ASCII check from section 7 over the composed JSON. Fail loudly
       on any non-ASCII byte in a text field.
   (g) Shotstack STAGE render, deliverable A (16:9).
   (h) Shotstack STAGE render, deliverable B (9:16).
   (i) Poll both. Return both stage MP4 URLs to Michael.

4. STOP HERE. Do not render on v1 production.
   Michael watches both stage renders and approves or sends notes.
   Only after his explicit go, re-render both on v1 production.

5. On any Soul or Kling failure, STOP and ask before retrying.
   Do not silently regenerate. Do not alter narration text.
   Do not substitute a different model to work around a failure.
```

---

## 10. Cost breakdown

| Stage | Expected |
|---|---|
| Higgsfield Soul, 24 images | 2.20 to 3.60 USD |
| Higgsfield Kling, 18 clips at 5s | 13.50 to 21.60 USD |
| ElevenLabs, approximately 11,000 chars long form | about 2.50 USD |
| ElevenLabs, approximately 1,100 chars short | about 0.25 USD |
| Shotstack stage, 2 renders | free within trial credits |
| **Stage total** | **about 18.45 to 27.95 USD** |
| Shotstack v1 production, 2 renders, after approval | per plan |

At roughly R16.50 to the dollar that is about **R305 to R460 per episode** before the production render. Weekly, that is roughly R1,300 to R2,000 a month.

If Michael wants this cheaper, the lever is Layer 1. Cutting from 18 Kling clips to 10 saves about 8 USD an episode and shifts more runtime onto motion graphics, which suits this content anyway. Raise it with him rather than deciding unilaterally.

---

## 11. Post-render checklist

- [ ] Long form runtime lands between 12:00 and 13:30
- [ ] Narration audio has no clipping, no mispronounced tool names - check `ElevenAgents`, `Hailuo`, `Adomate`, `POPIA` specifically
- [ ] No music under the 6:00 to 8:00 price-cut segment
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

## 12. Series notes for future weeks

This brief is the template. Things worth carrying forward:

- The hybrid Layer 1 / 2 / 3 split is what makes a weekly long-form economically sane. Do not drift back to fully-animated.
- Soul images in Group B and the abstract dividers are reusable across episodes. Cache them in `assets/ai-tools-drop/` rather than regenerating weekly.
- The palette, watermark, disclosure lower-third and end card should be built once as reusable Shotstack fragments.
- Segment count will vary week to week. Some weeks will have four tools, not ten. The composition needs to tolerate that.

---

## 13. Metadata

```yaml
brief_id: 2026-08-03-ai-tools-drop
series: ai-tools-drop
episode_week: 2026-W32
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
soul_images: 24
kling_animations: 18
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
estimated_stage_cost_usd: "18.45-27.95"
status: pending
created_by: perplexity-computer-scheduled
created_at: 2026-08-03T11:00:00+02:00
```

---

## 14. Post links

Fill in after publishing.

- YouTube:
- Facebook:
- TikTok:
- Instagram Reels:
- WhatsApp channel broadcast sent:
