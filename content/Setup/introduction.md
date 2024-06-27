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

ServX will create a [Config.xml](/config) in your *current working directory* when [executed](/setup/run) but only if a Config.xml does not already exist.

## Folder Structure

Create a new folder somewhere to house all the new folders we will be creating, something like *C:/CODEX*.

Within this folder create another new folder called *rundir* (or whatever you prefer, name doesn't matter. This will be our *current working directory*)

The default config will look for a folder named *core* and a folder named *stones* up one directy from the *current working directory*:

    <Core>../core</Core>
	<Axiom>../stones</Axoim>

After installing both the [Lua Scripts](/setup/lua) and [ServX](/setup/install), The final folder structure within *C:/CODEX* would look like this:

    core
    rundir
    servx
    stones

With *rundir* to contain the configuration files and act as our *current working directory*.