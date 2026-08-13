---
title: "IEEE LaTeX Template"
date: 2024-10-28
draft: false
role: "author"
repo: "https://github.com/AT-UNDERMINER/LATEX_Template"
tags: ["tex"]
---

A LaTeX template set up for IEEE-style papers, so that starting a new report does not mean rebuilding the formatting
every time. It comes with the two-column IEEE layout, title, author and abstract blocks, and a predefined section
structure to write into.

Bibliography handling uses `IEEEtran.bst` with a `references.bib` file, and there are directories for figures and for
splitting sections into separate files if a paper gets long. I pulled the layout and code-listing settings out into their
own parameter files, along with a base package file, so page layout, code style and extra packages can be adjusted
without digging through `main.tex`. Example figures and a compiled PDF are included so the output is visible before
compiling anything.

It works on Overleaf by uploading the files and compiling with `pdflatex`, or locally with TeX Live or MiKTeX - locally
you also need Strawberry Perl. My own setup is VSCode with the LaTeX Workshop extension, which handles the multi-pass
pdflatex/bibtex/pdflatex/pdflatex cycle the bibliography needs in one keypress.

**Tech used:** LaTeX (pdflatex), BibTeX with IEEEtran.bst, TeX Live / MiKTeX, Strawberry Perl, Overleaf, VSCode + LaTeX Workshop

[View on GitHub](https://github.com/AT-UNDERMINER/LATEX_Template)
