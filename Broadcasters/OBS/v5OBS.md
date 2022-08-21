---
title: OBS Studio (v5)
description: Configuration page for one or more connection(s) to OBS Studio instance(s)
published: false
date: 2022-08-21T23:34:35.902Z
tags: 
editor: markdown
dateCreated: 2022-08-19T16:26:40.705Z
---

> OBS WebSocket *v4.9+*{.obs-version-badge} and *v5+*{.obs-version-badge} are both supported, but the documentation on the wiki is in *v5+*{.obs-version-badge}
{.is-info}

- [<img src="/logos/obs-websocket.png"/>**Download OBS WebSocket *<i class="mdi mdi-github"></i> obs-websocket v5+***](https://github.com/obsproject/obs-websocket/releases/latest)
{.btn-grid .my-5}

# Overview

Adding at least one OBS connection will allow Streamer.bot to control your OBS.

![overview](/broadcasters/obs/overview.png =1000x){.align-center}

Once configured, connected OBS sessions will report their status on this screen.

# Configuration
`Right-Click` `->` `Add` to define a new OBS connection

![connection](/broadcasters/obs/obs-connection.png =250x)

### Name
Enter any name or label to describe this OBS instance, e.g. `Local`

### Version
Select the version of OBS WebSocket to use for this connection.

> As of OBS Studio v28.0, OBS WebSocket v5+ is included by default. 
> To continue using OBS WebSocket v4.9+, you must install the *obs-websocket-4.9.1-compat*{.obs-version-badge} plugin
{.is-warning}

It is recommended to update to *v5+*{.obs-version-badge} if you are currently using an older version.

### Host
Default is localhost, `127.0.0.1`
To connect to another OBS instance on your local network, you can enter the local IP address, e.g. `192.168.1.10`

### Port
Default is: *v4.9+*{.obs-version-badge} = `4444` or *v5+*{.obs-version-badge} = `4455`
It's recommended to keep this the same unless you are using multiple OBS portable installs on your same desktop.

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

Select an OBS connection in the top panel, then `Right-Click` `->` `Add` in the bottom events panel to register an OBS event.

![add obs event currentprogramscenechanged](/broadcasters/obs/add-obs-event-currentprogramscenechanged.png =300x)

### Event
Select the event type from OBS

A reference of all OBS Studio events is available [here](/en/Broadcasters/OBS/Events)

### Group
Optional group name to keep your events organized

### Action
Select the action to be executed any time the selected event is fired off from OBS

***
### Sub-Actions
- [<i class="mdi mdi-lightning-bolt-outline text--obs"></i>**OBS Studio Sub-Actions *Control OBS with all these amazing sub-actions!***](/en/Sub-Actions/OBS)
{.btn-grid .my-5}

### OBS Raw
- [<i class="mdi mdi-code-json text--obs"></i>**OBS Raw *Sub-Action for executing raw OBS requests***](/en/Sub-Actions/OBS/Raw)
{.btn-grid .my-5}

### OBS Raw Requests
- [<i class="mdi mdi-progress-question text--obs"></i>**OBS Raw Requests *Reference of all requests supported with OBS Raw***](/en/Broadcasters/OBS/Requests)
{.btn-grid .my-5}