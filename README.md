# Webium Astro Blog

Webium has been refactored from a Blogger theme build into a static Astro blog that deploys cleanly to Vercel.

## Stack

- Astro
- Markdown content collections
- Static output for Vercel

## Local development

```bash
npm install
npm run dev
```

## Production build

```bash
npm run build
```

The generated site is written to `dist/`.

## Content workflow

Add posts in `src/content/blog/*.md`.

Each post uses frontmatter like this:

```md
---
title: "Post title"
description: "Short summary"
publishedAt: 2026-04-24
author: "Your Name"
category: "Notes"
tags:
  - Astro
  - Vercel
featured: false
draft: false
---
```

## Files to customize

- `astro.config.mjs`: set your real site URL
- `src/consts.ts`: site title, description, navigation
- `src/pages/index.astro`: homepage copy
- `src/styles/global.css`: visual design

## Vercel deployment

This repo now uses:

- Install command: `npm install`
- Build command: `npm run build`
- Output directory: `dist`

Vercel usually detects Astro automatically, but those settings are the expected values if you configure them manually.
