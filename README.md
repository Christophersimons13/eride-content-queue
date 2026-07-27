# Eride Content Queue

Automation bridge between Perplexity (script author) and Claude Code (video generator).

## Folder structure

- `pending/` — Perplexity drops new briefs here. Claude Code polls this folder.
- `in-progress/` — Claude Code moves a brief here while generating.
- `approved/` — Michael moves briefs here after reviewing the generated video.
- `published/` — After posting, briefs are archived here.

## Brief format

Each brief is a Markdown file named `YYYY-MM-DD-slug.md` with YAML frontmatter:

```yaml
---
id: 2026-07-27-table-mountain-safety
platform: instagram-reels
duration_seconds: 30
aspect_ratio: 9:16
voice: female-warm
music: cinematic-slow
status: pending
created_by: perplexity
created_at: 2026-07-27T08:30:00+02:00
---
```

Body contains:
- Hook (0–3s)
- Shot list
- Voiceover script
- On-screen captions
- Hashtags
- Higgsfield prompt (fully composed for API)

## Claude Code workflow

In Claude Code on the laptop, run:

```
Read the newest file in pending/, generate the Higgsfield video using the composed prompt,
save the video URL to the file's frontmatter under `video_url:`, and move the file to in-progress/.
```
