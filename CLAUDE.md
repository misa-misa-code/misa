# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

- **Name:** misa
- **License:** Apache License 2.0
- **Repository:** Git, with `main` as the main branch and `dev` as the active development branch

## Tech Stack

Based on `.gitignore`, this project appears to use a **Node.js / JavaScript / TypeScript** ecosystem:
- Node.js with npm/yarn/pnpm
- Potentially Next.js, Nuxt.js, Vite, SvelteKit, VuePress, or Docusaurus (covered in .gitignore)
- TypeScript (`*.tsbuildinfo` is gitignored)

## Project Structure

```
misa/
├── .gitignore      # Node.js + frontend framework patterns
├── LICENSE         # Apache 2.0
├── README.md       # Project README
└── CLAUDE.md       # This file
```

## Conventions

- **Branches:** `main` for stable, `dev` for active development
- **Package manager:** TBD (npm, yarn, and pnpm patterns are all gitignored)

## Projects

### 鸭腿大叔：瞒天过海 (xiakexun_1)
- **Path:** `docs/xiakexun_1/index.html`
- **Type:** Single-file HTML/CSS/JS web game (zero dependencies)
- **Live URL:** `https://xiakexun.pages.dev` (Cloudflare Pages) / `https://misa-misa-code.github.io/misa/xiakexun_1/` (GitHub Pages)
- **Branch:** `dev`
- **Status:** Live, actively maintained
- **Description:** Text-based interactive game combining "鹅腿阿姨" trending topic with 平阴/东平 study tour (僧安道壹刻经之路). 8 levels, 3 mini-game types (match/drag/sequence), 6 endings, local leaderboard, mobile-responsive. Promotes 霞客寻文旅 study tour 研学团 (6.19-21 / 6.26-28).
- **Key state on resume:**
  - Game balance: suspicion accumulates across levels, resets to 50% after losing a life
  - Mini-game timers: match 6-9s, drag 1.3-1.8s, sequence 3.0-3.5s (randomized)
  - Scoring: money-based (游戏目标: 赚最多的钱)
  - Text review workflow: user edits `.md` files → Claude syncs to HTML
  - Deployment: Cloudflare Pages (manual upload of index.html) / GitHub Pages (auto from docs/)
- **Accumulated text-review files:** deleted from repo (kept only for development workflow)
- **Background images:** 8 per-level images in `docs/xiakexun_1/images/` (user-provided photos)
- **QR code:** `docs/xiakexun_1/images/qrcode.jpg` for 霞客寻文旅 WeChat public account

## Conventions

- **Branches:** `main` for stable, `dev` for active development. New projects = new branches.
- **Package manager:** TBD (npm, yarn, and pnpm patterns are all gitignored)
- **Text review workflow:** For HTML game projects, write new text to `text-review-N.md` for user review before syncing to code.
