# iakov.dev

Personal blog of Iakov Sumygin, served by GitHub Pages at https://iakov.dev.

Plain Jekyll, no theme: posts in `_posts/`, images in `assets/img/<year>/`, one stylesheet in `assets/css/site.css`.

## Run locally

```bash
bundle install
bundle exec jekyll serve --livereload
```

Then open http://localhost:4000.

## New post

Create `_posts/YYYY-MM-DD-slug.md`:

```markdown
---
title: Post title
description: One sentence for the post list and search engines.
tags: [engine]
youtube: VIDEO_ID   # optional, shown at the top
---

Text. Images go in assets/img/YYYY/ and are linked as ![alt](/assets/img/YYYY/file.jpg).
Inline videos: {% raw %}{% include youtube.html id="VIDEO_ID" %}{% endraw %}
```

Older posts (2009-2021) came from glow3d.com/blog.
