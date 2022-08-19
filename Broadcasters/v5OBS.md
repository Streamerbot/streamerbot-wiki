---
title: OBS Studio
description: Configuration page for one or more connection(s) to OBS Studio instance(s)
published: true
date: 2022-08-19T16:26:40.705Z
tags: 
editor: markdown
dateCreated: 2022-08-19T16:26:40.705Z
---

![obs.svg](/logos/obs.svg){.align-abstopright}

> OBS Websocket *v4.9+*{.obs-version-badge} and *v5+*{.obs-version-badge} are both supported.
{.is-info}

- [<img src="/logos/obs-websocket.png"/>**Download OBS WebSocket *<i class="mdi mdi-github"></i> obs-websocket v5+***](https://github.com/obsproject/obs-websocket/releases/latest)
{.btn-grid .my-5}

## Overview

Adding at least one connection will allow you to control your OBS either through the various [sub-actions](/Sub-Actions#main) that have been included, or via the [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code) sub-action

![broadcasters-obs-018.png](/broadcasters-obs-018.png)

> If you are using *v0.1.7*{.version-badge} or below the OBS configuration is found as a top level tab but the functionality is the same
{.is-info}


Once configured, connected OBS sessions will report their status on this screen

## Setup
`Right-Click` -> `Add` to define a new connection
Give it a name and set the IP address and Port number of the OBS Websocket

The Default values of `127.0.0.1` and `4444` will look for the out-of-box configuration for OBS installed on the same computer as CPH is running

`Password` Will not be required unless you have specified one in OBS

![New Connection](/119574587-9adb7e80-bdad-11eb-82c1-ec9ed668a40d.png)


Connections can be configured to `Auto Connect on Startup`, and to `Reconnect on Disconnect` with a retry interval you specify in seconds

***

### OBS Information

Shows the version number of OBS and the installed Websocket plugin

### Current Scene

Shows the name of the currently broadcasting scene on that connection

### Stream Status

Shows the status of current streaming and recording activity

### Sources

Lists all sources present on the currently selected scene

## Events

You can assign actions to events that OBS transmits across the websocket connection.

The data that an event emits, is added onto the arguents the same way it is with results from `OBS Raw`, as well as a `%obsEvent._json%` variable that can be parsed in C# (`JObject.Parse()`) for easier use.

OBS events are per-connection based.

---

- [<i class="mdi mdi-chevron-right primary--text"></i>**OBS Studio Events *Full events reference***](/en/Broadcasters/OBS/Events)
- [<i class="mdi mdi-chevron-right primary--text"></i>**OBS Raw *Sub-Action for executing raw OBS requests***](/en/Sub-Actions/OBS/Raw)
- [<i class="mdi mdi-github"></i>**OBS Raw Requests *Reference of all requests supported with OBS Raw***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#requests)
{.btn-grid .my-5}