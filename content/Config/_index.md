---
title: "Config.xml"
titleIcon: "fa-icons fa-solid fa-wrench"
categories: ["Config"]
weight: 999
---

### Default Config.xml

ServX will look for a Config.xml file in the current working directory. If one is not found then a default will be created. Below are various options and their descriptions.

---

# Config

| Name | Description |
| :---: | :---: |
| ExposeToInternet | If false, ServX will only listen on the local loopback (127.0.0.1). If true, ServX will listen on all interfaces. |
| AdvertiseServer | If true, ServX will be visible in the public server list. |
| AccessListOnly | If true, only those defined within AccessList.xml will be allowed a successful connection, anyone else will be denied. |
| AccessRestriction | When defined, only those with access greater than or equal to definition can successfully connect. |
| ServerIndex | This setting is useful to run multiple stand-alone instances of ServX, each instance can have a unique index to prevent collisions with ports. This setting directly affects [Ports](/setup/ports). Does not affect cluster instances. |
| ServerName | Name of the server, displayed in the server browser. |
| ServerDescription | A description of the server. |
| DEV | When true, a global lua variable *DEV* is declared as true. This allows writing logic to handle things from development to production by using different Config.xml files, as configurations are not shared between those environments. |
| StartingTemplate | The template a new player will use when created. |
| Core | Relative to *rundir* location of the core scripts and definitions |
| Game | Relative to *rundir* location of the game scripts and definitions. This can overwrite anything defined in Core. |
| Mod | Relative to *rundir* location of the mod scripts and definitions. This can overwrite anything defined in Core and/or Game. |
| Instance | The details of the ServX instance(s). |

###### Instance

    <Instance ServerIndex="0" Id="MyCluster.Stones" WorldName="Stones" MapUrl="http://127.0.0.1:3000" MaxUsers="32" Required="false" />
    <Instance ServerIndex="1" Id="MyCluster.Boulder" WorldName="Boulder" MapUrl="http://127.0.0.1:3001" MaxUsers="32" Required="false" />

| Name | Description |
| :---: | :---: |
| ServerIndex | When ServX runs as an instance to a cluster, this defines the ServerIndex to use for that instance. This setting directly affects [Ports](/setup/ports). |
| Id | Unique identifier for an Instance. This used to be called Region Address in Shards Engine and fragments will remain till they don't. |
| WorldName | The name of the world This must match the folder in mapdata of the map you wish to run. Requires exported mapdata from World Creator. |
| MapUrl | The remote http location of the map chunks exported from World Creator. |
| MaxUsers | The maximum number of users that can connect before ServX refuses further connections. |
| Required | ClusterX won't accept users until all ServX instances with *Required* set *True* are accepting users.

---

# Cluster
These settings are only applicable when running as a cluster.

| Name | Description |
| :---: | :---: |
| ClusterAddress | If this is defined ServX will wait until a connection to a ClusterX instance (at this address) is established before continuing. Comment out or remove from Config.xml to run ServX in standalone. |
| InstanceAddress | The public url/ip address ClusterX will connect players to when sending to this instance. |
| StartingInstanceId | The instance by Id that new players are sent to. |
