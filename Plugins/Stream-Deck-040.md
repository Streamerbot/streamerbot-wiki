---
title: Stream Deck Plugin (v0.4.0)
description: The official Streamer.bot plugin for the Elgato Stream Deck
published: false
date: 2023-01-23T00:10:43.889Z
tags: 
editor: markdown
dateCreated: 2023-01-22T20:49:41.805Z
---

- [<i class="mdi mdi-download"></i> **Download *<i class="mdi mdi-github"></i> Download the latest version of this plugin***](https://github.com/nate1280/streamdeck-Streamer.bot/releases/latest/download/nate1280.streamerbot.streamDeckPlugin)
- [<i class="mdi mdi-chevron-right"></i> **Releases *<i class="mdi mdi-github"></i> View all versions of this plugin on GitHub***](https://github.com/nate1280/streamdeck-Streamer.bot/releases)
{.btn-grid .list .dense .my-5}

---

## Overview
This plugin allows you to execute Streamer.bot actions from your [Elgato Stream Deck](https://www.elgato.com/en/stream-deck)

![overview-040.png](/plugins/streamdeck/overview-040.png =300x)
![overview-action.png](/plugins/streamdeck/overview-action.png =500x)
![overview-action.png](/plugins/streamdeck/overview-push-to-run-actions.png =500x)

> This plugin requires the that the [WebSocket Server](/Servers-Clients/WebSocket-Server) is enabled in Streamer.bot
{.is-warning}

## Installation
1. Close down the `Stream Deck` application
1. Double click the `nate1280.streamerbot.streamDeckPlugin` file that you've downloaded above, this will automatically install the plugin
3. Make sure that the `Streamer.bot Authentication` field matches your [WebSocket Server](/en/Servers-Clients/WebSocket-Server) settings

## Configuration
### Title
The title of the button, when empty this will be the name of the action.

### Host
The host for the Streamer.bot websocket. This can most of the times stay `localhost`/`127.0.0.1`.

### Port
The port of the Streamer.bot websocket. This by default is `8080` and should ideally not be changed.

### Endpoint
The endpoint of the Streamer.bot websocket. This by default is `/` and should almost never need to be changed.

## Buttons
More details about each button{.subtitle}
- [<i class="mdi mdi-lightning-bolt"></i>**Action *Run a Streamer.bot Action***](/Plugins/Stream-Deck/Action)
- [<i class="mdi mdi-lightning-bolt"></i>**Push to run Actions *Run seperate actions when pressing and releasing the button***](/Plugins/Stream-Deck/Push-to-run-Actions)
{.btn-grid .list .my-5}

---

- [<i class="mdi mdi-chevron-left"></i>**Streamer.bot External Plugins *Go Back***](/Plugins)
{.btn-grid .my-5}