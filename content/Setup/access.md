---
title: "AccessList.xml"
titleIcon: "fa-icons fa-solid fa-key"
categories: ["Setup"]
weight: 8
---

The AccessList file allows you to grant higher level access to users. Additionally, it allows you to grant access to users when you are running in 'AccessListOnly' mode. ServX will look for a AccessList.xml file in the current working directory. If one is not found, then a default will be created. Below are various options and their descriptions.

---

## AccessList
| Name | Description |
| :---: | :---: |
| UserId | This is the user's SteamID. See the [Steam FAQ](https://help.steampowered.com/en/faqs/view/2816-BE67-5B69-0FEC) on how to obtain this information from the user. The userId is also shown in the logs. |
| AccessLevel | Mortal, Immortal, Demigod, God |
| Name | *Optional* - Used as a reference and will show in the [logs](/setup/logs) on connect/disconnect. |
