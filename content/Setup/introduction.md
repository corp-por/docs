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

# Config.xml

ServX will create a [Config.xml](/config) for you when [run](/setup/run) but only if a config does not already exist. Right now we'll create a folder structure to work with this default when it's created.

## Folder Structure

The default config will look for a folder named *core* and a folder named *stones* up one directy from the *current working directory*:

    <Core>../core</Core>
	<Game>../stones</Game>

Next to these folders is a good place to install ServX, allowing one directory to hold all of the instance's data.

The final folder structure could then look something like this:

    core
    rundir
    servx
    stones

With *rundir* containing the configuration files and acting as our *current working directory*.