# AI Pipeline Brief v2: The 53,000 Deportation Crackdown

**Brief ID:** `2026-07-27-ai-pipeline-02-deportation-crackdown-v2`
**Product:** E-Migration Assist
**Format:** Fully-AI Reel (Higgsfield Soul → Kling → ElevenLabs → Shotstack)
**Target duration:** 45 seconds
**Aspect / resolution:** 9:16 vertical, 1080×1920, MP4
**Status:** pending — ready for Claude Code execution
**Renders both versions:** voiced + silent

**What changed from v1:**
1. All visuals are South Africa-specific (Beitbridge, Home Affairs, SA cities, ZA passports)
2. Higgsfield Soul generates each input image from a text prompt (no Pexels stock)
3. E-Migration Assist logo overlay at opening and closing
4. Script tightened — same length but sharper hooks and cleaner CTA

---

## 1. News source (verified)

Between Cabinet's 3 June 2026 crackdown announcement and Minister Kubayi's 12 July 2026 update, **53,449 foreign nationals** were processed for deportation/repatriation. Musina alone: 20,000+.

**Primary source:** [VisaVerge — 12 July 2026](https://www.visaverge.com/immigration/south-africa-deports-53449-migrants-in-major-crackdown-under-five-point-plan/)
**Government source:** [gov.za IMC Update — 12 July 2026](https://www.gov.za/news/media-statements/inter-ministerial-committee-update-comprehensive-approach-migration-12-jul)

---

## 2. Voiceover script (tightened — v2)

**Copy into ElevenLabs `text` field verbatim. ~108 words = ~43-45 seconds.**

```
South Africa just deported fifty-three thousand foreign nationals in six weeks. Musina alone: twenty thousand.

If you think this doesn't affect you because your visa is valid — think again.

The government's five-point plan targets workplace inspections. Immigration officials arriving at your employer. Asking to see every foreign employee's paperwork. On the spot.

Wrong occupation code. Expired renewal. Missing endorsement. All flagged.

E-Migration Assist runs a compliance audit on your file in five minutes. We show you what's weak. We show you what to fix. Before Home Affairs shows up.

Protect your status. Not tomorrow. Right now.
```

**What changed from v1:**
- Opening hook: "South Africa just deported" is punchier than "Between June and July, South Africa processed"
- Direct address: "If you think this doesn't affect you… think again" — pattern interrupt
- Removed "save your entire life here" — replaced with "Protect your status. Not tomorrow. Right now."
- CTA is action-oriented, not vague

**ElevenLabs settings** (unchanged):
- **Voice ID:** `P1LmKcX63Ihgqy11sVRt` (Andrew — SA male)
- **Model:** `eleven_multilingual_v2`
- **Voice settings:** `stability=0.55, similarity_boost=0.75, style=0.20, use_speaker_boost=true`
- **Output:** `mp3_44100_128`

---

## 3. Six SA-specific b-roll clips — TWO-STAGE (Soul → Kling)

For each clip: (a) generate input image via Higgsfield Soul, (b) animate it via Kling image-to-video.

### Stage A — Higgsfield Soul (text-to-image)

**Endpoint:** `POST https://platform.higgsfield.ai/v1/text2image/soul`
**Auth:** `hf-api-key: ${HF_API_KEY}` (Soul endpoint uses `hf-api-key`, not combined `Key <id>:<secret>`)
**Body template:**
```json
{
  "prompt": "[PROMPT_TEXT]",
  "width_and_height": "1152x2048",
  "quality": "1080p",
  "enhance_prompt": true,
  "batch_size": 1
}
```

Poll `GET https://platform.higgsfield.ai/v1/jobs/{id}` until complete. Save the image URL for stage B.

**Six prompts (execute in this order):**

**Image 1 — Beitbridge border post crossing (opens the Reel)**
```
Aerial documentary shot of Beitbridge border post between South Africa and Zimbabwe, long queue of trucks and travellers, dusty afternoon light, red dust road, immigration officials in green uniforms visible, editorial photojournalism style, authentic South African border scene, cinematic wide shot, warm golden hour lighting
```

**Image 2 — Home Affairs office queue (workplace inspection setup)**
```
South African Home Affairs office in Johannesburg CBD, morning queue of foreign nationals holding passports and documents, government building interior, fluorescent lighting, diverse people including African migrants from Zimbabwe and Mozambique, editorial photojournalism, natural composition, authentic South African government office atmosphere
```

**Image 3 — Green ZA passport with visa stamps (flagged paperwork segment)**
```
Close-up macro shot of South African green passport open to visa stamps page, on a wooden desk, warm document review lighting, Zimbabwean and South African visa stamps visible, editorial style, shallow depth of field, authentic detail, warm burgundy tones
```

**Image 4 — Immigration official inspecting documents (workplace inspection)**
```
South African immigration official in green Home Affairs uniform reviewing employment documents at an office desk, professional serious atmosphere, natural office lighting, authentic government inspection scene, editorial photojournalism, Johannesburg office setting, hands and documents in focus
```

**Image 5 — Foreign migrant worker at construction site (workplace scene)**
```
Foreign migrant construction worker at Johannesburg building site, wearing hard hat and hi-vis vest, holding work permit and ID document, late afternoon golden light, Johannesburg CBD skyline in background including Ponte Tower, editorial photojournalism style, dignified authentic portrait
```

**Image 6 — Hand signing document on desk (resolution / CTA segment)**
```
Hand holding pen making precise signature on formal compliance document, professional deliberate movement, clean office desk with E-Migration Assist logo visible on document header, warm resolution lighting, editorial documentary style, calm confident atmosphere
```

**Expected Soul cost:** ~$0.09-0.15 × 6 = ~$0.55-0.90

### Stage B — Kling image-to-video

For each of the 6 Soul-generated images, POST to Kling with a matching motion prompt:

**Endpoint:** `POST https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video`
**Auth:** `Authorization: Key ${HF_API_KEY}:${HF_SECRET}` (combined format)
**Body template:**
```json
{
  "image_url": "[SOUL_IMAGE_URL_FROM_STAGE_A]",
  "prompt": "[MOTION_PROMPT]",
  "duration": 5,
  "aspect_ratio": "9:16"
}
```

**Motion prompts (matched to each image):**

| Image | Motion prompt |
|---|---|
| 1 (Beitbridge) | slow cinematic drone drift forward over the border queue, dust particles in warm light, subtle movement of people and vehicles |
| 2 (Home Affairs queue) | slow lateral drift across the queue, subtle movement of people shifting weight, natural documentary observation |
| 3 (ZA passport) | slow zoom into visa stamps, subtle rotation to catch light, editorial macro movement |
| 4 (Official inspecting) | subtle push in on the hands and documents, natural professional movement, calm scrutiny |
| 5 (Migrant worker) | slow push in on the worker holding permit, natural late afternoon light shift, dignified stillness |
| 6 (Hand signing) | slow motion of pen stroke completing the signature, warm resolution lighting, decisive movement |

**Expected Kling cost:** ~$0.75-1.20 × 6 = ~$4.50-7.20

---

## 4. On-screen text overlays

| # | Timing | Text | Notes |
|---|---|---|---|
| T1 | 0:00–0:03 | 53,000 DEPORTED IN 6 WEEKS | Title card, navy #0a1a3e bg, white bold |
| T2 | 0:04–0:07 | MUSINA ALONE: 20,000 | White bold, centered |
| T3 | 0:09–0:12 | THINK YOUR VISA PROTECTS YOU? | White bold, direct address |
| T4 | 0:14–0:17 | WORKPLACE INSPECTIONS COMING | White bold, warning tone |
| T5 | 0:20–0:22 | WRONG OCCUPATION CODE | Red accent |
| T6 | 0:23–0:25 | EXPIRED RENEWAL | Red accent |
| T7 | 0:26–0:28 | MISSING ENDORSEMENT | Red accent |
| T8 | 0:31–0:35 | 5-MINUTE COMPLIANCE AUDIT | White bold, EMA brand |
| T9 | 0:39–0:44 | PROTECT YOUR STATUS · LINK IN BIO | White bold, CTA |

---

## 5. Logo overlay strategy

**Logo URL:** `https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/assets/brand/ema-logo-navy.jpg`

**Placement in Shotstack composition:**
- **Opening logo card (0:00–0:02.5):** Full-frame logo as first visual, before any b-roll
- **Persistent corner watermark (0:02.5–0:41):** Logo scaled to ~15% width, top-right corner, throughout the Reel
- **Closing logo card (0:41–0:45):** Full-frame logo again as final CTA frame

This gives brand book-ends plus continuous presence.

---

## 6. Shotstack composition — voiced version

**Endpoint:** `POST https://api.shotstack.io/edit/stage/render`
**Header:** `x-api-key: ${SHOTSTACK_API_KEY_STAGE}`

```json
{
  "timeline": {
    "soundtrack": {
      "src": "[URL_TO_ELEVENLABS_MP3]",
      "effect": "fadeInFadeOut"
    },
    "background": "#0a1a3e",
    "tracks": [
      {
        "clips": [
          {"asset": {"type": "image", "src": "https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/assets/brand/ema-logo-navy.jpg"}, "start": 0, "length": 2.5, "fit": "contain", "scale": 0.85},
          {"asset": {"type": "video", "src": "[KLING_CLIP_1_URL]"}, "start": 2.5, "length": 5, "fit": "cover"},
          {"asset": {"type": "video", "src": "[KLING_CLIP_2_URL]"}, "start": 7.5, "length": 5, "fit": "cover"},
          {"asset": {"type": "video", "src": "[KLING_CLIP_3_URL]"}, "start": 12.5, "length": 5, "fit": "cover"},
          {"asset": {"type": "video", "src": "[KLING_CLIP_4_URL]"}, "start": 17.5, "length": 6, "fit": "cover"},
          {"asset": {"type": "video", "src": "[KLING_CLIP_5_URL]"}, "start": 23.5, "length": 8, "fit": "cover"},
          {"asset": {"type": "video", "src": "[KLING_CLIP_6_URL]"}, "start": 31.5, "length": 9.5, "fit": "cover"},
          {"asset": {"type": "image", "src": "https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/assets/brand/ema-logo-navy.jpg"}, "start": 41, "length": 4, "fit": "contain", "scale": 0.85}
        ]
      },
      {
        "clips": [
          {"asset": {"type": "image", "src": "https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/assets/brand/ema-logo-navy.jpg"}, "start": 2.5, "length": 38.5, "fit": "none", "scale": 0.15, "position": "topRight", "offset": {"x": -0.03, "y": -0.03}}
        ]
      },
      {
        "clips": [
          {"asset": {"type": "title", "text": "53,000 DEPORTED IN 6 WEEKS", "style": "future", "background": "#0a1a3e", "color": "#ffffff", "size": "large", "position": "center"}, "start": 0, "length": 2.5},
          {"asset": {"type": "title", "text": "MUSINA ALONE: 20,000", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 4, "length": 3},
          {"asset": {"type": "title", "text": "THINK YOUR VISA PROTECTS YOU?", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 9, "length": 3},
          {"asset": {"type": "title", "text": "WORKPLACE INSPECTIONS COMING", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 14, "length": 3},
          {"asset": {"type": "title", "text": "WRONG OCCUPATION CODE", "style": "minimal", "color": "#ff4444", "size": "medium", "position": "bottom"}, "start": 20, "length": 2},
          {"asset": {"type": "title", "text": "EXPIRED RENEWAL", "style": "minimal", "color": "#ff4444", "size": "medium", "position": "bottom"}, "start": 23, "length": 2},
          {"asset": {"type": "title", "text": "MISSING ENDORSEMENT", "style": "minimal", "color": "#ff4444", "size": "medium", "position": "bottom"}, "start": 26, "length": 2},
          {"asset": {"type": "title", "text": "5-MINUTE COMPLIANCE AUDIT", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 31, "length": 4},
          {"asset": {"type": "title", "text": "PROTECT YOUR STATUS · LINK IN BIO", "style": "future", "color": "#ffffff", "size": "large", "position": "center"}, "start": 39, "length": 5}
        ]
      }
    ]
  },
  "output": {
    "format": "mp4",
    "resolution": "1080",
    "aspectRatio": "9:16",
    "fps": 30
  }
}
```

---

## 7. Shotstack composition — silent version

Same as section 6 **except:**
- Remove the `soundtrack` block
- Optionally add `"soundtrack": {"src": "https://shotstack-assets.s3-ap-southeast-2.amazonaws.com/music/moment.mp3", "effect": "fadeInFadeOut"}`

---

## 8. Execution flow for Claude Code

```
1. Load env vars (mask to last 4 chars only):
   HF_API_KEY, HF_SECRET, ELEVENLABS_API_KEY, SHOTSTACK_API_KEY_STAGE

2. Fetch this brief and show me sections 2, 3, 5, 6, 7 verbatim.
   Wait for my explicit approval before touching any paid API.

3. After approval:
   (a) Higgsfield Soul: generate 6 input images in parallel.
       Poll each. Save 6 image URLs.
   (b) Higgsfield Kling: for each Soul image, submit image-to-video
       with the matching motion prompt. Poll all 6. Save 6 video URLs.
   (c) ElevenLabs TTS: generate voiceover.mp3 from section 2 text.
   (d) Shotstack ingest: upload voiceover.mp3, get public URL.
   (e) Shotstack render voiced version (section 6 JSON).
   (f) Shotstack render silent version (section 7 JSON).
   (g) Poll both Shotstack renders. Return both final MP4 URLs.

4. If any Soul or Kling render fails, STOP and ask me before retrying.
   Do not modify voiceover script text. Do not spend on v1 production
   render without my explicit go.
```

---

## 9. Cost breakdown (expected)

| Stage | Est. cost |
|---|---|
| Higgsfield Soul: 6 SA input images | ~$0.55-0.90 |
| Higgsfield Kling: 6 image-to-video clips | ~$4.50-7.20 |
| ElevenLabs (~660 chars) | ~$0.15 |
| Shotstack stage: 2 × 45s renders | free within trial credits |
| **Total** | **~$5.20-8.25** |

---

## 10. Post-render checklist

- [ ] Watch voiced version — does the SA imagery feel authentic?
- [ ] Watch silent version — does the message land with logo continuity?
- [ ] Check logo persistence — is corner watermark visible throughout?
- [ ] Check timing sync
- [ ] Michael's approval → move to `approved/`
- [ ] Post-approval: re-render both on Shotstack v1 production (no watermark)
- [ ] After posting: move to `published/` with post links

---

## 11. Metadata

```yaml
brief_id: 2026-07-27-ai-pipeline-02-deportation-crackdown-v2
product: e-migration-assist
format: fully_ai_pipeline_v2
supersedes: 2026-07-27-ai-pipeline-01-deportation-crackdown
pipeline_stages:
  - higgsfield_soul_text_to_image
  - higgsfield_kling_image_to_video
  - elevenlabs_tts
  - shotstack_edit_stitch
renders_two_versions:
  - voiced
  - silent
sa_specific_visuals: true
logo_overlay: true
logo_url: https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/assets/brand/ema-logo-navy.jpg
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
soul_input_images: 6
kling_animations: 6
shotstack_environment: stage
target_duration_seconds: 45
aspect_ratio: "9:16"
news_reactive: true
```
