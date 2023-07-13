---
title: "Fold Structure"
titleIcon: "fa-solid fa-folder"
categories: ["WorldCreator"]
date: 2023-07-13T14:12:32-06:00
draft: false
weight: 2
---

# Folder Structure

Each map in CODEX is a folder, inside this folder there needs to be at least one (or both) of the following two folders:

    /raw
    /bin

## raw

The World Creator can load a map folder if there's a raw folder container [.chunx](/worldcreator/chunk/#chunx) files. This is also where World Creator will save data to when a map save is done. Only the chunks that have edits will be saved.

## bin

This is the folder World Creator will export map data into. Exported map data is ready to be used for client/server.