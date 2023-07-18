---
title: "Scripting"
titleIcon: "fa-solid fa-scroll"
categories: ["Scripting"]
weight: 3
---

ServX is powered by scripts. The [Templates](/scripting/template) use XML to define certain aspects of [GameObj](/lua/gameobj) that can be created/spawned. Each GameObj can have scripts or 'modules' attached to them. These attached scripts allow registering events to be handled on that GameObj. Also ServX loads the scripts/globals/main.lua file and all files [require](/lua/require)d within.

# API

The [API](https://servx.corppor.com) consists of the function defined by ServX that can be utilized within the Lua scripts. Generally (but not guaranteed) a function call with a `:` semicolon will be used to call ServX defined API functions. When a `.` period is used to call a function this is more than likely a globally defined Lua function.