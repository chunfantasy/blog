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


## OpenVPN

### Problems
```bash
Transport Error: socket_protect error (UDP)
Client terminate, restarting in 2000 ms...
```
### Solution 1 for one-time fix
```bash
sudo /Library/Frameworks/OpenVPNConnect.framework/Versions/Current/usr/sbin/ovpnagent
```
### Solution 2 for persistency fix after reboot
```bash
sudo launchctl load -w /Library/LaunchDaemons/org.openvpn.client.plist
```

