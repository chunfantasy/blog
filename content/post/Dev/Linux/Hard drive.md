---
title: Hard Drive
description: Notes for operating hard drive on Linux
slug: linux-hard-drive
date: 2018-05-01
categories:
  - Development
tags:
  - Development
  - Linux
  - Debian
---

## Show disk

`lsblk -o name,mountpoint,label,size,uuid`

## Edit mount rules

`vim /etc/fstab`

## Mount

`mount -a`

## Checking folder size
```shell
# h for human readable
# s for summary
du -hs
```

## Checking folder size
```bash
df -h
```

## Copy with progress bar

`rsync -ah --info=progress2 [source] [destination]`

## Prevent sleep/hibernate/suspend

```bash
# Prevent sleep
sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target

# Undo preventing sleep
sudo systemctl unmas sleep.target suspend.target hibernate.target hybrid-sleep.target
```