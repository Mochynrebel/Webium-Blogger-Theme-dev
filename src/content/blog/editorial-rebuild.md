---
title: "Rebuilding a Blogger Theme Into a Real Astro Site"
description: "A practical migration path from platform-specific XML templates to a Vercel-ready publishing workflow."
publishedAt: 2026-04-24
author: "Webium Editorial"
category: "Migration"
tags:
  - Astro
  - Vercel
  - Migration
featured: true
---

The old Webium theme was optimized for Blogger's XML templating system. That made it useful inside Blogspot, but awkward everywhere else.

Moving to Astro changes the model entirely:

- Content becomes Markdown instead of platform-bound widget markup.
- Routing becomes file-based instead of template-driven.
- Deployment becomes a standard static build instead of a Blogger upload flow.

That shift matters because it removes the biggest blocker for modern hosting. Vercel expects a normal site build. Astro gives you exactly that without forcing a large client runtime onto a reading-first blog.

## What survived from the original theme

The design direction still matters:

- a strong editorial layout
- generous typography
- a narrow reading column
- lightweight navigation

Those traits were worth preserving. The Blogger-specific runtime was not.

## What changes for editing

You now add posts in `src/content/blog`. Each file carries its metadata in frontmatter, which means title, date, category, and tags all live next to the article body.

That is easier to version, easier to review, and easier to deploy.
