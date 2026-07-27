# AI Pipeline Brief: The 53,000 Deportation Crackdown

**Brief ID:** `2026-07-27-ai-pipeline-01-deportation-crackdown`
**Product:** E-Migration Assist
**Format:** Fully-AI Reel (ElevenLabs VO + Higgsfield b-roll + Shotstack stitch)
**Target duration:** 45 seconds
**Aspect / resolution:** 9:16 vertical, 1080×1920, MP4
**Priority:** ⭐⭐⭐ HIGHEST — most urgent news cycle
**Status:** pending — ready for Claude Code execution
**Renders both versions:** voiced + silent

---

## 1. News source (verified)

Between Cabinet's 3 June 2026 crackdown announcement and Minister Kubayi's 12 July 2026 update, **53,449 foreign nationals** were processed for deportation/repatriation. Musina alone: 20,000+.

**Primary source:** [VisaVerge — 12 July 2026](https://www.visaverge.com/immigration/south-africa-deports-53449-migrants-in-major-crackdown-under-five-point-plan/)
**Government source:** [gov.za IMC Update — 12 July 2026](https://www.gov.za/news/media-statements/inter-ministerial-committee-update-comprehensive-approach-migration-12-jul)

---

## 2. Voiceover script (exact text for ElevenLabs)

**Copy the text below into ElevenLabs API `text` field verbatim. ~110 words = ~42-45 seconds at natural pace.**

```
Between June and July this year, South Africa processed fifty-three thousand foreign nationals for deportation. Musina alone handled twenty thousand.

But here's what most people don't realise. This isn't just about undocumented migrants. The government's five-point plan includes workplace inspections. Immigration officials showing up at your employer, asking to see every foreign employee's paperwork.

Wrong occupation code — flagged. Expired visa — flagged. Incomplete file — flagged.

At E-Migration Assist, we run a compliance audit on your case in under five minutes. We tell you where your file is weak, what to fix, and how to get your paperwork watertight.

Right now, five minutes could save your entire life here. Link in bio.
```

**ElevenLabs settings:**
- **Voice ID:** `P1LmKcX63Ihgqy11sVRt` (Andrew — deep South African male, 40s, calm authoritative)
- **Model:** `eleven_multilingual_v2`
- **Voice settings:** `stability=0.55, similarity_boost=0.75, style=0.20, use_speaker_boost=true`
- **Output format:** `mp3_44100_128`

**Fallback voices** (if Andrew doesn't fit tonally):
- `pFZP5JQG7iQjIQuC4Bku` (Lily — British) with v3 audio tag `[South African accent]`
- `TX3LPaxmHKxFdv7VOQHJ` (Liam) — American male, warmer alternative
- Any voice from Voice Library search for "South African" in the ElevenLabs app

---

## 3. B-roll clips needed (Higgsfield)

Six 5-second clips. Two already rendered tonight, four new renders needed.

### Already rendered — reuse

| # | Description | URL | Source image |
|---|---|---|---|
| A | Passport with visa stamps, slow zoom | `https://d3u0tzju9qaucj.cloudfront.net/fb1e5cec-662c-4f40-8a2a-3c3816a1217b/0706445f-ceac-4708-a6e8-57b4edab4251.mp4` | Pexels 5405596 |

### To render new (4 clips)

For each, POST to `https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video` with `Authorization: Key ${HF_API_KEY}:${HF_SECRET}` and `Content-Type: application/json`. Poll status every 8 seconds until complete.

**Clip B — Airport terminal drift** (opens the Reel)
```json
{
  "image_url": "https://images.pexels.com/photos/34010521/pexels-photo-34010521.jpeg?cs=srgb&fm=jpg",
  "prompt": "slow cinematic drift through sunlit airport terminal, warm golden hour atmosphere, silhouetted travelers, editorial tension mood",
  "duration": 5,
  "aspect_ratio": "9:16"
}
```

**Clip C — Documents on desk** (workplace inspection segment)
```json
{
  "image_url": "https://images.pexels.com/photos/33996085/pexels-photo-33996085.jpeg?cs=srgb&fm=jpg",
  "prompt": "slow lateral drift across office desk with stacked documents, warm document review lighting, institutional gravity",
  "duration": 5,
  "aspect_ratio": "9:16"
}
```

**Clip D — Passports with map** (flagged paperwork segment)
```json
{
  "image_url": "https://images.pexels.com/photos/29485309/pexels-photo-29485309.jpeg?cs=srgb&fm=jpg",
  "prompt": "slow zoom into passports on map, warm burgundy tones, tension mood, editorial documentary style",
  "duration": 5,
  "aspect_ratio": "9:16"
}
```

**Clip E — Hand signing** (solution segment)
```json
{
  "image_url": "https://images.pexels.com/photos/7504780/pexels-photo-7504780.jpeg?cs=srgb&fm=jpg",
  "prompt": "slow motion pen making precise signature stroke, professional deliberate movement, resolution mood, clean editorial lighting",
  "duration": 5,
  "aspect_ratio": "9:16"
}
```

Save the resulting video URLs from each Higgsfield response — you'll need them for Shotstack.

---

## 4. On-screen text overlays

Every Reel gets these text overlays. In the **silent version** they're the whole message. In the **voiced version** they're synced accents to the voiceover.

| # | Timing | Text | Notes |
|---|---|---|---|
| T1 | 0:00–0:03 | **WHY 53,000 DEPORTATIONS SHOULD SCARE YOU** | Title card, navy background, white bold |
| T2 | 0:04–0:07 | 53,449 FOREIGN NATIONALS | White bold, centered |
| T3 | 0:07–0:10 | PROCESSED FOR DEPORTATION | White bold, centered |
| T4 | 0:11–0:14 | MUSINA ALONE: 20,000 | White bold, centered |
| T5 | 0:16–0:19 | WORKPLACE INSPECTIONS ARE COMING | White bold, warning tone |
| T6 | 0:22–0:24 | WRONG OCCUPATION CODE — FLAGGED | Red accent under white |
| T7 | 0:25–0:27 | EXPIRED VISA — FLAGGED | Red accent under white |
| T8 | 0:28–0:30 | INCOMPLETE FILE — FLAGGED | Red accent under white |
| T9 | 0:32–0:36 | E-MIGRATION ASSIST · 5-MIN AUDIT | White bold, EMA brand |
| T10 | 0:41–0:45 | LINK IN BIO | White bold, CTA |

Font: bold sans-serif (Montserrat / DM Sans / Inter Bold). Position: bottom third of frame with slight drop shadow for readability.

---

## 5. Shotstack composition — voiced version

**Endpoint:** `POST https://api.shotstack.io/edit/stage/render` (use `stage` while trialling, `v1` when production-ready)

**Header:** `x-api-key: ${SHOTSTACK_API_KEY_STAGE}`

**Body (voiced):**
```json
{
  "timeline": {
    "soundtrack": {
      "src": "[URL_TO_ELEVENLABS_MP3_UPLOADED_TO_S3_OR_HOSTED]",
      "effect": "fadeInFadeOut"
    },
    "background": "#0a1a3e",
    "tracks": [
      {
        "clips": [
          {"asset": {"type": "video", "src": "[CLIP_B_URL]"}, "start": 0, "length": 5, "fit": "cover"},
          {"asset": {"type": "video", "src": "[CLIP_A_URL]"}, "start": 5, "length": 5, "fit": "cover"},
          {"asset": {"type": "video", "src": "[CLIP_C_URL]"}, "start": 10, "length": 8, "fit": "cover"},
          {"asset": {"type": "video", "src": "[CLIP_D_URL]"}, "start": 18, "length": 10, "fit": "cover"},
          {"asset": {"type": "video", "src": "[CLIP_E_URL]"}, "start": 28, "length": 10, "fit": "cover"},
          {"asset": {"type": "video", "src": "[CLIP_A_URL]"}, "start": 38, "length": 7, "fit": "cover"}
        ]
      },
      {
        "clips": [
          {"asset": {"type": "title", "text": "WHY 53,000 DEPORTATIONS SHOULD SCARE YOU", "style": "future", "background": "#0a1a3e", "color": "#ffffff", "size": "large", "position": "center"}, "start": 0, "length": 3},
          {"asset": {"type": "title", "text": "53,449 FOREIGN NATIONALS", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 4, "length": 3},
          {"asset": {"type": "title", "text": "PROCESSED FOR DEPORTATION", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 7, "length": 3},
          {"asset": {"type": "title", "text": "MUSINA ALONE: 20,000", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 11, "length": 3},
          {"asset": {"type": "title", "text": "WORKPLACE INSPECTIONS ARE COMING", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 16, "length": 3},
          {"asset": {"type": "title", "text": "WRONG OCCUPATION CODE — FLAGGED", "style": "minimal", "color": "#ff4444", "size": "medium", "position": "bottom"}, "start": 22, "length": 2},
          {"asset": {"type": "title", "text": "EXPIRED VISA — FLAGGED", "style": "minimal", "color": "#ff4444", "size": "medium", "position": "bottom"}, "start": 25, "length": 2},
          {"asset": {"type": "title", "text": "INCOMPLETE FILE — FLAGGED", "style": "minimal", "color": "#ff4444", "size": "medium", "position": "bottom"}, "start": 28, "length": 2},
          {"asset": {"type": "title", "text": "E-MIGRATION ASSIST · 5-MIN AUDIT", "style": "minimal", "color": "#ffffff", "size": "medium", "position": "bottom"}, "start": 32, "length": 4},
          {"asset": {"type": "title", "text": "LINK IN BIO", "style": "future", "color": "#ffffff", "size": "large", "position": "center"}, "start": 41, "length": 4}
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

## 6. Shotstack composition — silent version

Same as above **except:**
- Remove the `soundtrack` block entirely
- Optionally add a light instrumental music track: `"soundtrack": {"src": "https://shotstack-assets.s3-ap-southeast-2.amazonaws.com/music/moment.mp3", "effect": "fadeInFadeOut"}`
- Make text overlays **longer and more emphatic** since they carry the whole message — extend each title `length` by +1 second

---

## 7. Execution flow for Claude Code

```
1. Load env vars from higgsfield-keys.txt:
   HF_API_KEY, HF_SECRET, ELEVENLABS_API_KEY,
   SHOTSTACK_API_KEY_STAGE

2. Call ElevenLabs TTS:
   POST https://api.elevenlabs.io/v1/text-to-speech/P1LmKcX63Ihgqy11sVRt
   Header: xi-api-key: $ELEVENLABS_API_KEY
   Body: {"text": "[script from section 2]",
          "model_id": "eleven_multilingual_v2",
          "voice_settings": {"stability": 0.55, "similarity_boost": 0.75, "style": 0.20, "use_speaker_boost": true}}
   Save MP3 to local disk (voiceover.mp3).

3. Upload voiceover.mp3 to Shotstack's asset upload endpoint (or
   host it on a public URL Claude can generate — Shotstack accepts
   any HTTPS URL). Use Shotstack's ingest API:
   POST https://api.shotstack.io/ingest/stage/sources
   Header: x-api-key: $SHOTSTACK_API_KEY_STAGE
   Body: {"url": null, "upload": true}
   → returns signed upload URL → PUT the mp3 → returns public asset URL.

4. Render 4 new Higgsfield b-roll clips in parallel (or sequentially):
   For each, POST to platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video
   with the JSON bodies in section 3.
   Poll each until complete. Collect the 4 video URLs.

5. Submit voiced Shotstack render:
   POST https://api.shotstack.io/edit/stage/render
   Header: x-api-key: $SHOTSTACK_API_KEY_STAGE
   Body: [JSON from section 5, with all URL placeholders filled in]
   Save render ID.

6. Submit silent Shotstack render:
   Same as step 5 but with section 6's JSON body.

7. Poll both Shotstack renders every 10s:
   GET https://api.shotstack.io/edit/stage/render/{id}
   Header: x-api-key: $SHOTSTACK_API_KEY_STAGE
   Wait for status="done" on both.

8. Return two MP4 URLs to me:
   - voiced_version_url
   - silent_version_url
   Plus total credit costs from all three APIs if visible in responses.
```

---

## 8. Cost breakdown (expected)

| Stage | Estimated cost |
|---|---|
| ElevenLabs (~110 words / ~660 chars) | ~$0.15 (well under 10k character free tier limit) |
| Higgsfield: 4 new b-roll clips @ Kling 2.1 Pro | ~$3-6 total |
| Shotstack stage: 2 renders × 45s = 1.5 min | ~$0.45 (or 0.75 free credits) |
| **Total** | **~$4-7 for both versions** |

Shotstack stage renders include a watermark. When we like the format, we re-render on `v1` (production) using `SHOTSTACK_API_KEY_PROD` at same cost with no watermark.

---

## 9. Compliance & tone notes

- ✅ Voice: Andrew is a professional SA English voice, matches EMA authority tone
- ✅ Script tone: warning-based but not xenophobic — target audience is legal visa holders
- ✅ All numbers are official government figures
- ✅ Source imagery is Pexels-licensed
- ⚠️ Do not modify the script during execution — the timing math is calibrated for ~110 words at natural pace
- ⚠️ Never inline any API keys in shell commands — always $env: references

---

## 10. Post-render checklist

- [ ] Watch voiced version — does Andrew sound right for EMA?
- [ ] Watch silent version — does the message land without audio?
- [ ] Check timing — does everything sync?
- [ ] Michael's approval before posting
- [ ] Move brief to `in-progress/` when rendered
- [ ] Move to `approved/` after Michael approves
- [ ] Move to `published/` after posting with links

---

## 11. Metadata

```yaml
brief_id: 2026-07-27-ai-pipeline-01-deportation-crackdown
product: e-migration-assist
format: fully_ai_pipeline
pipeline_stages:
  - elevenlabs_tts
  - higgsfield_kling_image_to_video
  - shotstack_edit_stitch
renders_two_versions:
  - voiced
  - silent
elevenlabs_voice_id: P1LmKcX63Ihgqy11sVRt
elevenlabs_model_id: eleven_multilingual_v2
higgsfield_broll_clips: 5
higgsfield_new_renders: 4
higgsfield_reused_clips: 1
shotstack_environment: stage
target_duration_seconds: 45
aspect_ratio: "9:16"
resolution: "1080x1920"
fps: 30
news_reactive: true
news_urgency: highest
news_source_date: 2026-07-12
```
