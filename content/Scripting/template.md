---
title: "Templates"
titleIcon: "fa-solid fa-code"
categories: ["Scripting"]
weight: 2
---

## Introduction

ServX will look in the `templates` folder, recursively, for .template files. Templates can be organized in folders with names that fit your organization style. However, no two template files can share the same name, even if they are within seperate folders.

The format of the templates are lua tables and can be accessed from the global table `Template` but take care as to not unintentinally modify this global table, as any changes will only be represented in the global lua memory and will not affect creating a new item unless the template file is first modified and then reloaded.

Use `GetTemplateData(templateid)` to get a copy of the table if you wish to make modifications to it (for example, when making a custom item)

Many systems in `CORE` use Template Id (the name of the file.template without extension) to identify the item in question for various purposes. The Lua function [`Object.TemplateId(gameObj)`](https://github.com/corp-por/core/blob/main/scripts/globals/lib/object.lua#L35) is used to get this Id.

A Template Id is also a parameter when Creating a GameObj. Please see the [create library](https://github.com/corp-por/core/blob/main/scripts/globals/lib/create.lua).

The `/reloadtemplates` [command](scripting/commands) can be used by those with God access in-game to reload any template changes for testing.

## Template structure
Any value can be placed into a template, but there are specific values that ServX will look for when creating an item from this template, below are these specific values and their descriptions.

| Name | Description |
| :---: | :---: |
| TemplateName| Optional more user-friendly display name for the template in various internal locations. |
| ClientId | Dictates the visual model used for the object. See the [`ClienttIdReference.txt`](https://github.com/corp-por/core/blob/main/ClientIdReference.txt) file for a list of Ids. Also see [`ObjectTagDefinitions.xml`](https://github.com/corp-por/core/blob/main/ObjectTagDefinitions.xml) for information on properties associated with objects. |
| Name | The name that will be assigned to the object when created. |
| Attach | A single string (or table of strings) defining what lua script(s) will attach as modules when this item is created.
| SharedProperties | A Key(string)/Value(any) table of different SharedObjectProperties (these properties are sync'd between server/client for an object, this is how they are shared) The possible Key values are contained within [`ObjectTagDefinitions.xml`](https://github.com/corp-por/core/blob/main/ObjectTagDefinitions.xml) and are labled `SharedStateEntry` |
| ObjVars | A Key(string)/Value(any) table of Object Variables that will be set on this object when created. These are the same variables used in the CORE [`Var`](https://github.com/corp-por/core/blob/main/scripts/globals/lib/var.lua) library |
| Mobile | A table with two Keys `MovementSpeed` and `MobileType`, both are optional. If any table for Mobile is set within the template, and the object definitions allow it, this object will be created with the MobileComponent and will pass IsMobile checks, as well as gain the ability to path and move. |