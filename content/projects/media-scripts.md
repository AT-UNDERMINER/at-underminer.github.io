---
title: "Plex Media Scripts"
date: 2025-04-26
draft: false
role: "author"
repo: "https://github.com/AT-UNDERMINER/Media_Scripts"
tags: ["python"]
---

A set of Python scripts for keeping a movie library in the shape Plex expects. Plex scrapes metadata from file naming, so
a library that has drifted into inconsistent folder and file names stops matching properly - these scripts fix that
without me renaming things by hand.

The first script flattens single-file movie folders: it moves the `.mkv` up into the main library folder, renames it to
match the folder title, and removes the empty folder afterwards. Folders holding more than one `.mkv` are skipped rather
than guessed at, and every move, delete, skip and error is written to a log so I can check what happened. The second
script sorts `.mkv` files into `480p` through `2160p` subfolders by reading each file's height with `ffprobe`, which
makes later batch transcoding a per-folder job instead of a per-file decision.

The repo also holds two YouTube downloaders. One uses `pytubefix` to grab the best video and audio streams separately
and merge them with ffmpeg, naming files by title and putting playlists in their own folder. The other uses `yt-dlp`,
which is faster on large playlists but, since YouTube's mid-2025 backend changes, can fall back to HLS fragments and
produce files with no audio or broken seeking. I use the pytubefix one by default for that reason.

**Tech used:** Python 3.8+, ffmpeg / ffprobe, pytubefix, yt-dlp

[View on GitHub](https://github.com/AT-UNDERMINER/Media_Scripts)
