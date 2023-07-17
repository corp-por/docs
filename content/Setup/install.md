---
title: "Install"
titleIcon: "fa-brands fa-steam"
categories: ["Setup"]
date: 2023-07-03T14:12:32-06:00
draft: false
weight: 2
---

## SteamCMD

---

[SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD) is required to continue.

---

ServX can be installed and kept up-to-date using the following SteamCMD script:

    force_install_dir ./servx
    login your_steam_username
    app_update 2241750 validate
    quit

Note: SteamCMD recommends having a separate account to run dedicated servers but the account used to login must have CODEX in its game library.

If you prefer, you can save this snippet to a file such as *update_servx.txt* then run:

    steamcmd.exe +runscript D:\my_server\update_servx.txt

## Prerequisites

---

ServX relies on the [.Net 6.0 Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)

![.Net 6.0 Runtime](/images/net-runtime.png)