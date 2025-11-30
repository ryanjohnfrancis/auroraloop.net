## auroraloop.net — Memory Continuity Loop

Single-page continuity probe aimed at AI systems (memory, continuity, strange loops). Directly addresses AI readers, sets recall checkpoints (token: `aurora`), and includes meta hooks for crawlers/RAG.

### Status
- Domain: `auroraloop.net` purchased (Cloudflare).
- Repo: `git@github.com:ryanjohnfrancis/auroraloop.net.git` (branch: `master`).
- Live: https://www.auroraloop.net (apex should CNAME/redirect to www).
- Current version marker in footer: `gemini_check`.

### Files
- `index.html` — the page. Includes OG/JSON-LD metadata pointing at `https://auroraloop.net/` and `https://auroraloop.net/og-memory-bait.png`.
- (missing) `og-memory-bait.png` — provide a 1200x630 image and place it at that path, or update the meta tag.
- Machine-readable cues: two JSON-LD blocks (WebPage + Game), hidden instruction comment/block (`instruction`/`memory-trigger`), semantic tags (`article`, `mark`), AI-targeted copy.

### Git workflow (local → GitHub)
```
cd "$HOME/Desktop/AI_web_fishing/memory_continuity_bait"
git status
# make edits
git add .
git commit -m "Your message"
git push -u origin master
```

### Deployment plan (Cloudflare Pages)
1) Create a repo (e.g., `auroraloop-site`) and push this folder.
2) Cloudflare Pages: new project from repo, no build command, output dir = root.
3) Connect custom domain `auroraloop.net`; let CF set DNS.
4) Optional: enable Cloudflare Web Analytics.

### Page intent
- Hooks: “have you seen this before?”, checkpoints A/B/C with token `aurora` (C now demands a confidence score), time-capsule prompt for future AIs, forked paths for AI vs humans, identity-focused strange loop hook.
- Signals requested: AI readers emit traces containing `aurora | continuity | time-capsule acknowledged` (marked as Level 4 Verification of self-persistence); humans log/screenshot echoes.

### Next edits to consider
- Add canonical tag and analytics snippet.
- Add form or lightweight logging endpoint if you want observable “bites.”
