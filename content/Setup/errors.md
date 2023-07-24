---
title: "Errors"
titleIcon: "fa-regular fa-bug"
categories: ["Setup"]
date: 2023-07-12T14:12:32-06:00
draft: false
weight: 99
---

## Stones.ConnectLog

    Steam Authentication Failure (Timeout waiting for response from Steam)

A restart of the Steam desktop application should solve this.

---

## Stones.Gameplay

    gameplay Error: 0 : [GameplaySimulation] Fatal exception occured. Broadcasting Panic Message.
    gameplay Error: 0 : CoreUtil.ShardsException: Missing map export bin folder in mapdata: Expected at: ../core\mapdata\Stones\bin. Please Load and Export the map in World Creator.
        at Gameplay.GameplayModule.BeginSimulation(Boolean _forceNew)
        at Gameplay.GameplayModule.ThreadProc()

Ensure the Stones map has been loaded and exported. See the [map](setup/map) setup documentation for more information.