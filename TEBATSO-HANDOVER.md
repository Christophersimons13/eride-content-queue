# eMigration Assist — AI Reel Pipeline Handover

**For:** Tebatso Motswai
**From:** Michael Brits
**Date:** 28 July 2026
**Status:** Production-ready. Two v2 Reels already rendered. You'll be the second producer.

---

## What this is

A fully automated pipeline that turns a written brief into a finished 45-second vertical Reel (for Instagram/TikTok/YouTube Shorts). No filming. No editing software. You write a brief, run one command, and ~10 minutes later you have two MP4s (voiced + silent).

**Every Reel costs roughly $6–10 in API credits and takes ~10 minutes of wall-clock time.** Compare that to a studio shoot day.

## The four moving parts

| # | Service | What it does | Roughly |
|---|---------|--------------|---------|
| 1 | **Higgsfield Soul V2** | Generates 6 SA-authentic still images from text prompts | ~$0.10 per image |
| 2 | **Higgsfield Kling** | Animates each still into a 5s or 10s video clip | ~$0.75–1.50 per clip |
| 3 | **ElevenLabs** | Generates the voiceover from a script (Andrew SA voice) | ~$0.15 for a 45s reel |
| 4 | **Shotstack** | Stitches everything together — clips, voice, logo, captions, disclosure | Free on stage, ~$0.80 on production |

**On top of those:** Perplexity Computer (this, where you write the brief) and Claude Code (where the pipeline actually executes on your Windows machine).

---

## Part 1 — What to install on your Windows machine

Do these steps in order. Skip nothing.

### 1.1 — Node.js

Claude Code runs on Node.js. Without it, nothing else works.

1. Go to https://nodejs.org
2. Download the **LTS version** (the green button)
3. Run the installer, accept all defaults
4. Open **PowerShell** (search "PowerShell" in Start menu)
5. Type `node --version` and press Enter
6. You should see something like `v24.x.x`. If you do, Node.js is installed.

### 1.2 — Claude Code

This is the AI agent that actually runs the pipeline on your machine.

1. In PowerShell, type: `npm install -g @anthropic-ai/claude-code`
2. Wait for it to finish (~2 minutes)
3. Type `claude --version`
4. You should see something like `2.1.x`

You will need an **Anthropic API key** or a Claude subscription. Ask Michael for the shared team key.

### 1.3 — Perplexity Computer

This is where you do the strategy work — writing briefs, iterating on scripts, reviewing renders.

1. Go to https://www.perplexity.ai
2. Log in with your work email
3. Ask Michael to add you to the Eride Perplexity project so you see the shared sessions

You'll use Computer (the interface you're reading this in) to draft briefs and copy-paste commands into Claude Code.

### 1.4 — Perplexity MCP connection to Claude Code

This wires Perplexity's tools into Claude Code so it can fetch briefs from GitHub directly.

