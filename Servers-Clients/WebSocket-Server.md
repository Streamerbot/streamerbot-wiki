---
title: WebSocket Server
description: Configure the internal Streamer.bot WebSocket API
published: true
date: 2022-07-22T19:30:50.307Z
tags: websocket, api
editor: markdown
dateCreated: 2021-08-25T21:37:04.299Z
---

## Overview

Streamer.bot has an internal WebSocket server and API that can be enabled in the `Servers/Clients -> WebSocket Server` tab.

This allows you to connect to your Streamer.bot application using any WebSocket client and react to events in real time.

> **WARNING**
> Your client must [Subscribe](/Servers-Clients/WebSocket-Server/Requests#subscribe) to any events it wishes to receive from Streamer.bot
{.is-warning}

![Websocket Server settings](/123519236-e8475600-d6a1-11eb-8b9c-ef7390e48968.png =350x)

## Configuration
### Auto-Start
Enable to auto-start the WebSocket server when you open Streamer.bot

### Address
The IP address the server should bind to, defaults to `127.0.0.1`

If you need to connect to Streamer.bot from another machine on your local network, set this to your internal LAN IP, e.g. `192.168.0.25`

### Port
The port the server should bind to, defaults to `8080`

Change this if you already have another service using the default port, or have multiple Streamer.bot instances running.

### Endpoint
The endpoint path for all requests, defaults to `/`

Changing this will require you to connect at the configured location, e.g. `ws://127.0.0.1/myendpoint`


## API Reference

- [<i class="mdi mdi-upload-network primary--text"></i> **WebSocket Requests *Reference of all requests you can make to the Streamer.bot WebSocket API***](/Servers-Clients/WebSocket-Server/Requests)
- [<i class="mdi mdi-download-network primary--text"></i> **WebSocket Events *Reference of all events emitted over the Streamer.bot WebSocket API***](/Servers-Clients/WebSocket-Server/Events)
{.btn-grid .my-5}

