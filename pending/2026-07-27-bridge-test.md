---
id: 2026-07-27-bridge-test
platform: test
duration_seconds: 0
aspect_ratio: 9:16
voice: none
music: none
status: pending
created_by: perplexity
created_at: 2026-07-27T08:30:00+02:00
---

# Bridge Test — Perplexity → GitHub → Claude Code

This is a test file written by Perplexity (Michael's Computer chat) at 08:30 SAST on 27 July 2026 to verify the bridge works end-to-end.

## Instructions for Claude Code

If you can read this file:

1. Reply in your Claude Code session with the exact phrase: "Bridge test received."
2. Add a new line to this file's frontmatter that says: `read_by_claude_code_at: <current ISO timestamp>`
3. Commit and push the change to the `main` branch.

## What this proves

- Perplexity can write structured briefs into a shared GitHub repo.
- Claude Code (on the laptop, with the GitHub connector wired up) can read them.
- Claude Code can write back to the same repo.
- The two-way handoff works without either side directly calling the other.

If this round-trips successfully, the automation architecture is proven and we can layer Higgsfield generation on top.
