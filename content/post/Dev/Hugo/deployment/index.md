---
title: Hugo Deployment
description: How to deploy my blog to GitHub page?
slug: hugo-deployment
date: 2025-06-14
image: cover.png
categories:
  - Blog
tags:
  - Hugo
  - GitHub
  - Actions
  - Deployment
  - CI/CD
  - DevOps
---

## Deployment

### Problems and Solutions

- After having committed my blog to main branch, it does not deploy automatically.
Having tried with my own GitHub Actions workflow but does not help.

	Eventually a doc from Hugo saved me.
	[Host on GitHub Pages](https://gohugo.io/host-and-deploy/host-on-github-pages/)

- Not able to show pictures in title

	Need to use **index** as tilte and file name instead of the full meaningful title.


## Commitment

### Problems and Solutions

- Notes for Obsidian usage is located in one location while notes for Hugo is under blog's repo.

	So far, the simplest way to resolve this issue is to copy all notes to blog before committing.
	```bash
	cd /Users/chfa/dev/blog/content/post/
	rm -rf **
	cp -R /Users/chfa/NextcloudNotes/ChunNotes/10-Blog/* /Users/chfa/dev/blog/content/post/
	```

