# salman-khalid.com

Personal academic website built with Eleventy and hosted on Cloudflare Pages. Every change pushed to the `main` branch on GitHub goes live in about a minute.

## Add a blog post
Create a file in `src/blog/posts/` named like `2026-11-15-my-post-title.md`:

```
---
title: My post title
date: 2026-11-15
summary: One sentence that appears in the list and in link previews.
tags: [policy]
math: false        # set true to use $...$ and $$...$$ equations
---

Write the post here in Markdown.
```

## Add a lecture or lab
1. Put the file in `src/files/<course>/`, for example `src/files/eco345/lecture-03.pdf`.
2. Open the course file in `src/teaching/courses/` and add a line under `lectures:` or `labs:`

```
lectures:
  - title: Simple regression
    desc: Chapter 2, Wooldridge
    files:
      - { label: "SLIDES", url: /files/eco345/lecture-03.pdf }
      - /files/eco345/lecture-03.R   # plain paths show the file type as the label
```

Keep each file under 25 MB (Cloudflare limit).

## Edit research, media or profile
* Papers live in `src/_data/research.json`
* Op-eds and interviews live in `src/_data/media.json`
* Name, links, email and the job market badge live in `src/_data/site.json`
* The bio is at the top of `src/index.njk`
* Replace `src/assets/img/headshot.jpg` to change the photo, and `src/files/Khalid_CV.pdf` to update the CV

## Run locally (optional)
`npm install` then `npm start`, and open http://localhost:8080

Cloudflare Pages settings: build command `npx @11ty/eleventy`, output directory `_site`.
