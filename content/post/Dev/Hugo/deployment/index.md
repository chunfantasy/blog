---
title: Hugo Deployment
description: How to deploy my blog to GitHub page?
slug: hugo-deploymen
date: 2025-06-14
image: cover.png
categories:
  - Blog
tags:
  - Hugo
  - GitHub
  - GitHub
  - Actions
  - Deployment
  - CI/CD
  - DevOps
---


## Deployment
### Problems

After having committed my blog to main branch, it does not deploy automatically.
Having tried with my own GitHub Actions workflow but does not help.

### Solution

Eventually a doc from Hugo saved me.
[Host on GitHub Pages](https://gohugo.io/host-and-deploy/host-on-github-pages/)


## Commitment

### Problems

Notes for Obsidian usage is located in one location while notes for Hugo is under blog's repo.

### Solution

So far, the simplest way to resolve this issue is to copy all notes to blog before committing.
```bash
cp -R /Users/chfa/Notes/ChunNotes/10-Blog/* /Users/chfa/dev/blog/content/post/
```

