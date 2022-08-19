---
title: OBS Studio (v5)
description: Configuration page for one or more connection(s) to OBS Studio instance(s)
published: false
date: 2022-08-19T18:30:58.551Z
tags: 
editor: markdown
dateCreated: 2022-08-19T16:26:40.705Z
---

![obs.svg](/logos/obs.svg){.align-abstopright}

> OBS WebSocket *v4.9+*{.obs-version-badge} and *v5+*{.obs-version-badge} are both supported.
{.is-info}

- [<img src="/logos/obs-websocket.png"/>**Download OBS WebSocket *<i class="mdi mdi-github"></i> obs-websocket v5+***](https://github.com/obsproject/obs-websocket/releases/latest)
{.btn-grid .my-5}

# Overview

Adding at least one connection will allow Streamer.bot to control your OBS instance with all [OBS sub-actions](/Sub-Actions/OBS) or via the [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code) sub-action.

![overview](/broadcasters/obs/overview.png =700x)

Once configured, connected OBS sessions will report their status on this screen.

# Configuration
`Right-Click` -> `Add` to define a new OBS connection

![connection](/broadcasters/obs/obs-connection.png =250x)

### Name
Enter any name or label to describe this OBS instance, e.g. `Local`

### Version
Select the version of OBS WebSocket to use for this connection.

As of OBS Studio v28.0, OBS WebSocket 5.0 is included in the software by default. To continue using v4.9 requires the `obs-websocket-4.9.1-compat plugin`.
You can still use *v4.9+*{.obs-version-badge} but it's recommended to change to *v5+*{.obs-version-badge} because *v4.9+*{.obs-version-badge} won't be supported forever.

### Host
Default is localhost, `127.0.0.1`
To connect to another OBS instance on your local network, you can enter the local IP address, e.g. `192.168.1.10`

### Port
Default is `4444` *v4.9*{.obs-version-badge} or `4455` *v5+*{.obs-version-badge}
It's recommended to keep this the same unless you are using multiple OBS portable installs on the same desktop device.

### Password
Not required, devices can only connect to your OBS if they're on the same network as you.

### Auto Connect on Startup
When toggled this auto connects your OBS connection when you launch streamer.bot.

### Reconnect on Disconnect
When toggled this tries to reconnect (by default every 30s) when streamer.bot looses connection with your OBS.

### Retry Interval
When streamer.bot looses connection with your OBS this by default will try the reconnect every 30s, but you can change it to what you want.


# Status Panel
Overview of connection information available on the right-hand panel{.subtitle}

### OBS Information
Shows the version number of OBS and the installed WebSocket plugin

### Current Scene
Shows the name of the currently broadcasting scene on that connection

### Stream Status
Shows the status of current streaming and recording activity

### Sources
Lists all sources present on the currently selected scene

# Events
You can assign actions to events that OBS transmits across the WebSocket connection.

The data that an event emits, is added onto the arguments the same way it is with results from `OBS Raw`, as well as a `%obsEvent._json%` variable that can be parsed in C# (`JObject.Parse()`) for easier use.

OBS events are per-connection based.

---

- [<i class="mdi mdi-chevron-right primary--text"></i>**OBS Studio Events *Full events reference***](/en/Broadcasters/OBS/Events)
- [<i class="mdi mdi-chevron-right primary--text"></i>**OBS Raw *Sub-Action for executing raw OBS requests***](/en/Sub-Actions/OBS/Raw)
- [<i class="mdi mdi-github"></i>**OBS Raw Requests *Reference of all requests supported with OBS Raw***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#requests)
{.btn-grid .my-5}