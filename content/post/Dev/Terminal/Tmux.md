---
title: Tmux
description: Notes for using Tmux
slug: tmux
date: 2018-05-01
categories:
  - Development
tags:
  - Development
  - Terminal
---
## Basic
- Create a new session

  Ctrl a + :new

- Create a new window

  Ctrl a + c

- Close a pane

  Ctrl d

- Switch to last active pane

  Ctrl a + ;

- Vertical split

  Ctrl a + %

- Horizontal split

  Ctrl a + "

- Rename session

  Ctrl a + $

- Rename window

  Ctrl a + ,

- Switch window index

  : swap-window -s 2 -t 1

- Save windows

  Ctrl a + s

- Restore windows

  Ctrl a + r

- Reload config

  :source-file ~/.tmux.conf

- Copy

  Ctrl a + [; y

  ## Plugin

  https://github.com/tmux-plugins/tpm

  - tmux-resurrect

  ## Settings

  1. oh-my-tmux

  https://github.com/gpakosz/.tmux

  1. .tmux.conf.local

  ```Bash
  # Install xclip
  tmux_conf_copy_to_os_clipboard=true
  ```
