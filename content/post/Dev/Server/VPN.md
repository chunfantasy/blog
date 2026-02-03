---
title: VPN
description: Notes for using different VPNs
slug: VPN
date: 2025-08-01
categories:
  - Development
tags:
  - Development
  - HomeServer
---

## V2Ray

穿墙王

V2Ray with WebSocket on 443

```bash
{
  "inbounds": [{
    "port": 443,
    "protocol": "vless",
    "settings": {
      "clients": [{
        "id": "xxx",
        "level": 0,
        "email": "email@chun.no"
      }],
      "decryption": "none"
    },
    "streamSettings": {
      "network": "ws",
      "security": "tls",
      "tlsSettings": {
        "certificates": [{
          "certificateFile": "/usr/local/etc/v2ray/cert/fullchain.pem",
          "keyFile": "/usr/local/etc/v2ray/cert/privkey.pem"
        }]
      },
      "wsSettings": {
        "path": "/ws"
      }
    }
  }],
  "outbounds": [{
    "protocol": "freedom"
  }]
}
```

### Problems

#### Failed to start the service
```bash
Oct 28 22:29:29 debian systemd[1]: Started v2ray.service - V2Ray Service.
Oct 28 22:29:29 debian v2ray[861979]: V2Ray 5.31.0 (V2Fly, a community-driven edition of V2Ray.) Custom (go1.24.2 linux/amd64)
Oct 28 22:29:29 debian v2ray[861979]: A unified platform for anti-censorship.
Oct 28 22:29:29 debian v2ray[861979]: Failed to start: main/commands: failed to load config: [/usr/local/etc/v2ray/config.json] > infra/conf/v4: Failed to build TLS config. > infra/co
nf/cfgcommon/tlscfg: failed to parse certificate > open /home/chun/v2ray/cert/fullchain.pem: permission denied
Oct 28 22:29:29 debian systemd[1]: v2ray.service: Main process exited, code=exited, status=1/FAILURE
Oct 28 22:29:29 debian systemd[1]: v2ray.service: Failed with result 'exit-code'.
```
#### Solution
1. Copy certificates to /usr/local/etc/v2ray/cert
2. Change owner to root
3. Change mod to 644

## OpenVPN

很方便

OpenVPN + WebSocket？ + Nginx？（监听 443）

生成客户端

docker run -v $PWD/openvpn:/etc/openvpn --rm kylemanna/openvpn ovpn_genconfig -u tcp://域名
docker run -v $PWD/openvpn:/etc/openvpn --rm -it kylemanna/openvpn ovpn_initpki

### Problems

#### Transport error
```bash
Transport Error: socket_protect error (UDP)
Client terminate, restarting in 2000 ms...
```
#### Solution 1 for one-time fix
```bash
sudo /Library/Frameworks/OpenVPNConnect.framework/Versions/Current/usr/sbin/ovpnagent
```
#### Solution 2 for persistency fix after reboot
```bash
sudo launchctl load -w /Library/LaunchDaemons/org.openvpn.client.plist
```

# Wireguard (Not recommended)

It's

只支持 UDP

访问国内非常不稳定

# ipsec  (Not recommended)

太老了It's too old

https://github.com/hwdsl2/docker-ipsec-vpn-server

Change `-v ikev2-vpn-data:/etc/ipsec.d \`

to `-v /path/to/ipsec.d:/etc/ipsec.d \`

