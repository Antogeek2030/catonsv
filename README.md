# Catonsville Garage Doors

Astro static site for Catonsville Garage Doors — garage door repair, installation, and opener service in Catonsville, Arbutus, and surrounding Maryland areas.

**Live site target:** https://catonsvillegaragedoors.com  
**Address:** 1404 Parker Rd, Arbutus, MD 21227  
**Phone:** (410) 247-4567

## Features

- Responsive, mobile-friendly design
- LocalBusiness schema for fast Google indexing
- Sitemap (via `@astrojs/sitemap`) and `robots.txt`
- Blog section powered by Markdown content collections
- Service and problem pages for local SEO
- Optimized for Cloudflare Pages deployment

## Color scheme

Navy blue primary + orange accent (updated from the original teal template).

## Develop

```bash
npm install
npm run dev
```

## Build for Cloudflare Pages

```bash
npm install
npm run build
```

Output is in `dist/`. Connect the repo (or upload) to Cloudflare Pages:

- Build command: `npm run build`
- Output directory: `dist`
- Node version: 22 or higher

Trailing slash is enabled (`trailingSlash: 'always'`) to match directory-style URLs.

## Project structure

- `src/pages/` — routes (index, services, problems, blog, about, contact, service-areas)
- `src/content/blog/` — Markdown blog posts
- `src/content.config.ts` — content collection schema
- `src/components/` — Header, Footer
- `src/layouts/Layout.astro` — shared layout + SEO + schema
- `src/styles/global.css` — design system
- `public/robots.txt` — crawler rules + sitemap link

## Adding blog posts

Add a new `.md` file in `src/content/blog/` with frontmatter:

```yaml
---
title: "Your Title"
description: "Short description"
pubDate: 2026-10-26
author: "Catonsville Garage Doors"
---
```

It will appear on `/blog/` automatically after rebuild.
