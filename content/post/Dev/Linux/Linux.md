---
title: Webpack
description: Notes for code Webpack
slug: webpack
date: 2018-05-01
categories:
  - Development Category
tags:
  - Development
---

## 工具

- Remmina：远程桌面
- xfce-terminal:
    - xfce-terminal —fullscreen: 全屏启动
    - xfce-terminal —maximaize: 最大化启动
- Exa ls替代品
- imagemagick 图片PDF处理
- poppler-utils: pdf处理
    - 安装sudo apt-get install poppler-utils
    - pdf转图片 pdftoppm -png ejemplo.pdf imagen
    - pdf合并 pdfunite file1.pdf file2.pdf merged_output.pdf
- Okular pdf编辑器
- 微信 [https://github.com/loaden/nspawn-qq](https://github.com/loaden/nspawn-qq)

[[Hard drive]]

- Prevent sleep/hibernate/suspend
    - sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
    - Undo
    - sudo systemctl unmas sleep.target suspend.target hibernate.target hybrid-sleep.target

## Issues

- Beep声音
    - 解决方法，添加启动程序，命令xset b off

  

[[Wine - 不好用]]

  

[[sudo]]

[[source list]]

[[虚拟机复制粘贴]]