---
title: "Flask Wikipedia Demo"
date: 2025-08-04
draft: true
role: "author"
repo: "https://github.com/AT-UNDERMINER/flaskdemo"
tags: ["python"]
---

A demo Flask site built for CP1404 Practical 10 at JCU. It takes a search term, queries the Wikipedia API, and renders
the result back as a web page.

Unlike the earlier single-file Flask exercise, this one uses a proper template layout. There is a base `layout.html`
that the home, about, search and results pages all extend, plus a small stylesheet in `static/`. That split is really the
lesson of the practical: the Python side handles the request and the API call, and the templates handle presentation,
so neither one has to know much about the other.

Working with the Wikipedia API also meant dealing with responses I did not control - missing pages, unexpected shapes -
which is a different problem from the self-contained exercises earlier in the subject.

**Tech used:** Python, Flask, Jinja2 templates, Wikipedia API, CSS

[View on GitHub](https://github.com/AT-UNDERMINER/flaskdemo)
