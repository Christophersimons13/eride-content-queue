# Eride Content Automation — Perplexity → Claude Code → Higgsfield → Approval → Post

**Author:** Michael Brits (via Perplexity Computer session, 27 July 2026)
**Owner (implementation):** Joshua Ratau or Eride dev team
**Status:** Design spec — bridge read-side proven, awaiting build

---

## 1. Objective

Reduce the effort of producing short-form video content (Instagram Reels, TikTok, YouTube Shorts) for Eride Technologies products from ~2 hours per video to **~5 minutes of human decision-making**, with a single approval click before publication.

## 2. Non-Objectives

- Fully autonomous posting without human review. Every video passes through an approval gate.
- Real-time (< 1 minute) turnaround. Target latency is ~5–15 minutes end-to-end per video.
- Replacing human creative direction. Humans still choose topics, tone, and campaign strategy.

---

## 3. High-Level Flow

```
┌───────────────┐   1. brief    ┌─────────┐   2. read   ┌─────────────┐
│  Perplexity   │──────────────▶│  GitHub │────────────▶│ Claude Code │
│  (Michael's   │  push .md     │ (queue) │  fetch      │ (laptop)    │
│  Computer)    │               │         │             │             │
└───────────────┘               └─────────┘             └──────┬──────┘
                                     ▲                        │
                                     │ 6. status update       │ 3. call Higgsfield
                                     │                        ▼
                                ┌────┴─────┐            ┌─────────────┐
                                │ Approval │◀───────────│ Higgsfield  │
                                │ (Telegram│  4. video  │  API        │
                                │  or web) │  URL       └─────────────┘
                                └────┬─────┘
                                     │ 5. approve
                                     ▼
                              ┌──────────────┐
                              │  Publisher   │
                              │  (Meta API / │
                              │   Buffer /   │
                              │   manual)    │
                              └──────────────┘
```

---

## 4. Stage-by-Stage Specification

### Stage 1 — Brief Authoring (Perplexity → GitHub)

**Actor:** Perplexity Computer (this chat)
**Trigger:** Michael asks in a Perplexity chat: *"Write a Reel about [topic] for [product]."*
**Output:** A Markdown file with YAML frontmatter pushed to `eride-content-queue/pending/`.

**File naming:** `YYYY-MM-DD-slug.md` (e.g. `2026-07-27-emigration-visa-tips.md`)

**Frontmatter schema (required fields):**

```yaml
---
id: string                    # matches filename slug
product: e-migration-assist   # 8beauty | e-migration-assist | e-moola | companio | bantry-cycle-house
platform: instagram-reels     # instagram-reels | tiktok | youtube-shorts
duration_seconds: 30          # 15 | 30 | 60 | 90
aspect_ratio: 9:16
voice: female-warm            # or male-authoritative | female-energetic | none
music: cinematic-slow         # or upbeat | jazz | ambient | none
language: en                  # en | af | zu | st
target_audience: string       # e.g. "South African professionals considering emigration"
call_to_action: string        # e.g. "Book a free consultation at emigrationassist.com"
status: pending
priority: normal              # normal | high | urgent
created_by: perplexity
created_at: ISO8601 timestamp
approver: michael             # who signs off
---
```

**Body schema:**

```markdown
# [Video title]

## Hook (0–3s)
[Attention-grabbing opening line]

## Shot list
1. [0–3s] wide establishing shot: description
2. [3–8s] medium shot: description
3. [8–15s] close-up: description
...

## Voiceover script
[Timed, punctuated for TTS. One idea per line.]

## On-screen captions
[Short punchy overlays, one per shot]

## Hashtags
#eMigration #SouthAfrica #EmigrationAdvice ...

## Higgsfield prompt (composed for API)
[The exact prompt string Claude Code will send to Higgsfield, pre-composed with all
visual, motion, and style parameters filled in.]
```

**Success criterion:** File is committed to `main` branch of `eride-content-queue`, appears in `pending/`, and Michael sees a Perplexity chat confirmation with the GitHub file URL.

---

### Stage 2 — Ingestion (GitHub → Claude Code)

**Actor:** Claude Code on Michael's Windows laptop (Omnibook).
**Trigger:** Michael launches `claude` in a terminal and prompts:
> *"Check the eride-content-queue for new briefs and process the oldest one in pending/."*

**Required tools on the laptop (missing today, must install):**
- `git` (via `winget install Git.Git`)
- `gh` CLI (via `winget install GitHub.cli`)
- `gh auth login` completed against `Christophersimons13`

**Steps Claude Code performs:**

1. Clone or pull the repo to a local working directory (e.g. `C:\Users\Omnibook\eride-content-queue`).
2. List files in `pending/` sorted by `created_at`.
3. Read the oldest file. Parse frontmatter.
4. Move the file to `in-progress/` with a git commit: `"Start processing <id>"`.
5. Extract the composed Higgsfield prompt from the body.
6. Update frontmatter: `status: in-progress`, `picked_up_at: <ISO now>`.

