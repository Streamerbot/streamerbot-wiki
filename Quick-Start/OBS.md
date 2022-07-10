---
title: Quick Start - OBS Studio
description: Set up Streamer.bot to remotely control your OBS instance
published: true
date: 2022-07-10T01:33:32.353Z
tags: obs, guides
editor: markdown
dateCreated: 2022-07-10T01:33:32.353Z
---

# Prerequisites
To enable remote control of your `OBS` from **Streamer.bot** you will need to first install the OBS Websocket Plugin
> OBS Websocket v4.x is the only supported version at this time, v5.x requires a re-write and is being worked on, but is still missing capabilities
Download OBS Websocket plugin [here](https://obsproject.com/forum/resources/obs-websocket-remote-control-obs-studio-from-websockets.466/)
{.is-warning}

Once this is installed, configure your port settings and password if you want one inside OBS. You will need to match these settings in Streamer.bot
![WebsocketSettings](https://lh3.googleusercontent.com/-VCh9WVIx1ZI/YPtSPtSppaI/AAAAAAAAEA4/OK-jMEvnI3YAXDRBpLPhO8lG1V6jimZOwCLcBGAsYHQ/image.png)

# Configuration

Once configured, connected OBS sessions will report their status on the OBS tab in Streamer.bot

![obs_event_01_.png](/quick-start/obs_event_01_.png)

To add a new connection, `Right-Click` -> `Add` to open the new connection dialogue
![New Connection](/119574587-9adb7e80-bdad-11eb-82c1-ec9ed668a40d.png)

Give it a name and set the IP address and Port number of the OBS Websocket
The Default values of `127.0.0.1` and `4444` will look for the out-of-box configuration for OBS installed on the same computer as Streamer.bot is running

`Password` Will not be required unless you have specified one in OBS

> Connections can be configured to `Auto Connect on Startup`, and to `Reconnect on Disconnect` with a retry interval you specify in seconds
{.is-success}