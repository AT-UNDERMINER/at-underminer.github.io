# at-underminer.github.io

Source for my personal site at <https://at-underminer.github.io/> — project write-ups and build notes.
I'm an electrical engineering student and boilermaker, so most of what ends up here is embedded systems,
fabrication, or something sitting between the two.

## Stack

Hugo with the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. The theme is a git
submodule, not vendored, so theme updates stay separate from my content.

## Running it locally

```bash
git clone --recurse-submodules https://github.com/AT-UNDERMINER/at-underminer.github.io.git
cd at-underminer.github.io
hugo server -D
```

The `-D` matters — most pages sit as drafts until I'm happy with the writing, so without it the site
looks emptier than it is. If you cloned without `--recurse-submodules`, run
`git submodule update --init --recursive` or the build will fail with no theme.

## Content layout

| Path | What goes there |
| --- | --- |
| `content/projects/` | Repos I own and wrote — `role: "author"` |
| `content/contributions/` | Repos owned by others that I've worked on — `role: "contributor"` |
| `content/posts/` | Blog entries |
| `static/images/` | Images, referenced as `/images/name.jpg` |

Splitting projects from contributions keeps the distinction honest: the projects section is my own work,
and the contributions section is work where I was one of several hands.

## Front matter

```yaml
---
title: "Project Name"
date: 2026-03-14
draft: true
role: "author"        # or "contributor"
repo: "https://github.com/AT-UNDERMINER/project"
tags: ["python"]
---
```

- `role` distinguishes the two kinds of page and should match the section the file lives in.
- `repo` is the upstream repository. Omit it for anything not public, and say in the body that the
  repo isn't public rather than leaving a dead link.
- `date` is the repository's creation date for imported pages.
- `tags` are drawn from the repo's primary language and its GitHub topics.

## Conventions

- New pages start with `draft: true`. Nothing gets published without a read-through first.
- Plain first-person writing, no marketing language.
- Summaries are written fresh rather than pasted from a README.

## Deployment

A GitHub Actions workflow (`.github/workflows/hugo.yaml`) builds the site and deploys it to GitHub
Pages, so pushing to `main` is the whole release process.
