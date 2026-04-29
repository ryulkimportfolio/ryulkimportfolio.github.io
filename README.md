# Minseong Kim — Personal Site

Personal quant portfolio + technical blog, deployed via GitHub Pages + Jekyll.

## Local development

**Prerequisites:** Ruby ≥ 3.1, Bundler

```bash
gem install bundler
bundle install
bundle exec jekyll serve --livereload
```

Open `http://localhost:4000`.

## Deployment

1. Create a GitHub repo named exactly `<yourusername>.github.io`
2. Push to the `main` branch
3. In **Settings → Pages**, set Source to `main` / `/ (root)`
4. Site auto-deploys in ~60 seconds

Update `url` and `baseurl` in `_config.yml` to match your username before pushing.

## Adding a post

Create a file in `_posts/` with the naming convention:

```
_posts/YYYY-MM-DD-slug.md
```

Frontmatter:

```yaml
---
layout: post
title: "Your Title"
date: 2026-05-01
slug: your-slug
tags: [Python, Quant]
math: true          # include only if the post uses LaTeX
excerpt: "One-line summary shown on the blog index."
---
```

Set `math: true` to load MathJax. Use `$...$` for inline math and `$$...$$` for display math.

## Structure

```
.
├── index.html          # Portfolio homepage
├── blog/
│   └── index.html      # Article index
├── _posts/             # Markdown articles
├── _layouts/
│   ├── default.html    # Base layout
│   └── post.html       # Article layout (includes MathJax if math: true)
├── assets/
│   └── css/main.css    # All styles
├── _config.yml
└── Gemfile
```
