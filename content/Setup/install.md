---
title: "Install"
titleIcon: "fa-brands fa-steam"
categories: ["Setup"]
date: 2023-07-03T14:12:32-06:00
draft: false
weight: 2
---

# SteamCMD

---

[SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD) is required to continue.

---

ServX can be installed and kept up-to-date using the following SteamCMD script:

    force_install_dir ./servx
    login your_steam_username
    app_update 2241750 validate
    quit

If you prefer, you can save this snippet to a file such as *update_servx.txt* then run:

    steamcmd.exe +runscript D:\my_server\update_servx.txt