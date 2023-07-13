---
title: "Scripting"
titleIcon: "fa-solid fa-scroll"
categories: ["Scripting"]
weight: 1
---

ServX is powered by scripts. The [Templates](/scripting/template) use XML to define certain aspects of [GameObj](/lua/gameobj) that can be created/spawned. Each GameObj can have scripts or 'modules' attached to them. These attached scripts allow registering events to be handled on that GameObj. Also ServX loads the scripts/globals/main.lua file and all files [require](/lua/require)d within.