---
title: "Run"
titleIcon: "fa-solid fa-terminal"
categories: ["Setup"]
date: 2023-07-03T14:12:32-06:00
draft: false
weight: 5
---

# Run

Open a new Command Prompt or Powershell and navigate to your *rundir*, from there run the command:

    ..\servx\ServX.exe

---

## Config.xml changes ##

If this is the first time ServX has been run or you want a clean Config.xml file, immediately terminate the program (Ctrl+C) after a Config.xml has been created, change the [Config.xml](/setup/config) as necessary, and run ServX again.

## Specific Instance by Id

If there is more than one Instance defined in Config.xml a specific instance can be started by passing the Id:

    ..\servx\ServX.exe MyCluster.Stones

## Confirm Running

When ServX is ready for connections the console will output:

    Accepting Users

## Errors

If errors are encountered when trying to run ServX for the first time, ensure that all installation steps have been completed, including the installation of the .NET [prerequisites](/setup/install/#prerequisites), the [lua](/setup/lua) scripts. For other errors, see the [errors](/setup/errors) documentation.