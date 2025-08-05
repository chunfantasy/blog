---
title: General Usage for Linux
description: Notes for general usage for Linux, particularly for Debian
slug: linux
date: 2011-08-01
categories:
  - Development
tags:
  - Development
  - Linux
  - Debian
---


## Add user to sudo group

```Bash
su -
usermod -aG sudo chun
exit
```
## Beep Sound

解决方法，添加启动程序，命令 xset b off

## Source List

[https://wiki.debian.org/SourcesList#Repository_URL](https://wiki.debian.org/SourcesList#Repository_URL)

## Tools

- ### Remmina
	远程桌面
	
- ### xfce-terminal:
  - xfce-terminal —fullscreen: 全屏启动
  - xfce-terminal —maximaize: 最大化启动

- ### Exa
	ls 替代品
	
- ### imagemagick
	图片 PDF 处理
	
- ### poppler-utils
	pdf 处理
	  - 安装 sudo apt-get install poppler-utils
	  - pdf 转图片 pdftoppm -png ejemplo.pdf imagen
	  - pdf 合并 pdfunite file1.pdf file2.pdf merged_output.pdf

- ### Okular
	pdf 编辑器

- ### 微信 
	[https://github.com/loaden/nspawn-qq](https://github.com/loaden/nspawn-qq)

- ### htop

  htop 是一个交互式系统监视、进程查看和进程管理器
 

