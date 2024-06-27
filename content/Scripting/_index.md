---
title: "Scripting"
titleIcon: "fa-solid fa-scroll"
categories: ["Scripting"]
weight: 3
---

ServX is powered by scripts. The [Templates](/scripting/template) use XML to define certain aspects of [GameObj](/lua/gameobj) that can be created/spawned. Each GameObj can have scripts or 'modules' attached to them. These attached scripts allow registering events to be handled on that GameObj. Also ServX loads the scripts/globals/main.lua file and all files [require](/lua/require)d within.

## API

The [API](https://servx.corppor.com) consists of the function defined by ServX that can be utilized within the Lua scripts. Generally (but not guaranteed) a function call with a `:` semicolon will be used to call ServX defined API functions. When a `.` period is used to call a function this is more than likely a globally defined Lua function.

## Script layers

There are three layers of scripts possible in CODEX and the paths for each are defined in [Config.xml](/setup/config). `Core` is the base level scripts for the system. `Axiom` is the next level of scripts and will define the gameplay. `Mod` is the final level of scripts and can be used to customize features of the Axiom. Higher level files will override those with the same path and name in lower levels.

| Layer | Content | Default path
| :---: | :---: | :---: |
| Top layer - `Mod` | Feature customizations | `<Mod>../testcenter</Mod>` </p>(commented out by default)
| Middle layer - `Axiom` | Examples; Stones (skill based), Vanilla (class based, to be released) | `<Axiom>../stones</Axiom>`
| Base layer - `Core` | Core | `<Core>../core</Core>`
