---
title: "Ports"
titleIcon: "fa-solid fa-network-wired"
categories: ["Setup"]
date: 2023-07-06T14:12:32-06:00
draft: false
weight: 1000
---
## ServX
ServerIndex is set in [Config.xml](/config).

| Port | Protocol | Description |
| --- | --- | --- |
| 3000 + ServerIndex | TCP | ServX will host the active map on a http connection, this is useful for testing and small servers. Anything larger than a few dozen players should block this port and instead host the map files on a static webhost. |
| 3000 + ServerIndex | UDP | This is the main gameplay connection the client will use to connect to the server. |
| 27016 + ServerIndex | TCP/UDP | This is the [Steam Query Port](https://help.steampowered.com/en/faqs/view/2EA8-4D75-DA21-31EB). |


## ClusterX

| Port | Protocol | Description |
| --- | --- | --- |
| 5000 | UDP | This is the main gameplay connection the client will use to connect to the server. |
| 5001 | UDP | This is the port each ServX instance will connect to. It is imperative that security be handled at the firewall and **only allow known IPs** of each machine running an instance of Servx. |
| 27015 | TCP/UDP | This is the [Steam Query Port](https://help.steampowered.com/en/faqs/view/2EA8-4D75-DA21-31EB). |