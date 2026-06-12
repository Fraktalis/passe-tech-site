# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static site for the French-language YouTube channel **Passe-Tech** (AI, DevOps, Medical 3D). Built with Astro, deployed to GitHub Pages at `https://src.passe-tech.fr`. YouTube video data is fetched at build time via the YouTube Data API v3.

## Commands

```bash
npm run dev       # Start dev server (localhost:4321)
npm run build     # Build static site to dist/
npm run preview   # Preview built site locally
```

A `.env` file with `YOUTUBE_API_KEY` and `YOUTUBE_CHANNEL_ID` is required for pages that fetch YouTube data (`index.astro`, `videos.astro`). See `.env.example`.

## Architecture

**Astro static site** — all output is pre-rendered HTML with no SSR.

- `src/pages/` — file-based routing. Each `.astro` file becomes a URL.
- `src/components/` — reusable Astro components (`Nav`, `Footer`, `VideoCard`).
- `src/layouts/Layout.astro` — wraps every page with `<head>`, nav, and footer.
- `src/content/resources/` — Markdown files, one per video, rendered on `/resources`.
- `src/styles/global.css` — all styling; defines the "watermelon palette" CSS vars (`--rose`, `--vert`, `--jaune`, `--cream`, `--bg`, `--card`, etc.) and utility classes (`.btn`, `.card`, `.section`, `.prose`).
- `public/` — static assets served as-is.

## Adding a resource (typical task)

Create a Markdown file in `src/content/resources/` with this frontmatter:

```yaml
---
title: "Title"
date: YYYY-MM-DD
video_url: "https://youtu.be/..."   # or "#" if no video yet
tags: ["tag1", "tag2"]
---
```

The slug used for deep-linking (`/resources#slug`) is derived from the filename (without `.md`).

## Deployment

Push to `master` triggers GitHub Actions (`deploy.yml`), which builds and deploys to GitHub Pages. The workflow also runs daily at 06:00 UTC so fresh YouTube data is picked up without a manual push.

## Stack constraints

- No React, Vue, or other component frameworks — pure Astro + vanilla JS.
- Strict TypeScript (`tsconfig.json` extends `astro/tsconfigs/strict`).
- Client-side interactivity on `/resources` (tag filtering, sort, deep-link) is plain vanilla JS inlined in the page — keep it that way unless scope significantly changes.
