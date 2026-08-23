# klm-website

Personal portfolio + blog, built with [Astro](https://astro.build).

## Local development

```sh
npm install
npm run dev       # http://localhost:4321
npm run build     # static output in dist/
npm run preview   # preview the production build locally
```

## Adding content

**A new blog post**: add a Markdown file to `src/content/blog/`, e.g.
`src/content/blog/my-new-post.md`:

```md
---
title: "My New Post"
description: "One-line summary shown in the blog list."
date: 2026-09-01
tags: ["tag1", "tag2"]
---

Post content goes here, in Markdown.
```

The URL slug comes from the filename (`my-new-post` → `/blog/my-new-post/`).
Set `draft: true` in the frontmatter to keep a post out of the listing until
it's ready.

**A new project**: add a Markdown file to `src/content/projects/`, same
frontmatter shape (see `src/content/projects/example-project.md`) — it'll
show up automatically on the `/projects/` page.

## Deploying to GitHub Pages

1. Push this repo to GitHub. For the cleanest URL (no `/repo-name/` path),
   name the repo `<your-username>.github.io`.
2. In the repo's **Settings → Pages**, set the source to **GitHub Actions**.
3. Update `astro.config.mjs` — set `site` to your actual Pages URL
   (e.g. `https://your-username.github.io`). If you're using a *project*
   repo instead of a `<username>.github.io` user site, also set
   `base: '/your-repo-name'`.
4. Push to `main` — `.github/workflows/deploy.yml` builds and deploys
   automatically.

## Adding more "dynamic" touches later

The site currently ships zero client-side JS by default (Astro's default).
When you want an interactive widget (a canvas background, a theme toggle,
etc.), you can:

- Add plain `<script>` tags directly in an `.astro` file for small vanilla
  JS behavior, or
- Run `npx astro add react` (or `svelte`/`vue`) to add a UI framework and
  drop in an interactive "island" component without restructuring anything
  else.

Page transitions are already enabled via Astro's `<ClientRouter />`
(`src/layouts/BaseLayout.astro`).
