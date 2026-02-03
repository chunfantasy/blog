---
title: GitHub Actions
description: Notes for code GitHub Actions
slug: github-actions
date: 2025-09-10
categories:
  - Development
tags:
  - Development
  - CI/CD
---

# Remove Existing Runners

#### Issue
```shell
# Runner removal

Failed: Removing runner from the server
Value cannot be null. (Parameter 'configuredSettings')
```

#### Solution
```shell
rm .runner // if exists
rm .runner-migrated // if exists
./config.sh remove
```


