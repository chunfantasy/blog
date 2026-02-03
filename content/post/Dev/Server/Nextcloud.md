---
title: Nextcloud
description: Notes for using Nextcloud for file sharing
slug: nextcloud
date: 2024-01-01
categories:
  - Development
tags:
  - Development
  - HomeServer
---

## Background jobs

```Bash
sudo su
crontab -e
*/5 * * * * docker exec -u 1000 nextcloud php /var/www/html/cron.php
```
