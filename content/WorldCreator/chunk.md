---
title: "Chunk"
titleIcon: "fa-solid fa-diamond"
categories: ["WorldCreator"]
date: 2023-07-13T14:12:32-06:00
draft: false
weight: 3
---

# Chunks

Every map in CODEX is made with the World Creator and is comprised of many individual chunks. A Chunk can easily be visualized in the World Creator in the CODEX client with each chunk containing all the information to load that chunk (terrain, water, objects, collision, etc). This has the advantage of the player streaming in the map chunks around them as necessary. For this we use an http server to host the exported chunks. Another advantage is when working on a map with others, as long as different chunks are edited, there should be no collisions when trying to commit your work.

## .chunkx

This is the format each individual chunk file is saved in.