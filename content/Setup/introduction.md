---
title: "Introduction"
titleIcon: "fa-solid fa-icons fa-folder"
categories: ["Setup"]
date: 2023-07-03T14:12:32-06:00
draft: false
weight: 1
---

This information is written from the assumption the reader has a basic understanding of a computer command prompt.

---

Currently, ServX is only supported on Windows. Linux will be supported but for now only Windows.

## Config

ServX will look for a [Config.xml](/config) file in the current working directory, if one is not found then a default will be created. This is the same for the AccessList.xml

## Folder Structure

The default [Config.xml](/config) will look for a folder named *core* and a folder named *stones* up one directy from the working directory:

    <Core>../core</Core>
	<Game>../stones</Game>

Next to these folders is a good place to install ServX, allowing one directory to hold all of the instance's data.

The final folder structure could then look something like this:

    core
    rundir
    servx
    stones

With *rundir* containing the configuration files.