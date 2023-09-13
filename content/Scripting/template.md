---
title: "Templates"
titleIcon: "fa-solid fa-code"
categories: ["Scripting"]
weight: 2
---

## Introduction

ServX will look in the `templates` folder, recursively, for .xml files. Templates can be organized in folders with names that fit your organization. However, no two template files can share the same name, even if they are within seperate folders.

Many systems in `CORE` use Template Id (the name of the file.xml) to identify the item in question for various purposes. The Lua function [`Object.Template(gameObj)`](https://github.com/corp-por/core/blob/main/scripts/globals/lib/object.lua#L35) is used to get this Id.

A template is also a parameter when Creating a GameObj. Please see the [create library](https://github.com/corp-por/core/blob/main/scripts/globals/lib/create.lua).

The `/reloadtemplates` [command](scripting/commands) can be used by those with God access in-game to reload any template changes for testing.

## Template structure and examples
The `ClientId` dictates the model used for the object. See the [`ClienttIdReference.txt`](https://github.com/corp-por/core/blob/main/ClientIdReference.txt) file for a list of Ids. Also see [`ObjectTagDefinitions.xml`](https://github.com/corp-por/core/blob/main/ObjectTagDefinitions.xml) for information on properties associated with objects.

### System
#### Player
To set equipment, insert the name of the template but leave off the `equipment_` prefix.

From [`stones/templates/system/player.xml`](https://github.com/corp-por/stones/blob/main/templates/system/player.xml)

    <ObjectTemplate>
        <TemplateName>Male</TemplateName>
        <ClientId>1</ClientId>
        <ScaleModifier>1</ScaleModifier>
        <MobileComponent>
            <MobileType>Player</MobileType>
        </MobileComponent>
        <ObjectVariableComponent/>
        <ScriptEngineComponent>
            <LuaModule Name="player">
                <Initializer>
                    {
                        Equipment = {
                            Chest = "clothing_shirt",
                            Legs = "clothing_pants"
                        },
                        Stats = {
                            Health = 100,
                        }
                    }
                </Initializer>
            </LuaModule>
        </ScriptEngineComponent>	
    </ObjectTemplate>

### Items
Items have custom item properties configured separatly in Lua scripts that control damage, range, effects, etc. See the [properties documentation](scripting/properties#item-properties) for more information.

#### Armor
From [`stones/templates/items/armor/equipment_plate_legs.xml`](https://github.com/corp-por/stones/blob/main/templates/armor/equipment_plate_legs.xml)

    <ObjectTemplate>
    <Name>Plate Legs</Name>
        <ClientId>80</ClientId>
        <SharedStateEntry name="DenyPickup" type="bool" value="False"/>
        <ObjectVariableComponent>			
            <StringVariable Name="ArmorType">Heavy</StringVariable>
            <DoubleVariable Name="MaxDurability">30</DoubleVariable>
        </ObjectVariableComponent>
    </ObjectTemplate>

#### Scrolls
From [`stones/templates/items/scrolls/scroll_of_fireball.xml`](https://github.com/corp-por/stones/blob/main/templates/items/scrolls/scroll_of_fireball.xml)

    <ObjectTemplate>
    <Name>[00ff00]Scroll of Fireball[-]</Name>
        <ClientId>259</ClientId>
        <SharedStateEntry name="StackCount" type="double" value="20"/>
    </ObjectTemplate>

#### Weapons
From [`stones/templates/weapons/weapon_sledgehammer.xml`](https://github.com/corp-por/stones/blob/main/templates/weapons/weapon_sledgehammer.xml)

    <ObjectTemplate>
    <Name>Sledgehammer</Name>
        <ClientId>231</ClientId>
        <SharedStateEntry name="Variation" type="string" value="SM_Wep_Hammer_03"/>
        <SharedStateEntry name="CustomIcon" type="string" value="SM_Wep_Hammer_03"/>
    </ObjectTemplate>

### Mobiles
Mobiles have custom AI properties configured separatly in Lua scripts that control stats, abilities, loot, etc. See the [properties documentation](scripting/properties#ai-properties) for more information.

#### Animal
From [`stones/templates/mobiles/cow.xml`](https://github.com/corp-por/stones/blob/main/templates/mobiles/cow.xml)

    <ObjectTemplate>
        <ClientId>64</ClientId>
        <Name>Cow</Name>
        <ScaleModifier>1</ScaleModifier>
        <SharedStateEntry name="BodyOffset" type="double" value="2"/>
        <MobileComponent />
        <ScriptEngineComponent>
            <LuaModule Name="ai.brain_prey" />
        </ScriptEngineComponent>
    </ObjectTemplate>

#### Humanoid
From [`stones/templates/mobiles/bandit.xml`](https://github.com/corp-por/stones/blob/main/templates/mobiles/bandit.xml)

    <ObjectTemplate>
        <ClientId>1</ClientId>
        <Name>Scarlet Bandit</Name>
        <ScaleModifier>1</ScaleModifier>
        <SharedStateEntry name="BodyOffset" type="double" value=".33"/>
        <MobileComponent />
        <ScriptEngineComponent>
            <LuaModule Name="ai.brain_monster">
                <Initializer>
                    {
                    DNA = 
                        {
                            {"Head_Male_01","Head_Male_02","Head_Male_03","Head_Male_04","Head_Male_05"},

                            { "Hair_04", "Hair_05", "Hair_08", "Hair_14", "Hair_20", "Hair_21", "Hair_34", "Hair_1" },

                            "HeadCoverings_No_FacialHair_03",
                            {"Torso_Male_14", "Torso_Male_13"},
                            {"Hips_Male_10", "Hips_Male_13"},
                            "LegLeft_Male_02",
                            "LegRight_Male_02",
                            "ArmLowerRight_Male_00",
                            "ArmUpperRight_Male_00",
                            "ArmLowerLeft_Male_00",
                            "ArmUpperLeft_Male_00",
                            "HandRight_Male_04",
                            "HandLeft_Male_04",
                            "Color_Metal_Dark=F55A42",
                            "Color_Primary=F55A42",
                            "Color_Secondary=F55A42",
                            {"Color_Hair=A0522D", "Color_Hair=D2B48C", "Color_Hair=000000", "Color_Hair=C0C0C0", "Color_Hair=FFFFE0", "Color_Hair=F5DEB3", "Color_Hair=FAF0E6", "Color_Hair=FAFAD2", "Color_Hair=696969"}
                        },
                    Equipment = 
                        {
                            RightHand = {"weapon_dagger"},		
                        },
                    }
                </Initializer>
            </LuaModule>
        </ScriptEngineComponent>
    </ObjectTemplate>

## Additional resources
See Gizmo's Codex Basics videos for a step-by-step guide on creating a mobile and a weapon:
* [Codex Basics - Part 1 Creating a Mobile](https://www.youtube.com/watch?v=N-_6ERpLn60)
* [Codex Basics - Part 2 Creating a Weapon](https://www.youtube.com/watch?v=HvPb0-BkrsM)