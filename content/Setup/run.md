---
title: "Run"
titleIcon: "fa-solid fa-terminal"
categories: ["Setup"]
date: 2023-07-03T14:12:32-06:00
draft: false
weight: 3
---

# Prerequisites

ServX relies on the [.Net 6.0 Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)

![.Net 6.0 Runtime](/images/net-runtime.png)

# Run

Open a new Command Prompt or Powershell and navigate to your *rundir*, from there run the command:

    ..\servx\ServX.exe

---

### Specific Instance by Id

If there is more than one Instance defined in [Config.xml](/config) a specific instance can be started by passing the Id:

    ..\servx\ServX.exe MyCluster.Stones


# Confirm Running

When ServX is ready to be connected to you will see:

    Accepting Users

If this is your first run or you want a clean Config.xml file, immediately terminate the program (Ctrl+C) after a Config.xml has been created, change the Config.xml as necessary, and run ServX again.