Follow the guide: [Perplexity MCP Integration Guide — Claude Desktop & Claude Code](https://github.com/Christophersimons13/eride-content-queue/blob/main/docs/perplexity-mcp-integration.md) (Michael can point you to the exact file — it's already saved in workspace).

### 1.5 — The credentials file

Every API needs a key. To keep them out of chat and out of scripts, we store them in a single local text file. Never share this file. Never paste its contents into a chat window.

1. Create a folder on your Desktop called `emigration-pipeline`
2. Inside that folder, create a file called `higgsfield-keys.txt`
3. Michael will send you the file contents via a secure channel (not Telegram, not email — use a password manager share or in person)
4. The file has this structure:

```
HF_API_KEY=<the key>
HF_SECRET=<the secret>
ELEVENLABS_API_KEY=<the key>
SHOTSTACK_API_KEY_STAGE=<the stage key>
SHOTSTACK_API_KEY_PROD=<the prod key>
```

**Important quirk:** the file has stray `<` and `>` characters around the values. When Claude Code parses it, it will strip them automatically. Don't remove them by hand — just paste as Michael sends.

### 1.6 — Git (optional but recommended)

Not strictly required, but useful for fetching briefs from the repo without going through the browser.

1. Download from https://git-scm.com/download/win
2. Run the installer, accept all defaults

---

## Part 2 — How the pipeline actually works

Here's the mental model. Once you understand this, every step below makes sense.

```
   YOU (Perplexity Computer)
   │
   │  1. Write brief in Markdown
   │  2. Push brief to GitHub
   │  3. Compose "Claude Code command"
   │
   ▼
   YOU (paste command into Claude Code)
   │
   ▼
   CLAUDE CODE (running on your Windows machine)
   │
   │  4. Fetches brief from GitHub
   │  5. Reads credentials from higgsfield-keys.txt
   │  6. Calls Higgsfield Soul → gets 6 images
   │  7. Calls Higgsfield Kling → animates each into a clip
   │  8. Calls ElevenLabs → generates voiceover
   │  9. Calls Shotstack → composites everything with logo + disclosure
   │  10. Returns two MP4 URLs
   │
   ▼
   YOU (review videos)
   │
   ▼
   Approved → Shotstack production render (no watermark) → Post
   Rejected → Iterate brief → Loop back to step 1
```

The key insight: **Perplexity Computer is your creative studio, Claude Code is your production line.** You never leave Perplexity to plan or iterate. You only go to Claude Code to actually spend money.

---

## Part 3 — The four APIs, one by one

Read these once so you know what's happening under the hood. You won't call them directly — Claude Code does — but if something breaks, this is what breaks.

### 3.1 — Higgsfield Soul V2 (image generation)

**Endpoint:** `POST https://platform.higgsfield.ai/higgsfield-ai/soul/v2/standard`

**Headers:**
```
Content-Type: application/json
hf-api-key: <HF_API_KEY>
hf-secret: <HF_SECRET>
```

**Body (must be flat, not nested):**
```json
{
  "prompt": "Beitbridge border, official South African checkpoint, dusk, editorial photography style",
  "aspect_ratio": "9:16",
  "resolution": "1080p",
  "batch_size": 1,
  "enhance_prompt": true
}
```

**Common pitfall:** the official docs mention `/v1/text2image/soul` — that path is **wrong**. Use `/higgsfield-ai/soul/v2/standard`. Also, the auth uses **two separate headers** (`hf-api-key` and `hf-secret`), NOT a combined `Authorization: Key key:secret` header. That combined format is only for Kling.

### 3.2 — Higgsfield Kling (image-to-video)

**Endpoint:** `POST https://platform.higgsfield.ai/kling-video/v2.1/pro/image-to-video`

**Headers:**
```
Authorization: Key <HF_API_KEY>:<HF_SECRET>
Content-Type: application/json
```

**Body:**
```json
{
  "image_url": "<url of the Soul image>",
  "prompt": "Slow zoom in, natural motion, editorial cinematic style",
  "duration": 5
}
```

**Common pitfall:** Kling has historically only accepted `duration: 5` or `duration: 10`. Do not try arbitrary numbers like 6 or 8 unless you've tested — the API will silently freeze on the last frame if you get this wrong. If you need a 7s clip, generate 10s and trim in Shotstack.

### 3.3 — ElevenLabs (voiceover)

**Endpoint:** `POST https://api.elevenlabs.io/v1/text-to-speech/P1LmKcX63Ihgqy11sVRt`

The voice ID `P1LmKcX63Ihgqy11sVRt` is **Andrew, SA English male**. Locked in as our brand voice for the deportation series.

**Headers:**
```
xi-api-key: <ELEVENLABS_API_KEY>
Content-Type: application/json
```

**Body:**
```json
{
  "text": "The full voiceover script here...",
  "model_id": "eleven_multilingual_v2",
  "voice_settings": {
    "stability": 0.55,
    "similarity_boost": 0.75,
    "style": 0.20,
    "use_speaker_boost": true
  }
}
```

Do not change the voice ID or the settings without checking with Michael first — consistency across Reels is more valuable than tweaking any single one.

### 3.4 — Shotstack (composition)

**Endpoints:**
- Stage (free, watermarked): `POST https://api.shotstack.io/edit/stage/render`
- Production (paid, no watermark): `POST https://api.shotstack.io/edit/v1/render`

**Headers:**
```
x-api-key: <SHOTSTACK_API_KEY_STAGE or _PROD>
Content-Type: application/json
```

The body is a JSON timeline describing every clip, caption, logo, and audio track. Claude Code builds this from the brief.

**Common pitfall:** never use non-ASCII characters in on-screen text (no middle-dot `·`, no em-dash `—`, no bullet `•`). PowerShell 5.1's `Invoke-RestMethod` mangles them into `\u00b7` or `Â·` no matter what encoding tricks you try. Use plain ASCII: pipe `|`, slash `/`, hyphen `-`. This cost me 3 wasted render pairs on 27 July.

**Also:** always render on stage first (free), review, then submit to production. Never go straight to production.

---

## Part 4 — Repo structure

Everything lives at https://github.com/Christophersimons13/eride-content-queue (currently public so Claude Code can fetch briefs without authentication).

```
eride-content-queue/
├── AUTOMATION-SPEC.md      ← the master pipeline specification
├── TEBATSO-HANDOVER.md     ← this document
├── README.md
├── pending/                ← briefs waiting to be rendered
│   ├── 2026-07-27-ai-pipeline-02-deportation-crackdown-v2.md
│   └── ...
├── in-progress/            ← briefs currently being rendered
├── approved/               ← briefs that have been reviewed and approved
├── published/              ← briefs whose Reels are live
└── assets/
    └── brand/
        ├── ema-logo.png           ← navy version (for light scenes)
        ├── ema-logo-white.png     ← white version (for dark scenes — default)
        ├── ema-logo.svg
        └── ema-logo-white.svg
```

**Workflow:** you write a brief → save to `pending/` → run pipeline → if approved, move to `approved/` → once posted, move to `published/`.

---

## Part 5 — First run: reproduce the deportation Reel v2

Do not start with a new brief. First, reproduce what's already been made. That way you know the system works end-to-end on your machine before you spend time on new creative.

### Step 1 — Fetch the existing brief

Open your browser and go to:
https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/pending/2026-07-27-ai-pipeline-02-deportation-crackdown-v2.md

Save it locally so you can read it alongside the render.

### Step 2 — Start a fresh Claude Code session

1. Open PowerShell
2. Type `cd $HOME\Desktop\emigration-pipeline`
3. Type `claude`
4. Wait for the prompt

### Step 3 — Paste this command

```
Reproduce the deportation Reel v2 render.

Context:
- Brief: https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/pending/2026-07-27-ai-pipeline-02-deportation-crackdown-v2.md
- Credentials: C:\Users\<YourUsername>\Desktop\emigration-pipeline\higgsfield-keys.txt
  File has stray < > characters — strip them when parsing.

Pipeline:
1. Higgsfield Soul V2 → 6 SA images (endpoint /higgsfield-ai/soul/v2/standard, TWO separate hf-api-key + hf-secret headers, flat body with aspect_ratio 9:16 and resolution 1080p)
2. Higgsfield Kling → animate each (endpoint /kling-video/v2.1/pro/image-to-video, Authorization: Key KEY:SECRET, duration 5 or 10 only)
3. ElevenLabs → voiceover with voice P1LmKcX63Ihgqy11sVRt (Andrew SA), model eleven_multilingual_v2, stability 0.55, similarity_boost 0.75, style 0.20, use_speaker_boost true
4. Shotstack (STAGE, not production) → composite with:
   - White logo overlay bottom-right, ~15% width, ~4% margin, visible full duration
     (https://raw.githubusercontent.com/Christophersimons13/eride-content-queue/main/assets/brand/ema-logo-white.png)
   - "AI-GENERATED B-ROLL" corner label bottom-left, opacity 0.6, visible 2.5s to 41s
   - CTA card at 0:39-0:44 reading "EMIGRATIONASSIST.CO.ZA | LINK IN BIO" (ASCII pipe, no non-ASCII characters anywhere)

Constraints:
- Never use non-ASCII characters in Shotstack on-screen text
- Show me the Shotstack JSON before submitting
- Stage tier only, do not touch production
- Do not proceed past any 500 or 422 error without stopping to explain

Return the two output URLs (voiced + silent) when done.
```

### Step 4 — Watch what happens

Claude Code will:
1. Ask a clarifying question or two (answer them honestly — that's a good sign, not a bad one)
2. Fetch the brief from GitHub
3. Read your credentials file
4. Show you the Soul API request body — approve it
5. Call Soul six times (should take ~90 seconds)
6. Call Kling six times (should take ~5 minutes)
7. Call ElevenLabs once (~15 seconds)
8. Show you the Shotstack JSON — spot-check that the CTA card reads correctly and the pipe character is a real pipe
9. Submit to Shotstack twice (voiced + silent) — each takes ~90 seconds
10. Return two S3 URLs

Total: ~10 minutes of wall-clock time. Total cost: ~$6–10.

### Step 5 — Download both MP4s and watch them

Click each S3 URL, download, watch. You should see:
- Six SA-authentic scenes (Beitbridge, Home Affairs queue, ZA passport, immigration official, migrant worker, hand signing)
- Andrew's SA-English voiceover matching the visuals
- White EMA logo bottom-right the whole time
- "AI-GENERATED B-ROLL" label bottom-left during the b-roll
- Clear `EMIGRATIONASSIST.CO.ZA | LINK IN BIO` on the final frame

**If all of that is present, the pipeline is working on your machine.**

### Step 6 — Ping Michael

Send him the two S3 URLs. He'll confirm they match the ones he rendered on 27 July.

---

## Part 6 — Producing a new Reel from scratch

Once step 5 succeeds, you're ready to make new content. Here's the loop:

1. **In Perplexity Computer**, describe what you want:
   > "I want a 45s Reel about the new visa waiver rules for Botswana. Same structure as the deportation Reel — SA-specific imagery, fear-based hook, tightened CTA."

2. Perplexity will draft:
   - The voiceover script (~110 words)
   - Six Higgsfield Soul prompts for SA-authentic images
   - Six Kling animation prompts
   - The Shotstack timeline outline
   - The AI-disclosure copy

3. Iterate with Perplexity until you're happy with the script and the scene list. **This is where most of the creative work happens.**

4. Ask Perplexity to write the brief in the same format as `2026-07-27-ai-pipeline-02-deportation-crackdown-v2.md` and push it to `pending/` in the repo.

5. Ask Perplexity to compose the Claude Code command with the URL of the new brief.

6. Copy that command, paste into Claude Code. Follow Part 5, steps 4-6.

7. If the stage render is good, tell Claude Code:
   > "Approved. Submit both to production tier for the final MP4s."

8. Download the production files (no watermark), post to your channels, move the brief from `pending/` to `published/`.

---

## Part 7 — Non-negotiables

Break these and you'll cost the company money and possibly reputation.

1. **Never paste API keys into any chat window** — Perplexity, Claude Code, Telegram, WhatsApp, none. Keys go in the local text file only. If you accidentally paste one, tell Michael immediately so he can rotate it.

2. **Stage tier first, always.** Never render on Shotstack production tier until stage is reviewed and approved. Production costs money per render — stage is free trial credits.

3. **AI-GENERATED B-ROLL disclosure must appear on every Reel** that uses generative video. Meta and TikTok require this. Do not remove the corner label.

4. **In-app disclosure toggle must be ON at upload** on both Meta Business Suite and TikTok. This is separate from the corner label — both are required.

5. **No non-ASCII characters in Shotstack on-screen text.** Middle-dot, em-dash, bullet — banned. Use pipe `|`, slash `/`, hyphen `-`.

6. **If something breaks, stop.** Do not retry blindly. Claude Code is very good at stopping and asking — trust it. A 500 error retried three times is money down the drain.

7. **Voice consistency.** Andrew (`P1LmKcX63Ihgqy11sVRt`) is our brand voice. Do not switch voices between Reels in the same series without approval.

8. **Logo lock.** The two logo PNGs in the repo are the only approved versions. Do not use the JPG that's still there for legacy reasons — it will be removed soon.

---

## Part 8 — What Perplexity does vs. what Claude Code does

Simple rule that will save you a lot of confusion:

**Perplexity Computer = thinking**
- Drafting scripts
- Iterating on visual prompts
- Researching immigration news
- Reviewing renders
- Writing briefs
- Composing Claude Code commands
- Answering strategic questions

**Claude Code = doing**
- Actually calling the APIs
- Actually spending money
- Actually generating files
- Running PowerShell commands
- Managing local files on your Windows machine

If you catch yourself asking Claude Code to help you brainstorm, stop. Come back to Perplexity. If you catch yourself asking Perplexity to render a video, stop. Perplexity doesn't have your keys and doesn't run on your machine.

---

## Part 9 — Troubleshooting quick reference

| Symptom | Likely cause | Fix |
|---------|--------------|-----|
| Soul returns 500 | Wrong endpoint path or nested body | Use `/higgsfield-ai/soul/v2/standard` with flat body |
| Soul returns 422 | Credentials have stray `<` `>` in them | Strip them in the parse step |
| Kling clip freezes on last frame | Duration mismatch — clip is shorter than the Shotstack length slot | Match durations exactly, or use `duration: 10` and trim |
| Shotstack CTA text shows `\u00b7` or `Â·` | Non-ASCII character being mangled by PowerShell | Use pipe `|` — never middle-dot |
| Claude Code says "session limit" | Anthropic session got too large | Start a fresh Claude Code terminal, paste more context |
| Kling CloudFront URL 403s | Signed URL expired (24-48h) | Regenerate that clip only, not the whole batch |
| Higgsfield returns "content moderation" | Prompt contains politically sensitive keywords | Soften the language, avoid naming specific officials |

---

## Part 10 — Contacts and channels

- **Michael Brits** — pipeline owner, final approval on content
- **GitHub repo** — https://github.com/Christophersimons13/eride-content-queue
- **Perplexity project** — Eride team space (Michael will add you)
- **Telegram** — Eride Content channel for day-to-day coordination
- **Shared credentials file** — Michael will send via password manager only

---

## Appendix — The two v2 Reels already produced

For reference. These are stage renders (watermarked). Production versions are on Michael's local machine, unposted as of 28 July.

- **Voiced:** https://shotstack-api-stage-output.s3-ap-southeast-2.amazonaws.com/4rddvk34xl/f26399bf-2aa4-494f-8dbc-161cfd274a43.mp4
- **Silent:** https://shotstack-api-stage-output.s3-ap-southeast-2.amazonaws.com/4rddvk34xl/82b9af2e-7070-4f03-b7db-b0982d88a756.mp4

These are the golden reference. Anything you produce should feel like it belongs alongside them.

---

**End of handover. Any questions, ping Michael directly. Welcome to the production line.**
