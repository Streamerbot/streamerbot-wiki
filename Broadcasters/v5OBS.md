---
title: OBS Studio (v5)
description: Configuration page for one or more connection(s) to OBS Studio instance(s)
published: false
date: 2022-08-20T11:40:12.678Z
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

> As of OBS Studio v28.0, OBS WebSocket v5.0 is included by default. 
> To continue using OBS WebSocket v4.9, you must install the *obs-websocket-4.9.1-compat*{.obs-version-badge} plugin
{.is-warning}

It is recommended to update to *v5.0.0*{.obs-version-badge} if you are currently using an older version.

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

Select an OBS connection in the top panel, then `Right-Click` -> `Add` in the bottom events panel to register an OBS event.

![add obs event currentprogramscenechanged](/broadcasters/obs/add-obs-event-currentprogramscenechanged.png =300x)

### Event
Select the event type from OBS

A reference of all OBS Studio events is available [here](/en/Broadcasters/OBS/Events)

### Group
Optional group name to keep your events organized

### Action
Select the action to be executed any time the selected event is fired off from OBS

---

- [<img src="/logos/obs.svg"></img>**OBS Raw *Sub-Action for executing raw OBS requests***](/en/Sub-Actions/OBS/Raw)
- [<i class="mdi mdi-progress-question text--obs"></i>**OBS Raw Requests *Reference of all requests supported with OBS Raw***](/en/Broadcaster/OBS/Requests)
{.btn-grid .my-5}