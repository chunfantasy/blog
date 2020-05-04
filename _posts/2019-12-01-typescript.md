---
layout: post
title: TypeScript Notes
description: "This note is about the JavaScript."
modified: 2019-12-01
tags: [Program Language]
comments: true
image:
  feature: 2019-12-01-typescript.jpeg
---

## Typescript notes

---

## Cannot find modoule issue

```bash
Cannot find module '*.jpg'.ts(2307)
Cannot find module '*.png'.ts(2307)
Cannot find module '*.svg'.ts(2307)
Cannot find module '*.json'.ts(2307)
```

Solution

Create `typings.d.ts` at `root`.

```javascript
declare module '*.jpg';
declare module '*.png';
declare module '*.json';
declare module '*.svg';
```
