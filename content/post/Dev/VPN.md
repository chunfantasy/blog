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

# OpenVPN

很方便

OpenVPN + WebSocket + Nginx（监听 443）

生成客户端

docker run -v $PWD/openvpn:/etc/openvpn --rm kylemanna/openvpn ovpn_genconfig -u tcp://域名  
docker run -v $PWD/openvpn:/etc/openvpn --rm -it kylemanna/openvpn ovpn_initpki  

# Wireguard

只支持UDP

访问国内非常不稳定

# ipsec 有点老

https://github.com/hwdsl2/docker-ipsec-vpn-server

Change `-v ikev2-vpn-data:/etc/ipsec.d \`

to `-v /path/to/ipsec.d:/etc/ipsec.d \`