---
title: Database
description: This is a note for Database
slug: database
date: 2020-01-01
categories:
  - Development
tags:
  - Database
---

# DBeaver

Dbeaver is a database administrator. Use the following script to start it up via docker.

```Bash
sudo docker run \
  --name cloudbeaver \
  -ti -d \
  --restart unless-stopped \
  -p 8088:8978 \
  -v /home/chun/dev/cloudbeaver/workspace:/opt/cloudbeaver/workspace \
  dbeaver/cloudbeaver:latest
```
