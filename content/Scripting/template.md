---
title: "Template"
titleIcon: "fa-solid fa-code"
categories: ["Scripting"]
weight: 2
---

# Template

ServX will look in the `templates` folder, recursively, for .xml files. An example template looks like this:

    <ObjectTemplate>
        <Name>[00ff00]Scroll of Fireball[-]</Name>
        <ClientId>259</ClientId>
        <SharedStateEntry name="StackCount" type="double" value="20"/>
    </ObjectTemplate>

Templates can be organized in folders with names that fit your organization. However no two template files can share the same name, even if they are within seperate folders.

Many systems in `CORE` use Template Id (the name of the file.xml) to identify the item in question for various purposes. The Lua function [`Object.Template(gameObj)`](https://github.com/corp-por/core/blob/main/scripts/globals/lib/object.lua#L35) is used to get this Id.

A template is also a parameter when Creating a GameObj. Please see the create library by [clicking here](https://github.com/corp-por/core/blob/main/scripts/globals/lib/create.lua).