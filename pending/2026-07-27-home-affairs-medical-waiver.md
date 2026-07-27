# Brief: Home Affairs scraps medical report requirement — what applicants must know

**Brief ID:** `2026-07-27-home-affairs-medical-waiver`
**Product:** E-Migration Assist
**Created:** 2026-07-27
**Author:** Perplexity (via Michael Brits)
**Status:** pending
**Priority:** high — fresh news cycle, react within 48 hours

---

## 1. News hook & source

On **8 July 2026**, Home Affairs Minister Leon Schreiber signed an immigration directive that scraps the medical-report requirement for both permanent-residence and temporary-residence visa applications. The waiver was gazetted with immediate effect and applies to all future applications *and* those currently pending adjudication.

**Primary source:** [Home Affairs confirms sweeping visa changes — South African Lawyer, 21 July 2026](https://www.southafricanlawyer.co.za/article/2026/07/home-affairs-confirms-sweeping-visa-changes/)

**Legal instruments affected:** Sub-regulations 9(1)(c) and 23(1)(f) of the 2014 Immigration Regulations.

**Critical clarification (not widely reported):**
Per IBN Immigration Services, the waiver for **temporary residence visas is only applicable to those already inside South Africa**. Applicants applying from outside SA — through an embassy, consulate, or VFS office abroad — must still submit a medical report. Missing this nuance is exactly the kind of thing that causes rejected applications.

**Why this matters for E-Migration Assist:** Real users are now confused about whether they need a medical report. Some will skip it and get rejected. Some will submit it unnecessarily. Our product answers exactly this in seconds.

---

## 2. Positioning angle

**Problem the news creates:** Every applicant currently in queue is now unsure whether their submission is complete, missing a doc, or over-documented. Consultants will milk this for panic calls. Immigration lawyers will bill for clarification. Ordinary applicants will guess wrong.

**Our answer:** *E-Migration Assist maps your exact 2026 pathway in under 5 minutes — so you know what to submit, what to skip, and where the new rules apply to your specific case.*

**Voice / tone:** Confident, calm, not alarmist. Position as the sensible guide, not another panic account.

---

## 3. Reel script (target: 20 seconds, 9:16 vertical)

### Hook (0:00 – 0:03)
> **On-screen text:** "SA VISA RULES JUST CHANGED"
> **Voiceover:** *"If you're applying for a South African visa right now — the rules just changed."*
> **Visual:** Slow zoom into a passport / official document.

### Body (0:03 – 0:15)
> **On-screen text:** "MEDICAL REPORT: WAIVED (with a catch)"
> **Voiceover:** *"Home Affairs has scrapped the medical report requirement for permanent and temporary residency — but only if you're applying from inside South Africa. Apply from abroad and you still need it. Most people will get this wrong."*
> **Visual:** Cinematic drift across the document, warm golden hour light.

### Close (0:15 – 0:20)
> **On-screen text:** "E-MIGRATION ASSIST · YOUR PATHWAY IN 5 MIN"
> **Voiceover:** *"E-Migration Assist maps your exact pathway to the 2026 rules — link in bio."*
> **Visual:** Subtle vignette closing in, brand mark fades in.

---

## 4. Caption for the post

> 🇿🇦 **Home Affairs just changed the visa rules — and most applicants don't know the fine print.**
>
> Minister Schreiber signed a directive on 8 July 2026 scrapping medical-report requirements for permanent and temporary residence applications. Effective immediately, retroactive to pending applications.
>
> **The catch nobody's talking about:** the waiver only applies if you're applying from **inside** South Africa. Apply through an embassy, consulate, or VFS office abroad → you still need the medical report.
>
> Get your exact 2026 pathway in 5 minutes → link in bio.
>
> Source: South African Lawyer, 21 July 2026
>
> #SAImmigration #HomeAffairs #VisaSA #PermanentResidencySA #EMigrationAssist #CapeTown #Johannesburg #SouthAfrica2026

---

## 5. Source image (to feed Higgsfield)

**Selected image URL:** `https://images.pexels.com/photos/5405596/pexels-photo-5405596.jpeg?cs=srgb&dl=pexels-taryn-elliott-5405596.jpg&fm=jpg`
**Source:** [Pexels — Travel documents and necessities](https://www.pexels.com/photo/travel-documents-and-necessities-5405596/)
**Photographer:** Taryn Elliott
**License:** Pexels License — free for commercial use, no attribution required (attribution optional; we'll credit anyway in the caption)
**Reason chosen:** Flat-lay of an open passport with visa entry/exit stamps, world map, wristwatch, coins, travel tickets. No people visible. Neutral warm tones. Portrait orientation. Directly reinforces the "visa rules changing" story.

**Fallback options (also verified, legally clear, Pexels licensed):**
- **Passports with currency on map** — Marta Branco, [photo 29485309](https://www.pexels.com/photo/european-passports-with-euro-currency-on-map-29485309/) — `https://images.pexels.com/photos/29485309/pexels-photo-29485309.jpeg?cs=srgb&fm=jpg`
- **Airport arrivals golden hour** — Wellington Franzao, [photo 34010521](https://www.pexels.com/photo/silhouetted-travelers-in-a-sunny-airport-terminal-34010521/) — `https://images.pexels.com/photos/34010521/pexels-photo-34010521.jpeg?cs=srgb&fm=jpg`
- **Hand signing document** — Olha Ruskykh, [photo 7504780](https://www.pexels.com/photo/close-up-photo-of-a-person-s-hand-signing-a-paper-7504780/) — `https://images.pexels.com/photos/7504780/pexels-photo-7504780.jpeg?cs=srgb&fm=jpg`
- **Vintage government office desk** — Cheng Shi Song, [photo 33996085](https://www.pexels.com/photo/vintage-office-desk-with-lamp-in-meiling-palace-33996085/) — `https://images.pexels.com/photos/33996085/pexels-photo-33996085.jpeg?cs=srgb&fm=jpg`

---

## 6. Higgsfield API call spec

**Endpoint:** `POST https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video`

> **Correction note (2026-07-27, 4:21 PM SAST):** Earlier draft included a `v1/` prefix. The verified working endpoint (from `request_id 319dcc7e-3f6b-40c6-8841-78f8e744e38f`) has NO `v1/` prefix. The `v1/` namespace exists separately for `text2image/soul` only. Fixed.

**Headers:**
```
Authorization: Key ${HF_API_KEY}:${HF_SECRET}
Content-Type: application/json
Accept: application/json
```
(Load `HF_API_KEY` and `HF_SECRET` from environment variables — never inline them.)

**Body:**
```json
{
  "image_url": "https://images.pexels.com/photos/5405596/pexels-photo-5405596.jpeg?cs=srgb&fm=jpg",
  "prompt": "cinematic slow zoom into official document, gentle camera drift, warm golden hour tones, shallow depth of field, subtle vignette, professional editorial mood",
  "duration": 5,
  "aspect_ratio": "9:16",
  "negative_prompt": "text overlays, watermarks, logos, faces, distortion, blurry, artifacts"
}
```

**Poll for completion:** Same pattern as our verified test — 8-second intervals, up to 20 polls (~2:40 max wait).

**Expected credit cost:** Same tier as our first successful clip (`request_id: 319dcc7e-3f6b-40c6-8841-78f8e744e38f`). Check Higgsfield billing dashboard for exact deduction.

---

## 7. Post-production notes (for Michael / editor)

- **Voiceover:** Record in a South African English accent, calm confident delivery. Alternatively use ElevenLabs "Adam" voice or similar authoritative male voice.
- **On-screen text:** Overlay the three text cues above using CapCut or Descript. Font: bold sans-serif (Inter, Poppins, or DM Sans). Colour: white with subtle drop shadow.
- **Music:** Low-tempo cinematic underscore. Suggested: Epidemic Sound "Slow Motion" or "Editorial Documentary" categories.
- **End frame:** Hold on E-Migration Assist logo for 1 second before cut.

---

## 8. Approval checklist (before posting)

- [ ] Video renders correctly at 9:16, 5 seconds
- [ ] Voiceover recorded and synced
- [ ] Captions on-screen match voiceover
- [ ] No copyrighted news photos anywhere in the frame
- [ ] Source article linked in Instagram description
- [ ] E-Migration Assist link in bio verified live
- [ ] Michael approves final cut via Telegram approval bot (once bot is wired)

---

## 9. Legal & compliance notes

- ✅ **News facts are fair use** — factual reporting of a gazetted government directive.
- ✅ **Source image is commercially licensed** — Pexels license permits marketing use.
- ⚠️ **Do not** overlay any News24, Daily Maverick, EWN, or wire-service imagery in the final cut.
- ⚠️ **Do not** imply E-Migration Assist has any official Home Affairs endorsement.
- ✅ Attribution: mention the source ("South African Lawyer") in the Instagram caption.

---

## 10. Metadata (for tracking)

```yaml
brief_id: 2026-07-27-home-affairs-medical-waiver
product: e-migration-assist
platform_targets:
  - instagram_reels
  - tiktok
  - linkedin_video
news_reactive: true
news_source_url: https://www.southafricanlawyer.co.za/article/2026/07/home-affairs-confirms-sweeping-visa-changes/
news_date: 2026-07-21
directive_signed: 2026-07-08
directive_effective: immediate
target_duration_seconds: 20
video_clip_duration_seconds: 5
aspect_ratio: "9:16"
higgsfield_model: kling-video/v2.1/pro/image-to-video
```
