---
title: "CP1404 Flask Project"
date: 2025-08-04
draft: true
role: "author"
repo: "https://github.com/AT-UNDERMINER/cp1404_FlaskProject"
tags: ["python"]
---

A small Flask application I wrote as a CP1404 practical solution. The whole thing is a single `app.py`, which suited the
exercise - the point was to see how routing works, not to build out a project structure.

It serves four routes. `/` returns a hello-world heading, `/greet` and `/greet/<name>` show how a route can take an
optional path parameter, and `/c2f/<temp>` converts a Celsius value in the URL to Fahrenheit. The practical only asked
for the Celsius conversion, but leaving it one-directional bothered me, so I added `/f2c/<temp>` and a matching
`convert_f_to_c` function to round out the behaviour.

The conversions themselves live in plain functions separate from the route handlers, which keeps the maths testable and
independent of Flask. There is no README on this repo - the code is short enough to read directly.

**Tech used:** Python, Flask

[View on GitHub](https://github.com/AT-UNDERMINER/cp1404_FlaskProject)
