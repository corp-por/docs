---
title: "Properties"
titleIcon: "fa-solid fa-gear"
categories: ["Scripting"]
weight: 3
---

# Properties

## AI properties
Mobile AI properties can be managed with Lua in [`stones/scripts/globals/static_data/ai_properties`](https://github.com/corp-por/stones/tree/main/scripts/globals/static_data/ai_properties)

### Example
From [`stones/scripts/globals/static_data/ai_properties/undead.lua`](https://github.com/corp-por/stones/blob/main/scripts/globals/static_data/ai_properties/undead.lua). This code dictates the properties of the [lich template](https://github.com/corp-por/stones/blob/main/templates/mobiles/lich.xml).

    AIProperties.lich = {
        Level = 80,
        TeamType = "Undead",
        Weapon = {
            Speed = 0.4,
            Damage = {24,26},
            Range = 1.25,
            DamageType = "Bashing"
        },
        Stats = {
            Health = 120,
        },
        Abilities = {
            "Fireball",
            "Energybolt"
        },
        Loot = {
            {"gold", {50,70}},
            "scroll_of_energybolt"
        },
        BaseMoveSpeed = 4.0,
    }

## Item properties
Item properties can be managed with Lua in [`stones/scripts/globals/static_data/item_properties`](https://github.com/corp-por/stones/tree/main/scripts/globals/static_data/item_properties).

### Example
From [`stones/scripts/globals/static_data/item_properties/weapons.lua`](https://github.com/corp-por/stones/blob/main/scripts/globals/static_data/item_properties/weapons.lua) This code dictates the properties of the [spear template](https://github.com/corp-por/stones/blob/main/templates/weapons/weapon_spear.xml).

    ItemProperties.weapon_spear = {
        Speed = 0.6,
        Damage = {20,30},
        Range = 2.0,
        DamageType = "Piercing",
        TwoHanded = true,
        ImpactSound = "spear"
    }