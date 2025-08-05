---
title: Apollo GraphQL
description: Notes for GraphQL
slug: apollo-graphql
date: 2018-05-01
categories:
  - Development
tags:
  - Development
---

## Problems

```Bash
Missing field 'verifier' while writing result
```

**Solution:**

```Bash
fetchPolicy: 'no-cache'
```