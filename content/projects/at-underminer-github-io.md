---
title: "Personal Site"
date: 2026-08-13
draft: true
role: "author"
repo: "https://github.com/AT-UNDERMINER/at-underminer.github.io"
tags: []
---

This is the repository for the site you are reading. It is a Hugo static site using the PaperMod theme, pulled in as a git
submodule rather than vendored, so theme updates stay separate from my own content.

Content is split into `content/projects/` for build and project write-ups and `content/posts/` for blog entries, with
both listed as main sections on the home page. Images live in `static/images/` and are referenced by absolute path.
Everything about the site's structure is configured in a single `hugo.toml` - base URL, menu, and the home page
introduction - which keeps the setup easy to reason about later.

Publishing is handled by a GitHub Actions workflow that builds the site and deploys it to GitHub Pages, so pushing to
`main` is the whole release process. New pages start as drafts, and I promote them once I am happy with the writing.

**Tech used:** Hugo, PaperMod theme, GitHub Actions, GitHub Pages, Markdown

[View on GitHub](https://github.com/AT-UNDERMINER/at-underminer.github.io)