**Guardrails:**
- Claude Code prompts Michael for approval before every git push (this is the built-in Claude Code behavior — do not try to disable it).
- Skip any file whose frontmatter doesn't validate against the schema.
- If pending/ is empty, report "no work" and exit cleanly.

---

### Stage 3 — Video Generation (Claude Code → Higgsfield)

**Actor:** Claude Code, calling the Higgsfield API.

**Prerequisite:** Higgsfield API access. Two options:

**Option A — Direct HTTPS from Claude Code (recommended):**
- Higgsfield exposes a REST API (verify at [higgsfield.ai/api](https://higgsfield.ai) — endpoint and auth pattern TBD).
- Store `HIGGSFIELD_API_KEY` in a `.env` file at `C:\Users\Omnibook\.higgsfield-env` (never committed to the repo).
- Claude Code uses PowerShell/curl to POST the composed prompt.

**Option B — Higgsfield MCP server (if one exists):**
- Search the MCP registry ([modelcontextprotocol.io/servers](https://modelcontextprotocol.io/servers)) for `higgsfield`.
- If available, add it to Claude Code with:
  ```
  claude mcp add higgsfield --env HIGGSFIELD_API_KEY=<key> -- cmd /c npx -y <package-name>
  ```
- Same install pattern we used for Perplexity.

**Steps Claude Code performs:**

1. POST the composed prompt to Higgsfield with the aspect ratio, duration, and style parameters from the brief.
2. Poll the returned job ID until the video is ready (Higgsfield renders are async; typically 2–5 min).
3. Download the video URL and MP4 file to `C:\Users\Omnibook\eride-content-queue\videos\<id>.mp4`.
4. Update the brief's frontmatter: `video_url: <higgsfield URL>`, `video_generated_at: <ISO now>`.
5. Commit and push.

**Failure handling:**
- Timeout after 10 minutes → mark `status: failed`, `error: timeout`, move file to `pending/` for retry.
- API error 429 (rate limit) → wait 60s, retry once.
- API error 4xx (bad prompt) → mark `status: failed`, `error: <message>`, alert Michael via Telegram.

---

### Stage 4 — Approval Notification

**Actor:** Claude Code sends a Telegram message via the `telegram_bot_api__pipedream` connector Michael already has.

**Message format:**

```
🎬 Video ready for approval

Title: [title]
Product: [product] · Platform: [platform] · Duration: [duration]s
Video: [higgsfield URL]

Approve? Reply with:
  /approve <id>   → moves to approved/, posts to platform
  /reject <id> "reason"   → moves back to pending/ with error note
  /skip <id>   → moves to archived/, no post
```

**Alternative approval channels:**
- **Email** via Outlook connector (fallback).
- **Simple web dashboard** — a static page rendered from `pending/`, `in-progress/`, `approved/` — hosted on GitHub Pages or Vercel. Michael clicks Approve/Reject; a Vercel serverless function calls the GitHub API to move files.

**Recommended for MVP:** Telegram, because Michael already uses it heavily and the bot connector is live.

---

### Stage 5 — Publishing

**Actor:** A **posting worker** (separate from Claude Code — this is where a lightweight always-on script fits).

**Options:**

| Option | Pros | Cons |
|---|---|---|
| **Manual post** | Zero setup. Michael/team downloads video from GitHub, uploads to Meta/TikTok/YouTube manually. | Least automated. |
| **Buffer/Later API** | Handles multi-platform scheduling. Buffer has a Free tier. | Extra tool, monthly cost past free tier. |
| **Meta Graph API + TikTok Content Posting API** | Direct posting, fully automated. | Requires app review, ~2 weeks setup, ongoing token management. |
| **GitHub Actions + n8n webhook** | Fires on push to `approved/`, posts via Buffer or platform APIs. | Middleware to maintain. |

**Recommended for MVP:** **Manual post** for the first 5–10 videos while the pipeline stabilises. Add Buffer once volume justifies it.

**On successful publish:**
- Move brief from `approved/` to `published/`.
- Update frontmatter: `published_at`, `published_url` (Instagram/TikTok/YouTube link).
- Optional: post a "published ✅" confirmation back to Telegram.

---

## 5. Roles & Responsibilities

| Role | Actor | What they do |
|---|---|---|
| **Author** | Michael + Perplexity | Decides topics, prompts Perplexity to write briefs |
| **Orchestrator** | Claude Code | Reads pending briefs, calls Higgsfield, moves files |
| **Video renderer** | Higgsfield API | Turns prompts into MP4 |
| **Approver** | Michael | Clicks approve/reject in Telegram |
| **Publisher** | Manual (Phupho? Michael?) or Buffer worker | Posts to Meta/TikTok/YouTube |

## 6. Data Retention & Cleanup

- `published/` — keep 90 days, then delete video files (keep the .md brief for records).
- `videos/` folder — mirror to Google Drive or S3 monthly; git LFS optional for large volume.
- Never commit API keys, Higgsfield tokens, or Perplexity keys to the repo. Use `.env` files at machine level.

## 7. Security Notes

- **API keys stored in `.env` files at OS level**, never in the repo. Add `.env`, `*.key`, `secrets/` to `.gitignore`.
- **Repo stays private.** Public was only used for the bridge test.
- **`.gitignore`** must include: `.env`, `secrets/`, `*.mp4`, `videos/`.
- **Telegram bot token** kept in a Windows environment variable (`TELEGRAM_BOT_TOKEN`), not in the repo.
- **Rotate API keys** every 90 days on a calendar reminder.

## 8. Cost Estimate (Monthly, Order-of-Magnitude)

Assumes 20 videos/month, 30s each.

| Component | Estimated cost | Notes |
|---|---|---|
| Perplexity API (brief writing) | $5–15 | ~1M tokens/mo at Sonar pricing |
| Anthropic (Claude Code sessions) | Included in Claude Pro | If usage stays under Pro cap |
| Higgsfield | $50–150 | Depends on plan and quality tier |
| GitHub | $0 | Private repos free on personal accounts |
| Telegram | $0 | Free |
| Buffer (if adopted) | $6–15 | Essentials tier |
| **Total** | **~$60–180/mo** | For 20 videos |

Compare to current cost (manual, ~2h/video @ ~$25/h = $50/video, 20 videos = $1,000/mo of Michael's time). ROI is strong.

## 9. Rollout Plan

**Phase 0 (this session — done):**
- ✅ Perplexity MCP wired into Claude Desktop and Claude Code.
- ✅ GitHub bridge repo created (`eride-content-queue`, private).
- ✅ Read side of the bridge proven.

**Phase 1 — Bridge write side (2 hours of work):**
- Install `git` and `gh` on Michael's laptop.
- Test end-to-end: Perplexity pushes a brief, Claude Code reads it, edits frontmatter, pushes back.

**Phase 2 — Higgsfield integration (1 day):**
- Verify Higgsfield API access. Get key, test one manual API call from a terminal.
- Have Claude Code call the API from a brief. Save video URL back to the brief.

**Phase 3 — Telegram approval (half day):**
- Wire the `telegram_bot_api__pipedream` connector to send approval messages.
- Build simple command handlers: `/approve`, `/reject`, `/skip`.

**Phase 4 — Publishing (variable):**
- Start with manual posting.
- After 5–10 approved videos, evaluate whether to automate via Buffer or Meta API.

**Phase 5 — Scale (ongoing):**
- Add second and third products (currently spec assumes one at a time).
- Add analytics: which briefs → highest engagement.
- Add A/B testing: two Higgsfield prompts per brief, post both, compare.

## 10. Open Questions

1. **Does Higgsfield have an official API?** — Need to verify. If not, the pipeline stalls until they release one or a scraper is built (fragile, not recommended).
2. **Which products get automation first?** — Suggest E-Migration Assist (highest content demand, clearest brand voice).
3. **Who handles manual posting during MVP?** — Michael, Phupho, Koketso?
4. **Language mix per product?** — E-Migration Assist likely English + Afrikaans. 8Beauty may want isiZulu and Sesotho. Affects brief templates.
5. **Brand voice guardrails per product?** — Need one-page brand voice sheets per product for Perplexity to reference.

## 11. Success Metrics (After 30 Days of Operation)

- Time from Michael requesting a brief to approved video: **under 15 minutes** (target).
- Approval rate on first render: **> 60%** (below this, brief templates need tuning).
- Videos published per week: **≥ 5** per active product.
- Zero API keys leaked or committed to the repo.

---

## 12. Immediate Next Actions

For Michael to execute:

- [ ] Rotate the leaked Perplexity API key (`pplx-vTZu1u86cCneh...`) at [perplexity.ai/settings/api](https://www.perplexity.ai/settings/api).
- [ ] Install `git` and `gh` on the laptop: `winget install Git.Git` and `winget install GitHub.cli`.
- [ ] Run `gh auth login` and authenticate as `Christophersimons13`.
- [ ] Confirm Higgsfield API availability (check plan, get docs link, obtain API key).
- [ ] Decide first product for automation (recommend E-Migration Assist).

For me (next Perplexity session):

- [ ] Write the brand voice sheet for the chosen first product.
- [ ] Write brief template v1 (fully populated for the chosen product).
- [ ] Ship first real brief to `pending/` for a live end-to-end test.

For Joshua / dev team (once phases 1–2 are validated):

- [ ] Build the Telegram approval bot handlers.
- [ ] Wire publishing (manual → Buffer → API depending on volume).
- [ ] Add monitoring: Slack/Telegram alert if a brief sits in `in-progress/` for > 30 min (stuck).
