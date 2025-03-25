---
title: "Fold Structure"
titleIcon: "fa-solid fa-folder"
categories: ["WorldCreator"]
date: 2023-07-13T14:12:32-06:00
draft: false
weight: 2
---

# Folder Structure

Each map in CODEX is a folder under /mapdata, inside this folder there will be a list of chunx, each file corosponding to its place in the world.

Under /mapseed a file that matches the name of the map will define the Seed spawns for the map. (Initial spawns and respawns after a resetworld).

For example, the map /mapdata/Test would have a /mapseed/Test.xml, this xml contains defitions to the intial seed spawns.