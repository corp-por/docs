---
title: "Commands"
titleIcon: "fa-icons fa-solid fa-hashtag"
categories: ["Scripting"]
weight: 999
---

This list may become out-of-date as commands are added or removed. Please check the code if commands are not behaving as they should.

---

## Commands
Most of these commands can be found under their respective access level folders under `<core/stones>\scripts\commands\<accesslevel>\main.lua`. For commands affecting an object, leaving off the object id from the command should produce either a targeting cursor or a UI window.

### Core commands
| Name | Description | [Access level](/setup/access) | Format (alias) |
| :---: | :---: | :---: | :---: |
| /help | Lists all available commands or describes a specific command. | Everyone | `/help <command>` |
| /allnames |  | Everyone | `/allnames <all/players/off>` |
| /logoff | Return to world select. | Everyone | `/logoff` |
| /quit | Quit to desktop. | Everyone | `/quit` |
| /bloom | Toggle bloom effect. | Everyone | `/bloom <on/off>` |
| /fpslock | Locks framerate to specified value. | Everyone | `/fpslock <5/10/15/30/60>` |
| /music | Sets the music volume. | Everyone | `/music <0-10>` |
| /sound | Sets the sound effects volume. | Everyone | `/sound <0-10>` |
| /say |  | Mortal | `/say <text>` |
| /where | Gives current coordinates. | Mortal | `/where` |
| /deletechar |  | Mortal | `/deletechar` |
| /bugreport | Currently disabled. | Mortal | `/bugreport` |
| /cast | Perform an ability | Mortal | `/cast` |
| /resurrect | Bring something back from the dead. | Immortal | `/resurrect` (`/res`) |
| /teleport | Jump. Jump. Jump around. | Immortal | `/teleport` (`/tele`) |
| /invulnerable | Toggle self invulnerability. | Immortal | `/invulnerable` (`/inv`) |
| /goto | Teleport to a specific location. | Immortal | `/goto` (`/go`) |
| /create | Allows for spawning of objects. | Demigod | `/create <template>` |
| /destroy | Allows for the removal of objects. | Demigod | `/destroy <target_id>` |
| /search |  | Demigod | `/search <name>` |
| /copy |  | Demigod | `/copy <target_id>` |
| /slay |  | Demigod | `/slay <target_id>` |
| /heal | Fully heals the target. | Demigod | `/heal <target_id>` |
| /summon | Summon your target. | Demigod | `/summon <target_id>` |
| /backup | Force a backup to take place. | God | `/backup` |
| /resetworld |  | God | `/resetworld` |
| /destroyall |  | God | `/destroyall` |
| /dostring |  | God | `/dostring <lua code>` (`/exec`) |
| /reload | [DEBUG COMMAND] Reload the behavior in memory. | God | `/reload` |
| /reloadtemplates | [DEBUG COMMAND] Reload all templates in memory. | God | `/reloadtemplates` |
| /info | Get information about an object. Gives cursor. | God | `/info` |
| /opencontainer | View the contents of a container. | God | `/opencontainer` |
| /shadow | Debug movement by seeing the server representation of a character. | God | `/shadow` |

### Stones commands
| Name | Description | [Access level](/setup/access) | Format (alias) |
| :---: | :---: | :---: | :---: |
| /getskill | Get the level of a skill | Mortal | `/getskill <skill>` |
| /setskill | Set the level of a skill. | God | `/setskill <skill> <level>` |