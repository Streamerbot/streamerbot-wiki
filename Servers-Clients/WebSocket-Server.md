---
title: WebSocket Server
description: 
published: true
date: 2022-07-09T19:58:52.266Z
tags: websocket
editor: markdown
dateCreated: 2021-08-25T21:37:04.299Z
---

Connect to `Streamer.bot` with a websocket client, whether its from `JS`, or some other language, and react to events that happen within `Streamer.bot` in real time, and/or even from custom events you can emit from within the [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code)

![Websocket Server settings](/123519236-e8475600-d6a1-11eb-8b9c-ef7390e48968.png)

***
By going to the `Websockets` tab, and then the `Server` tab, you can change what `IP`, `Port` and the `endpoint` the server will listen on, as well as toggle it to auto start on application launch.

As of [Version 0.0.52](/Changelogs/Version-0052) the client connecting needs to [subscribe](/Servers-Clients/WebSocket-Server/Events) to the events it wishes to receive.

**Note** This is a work in progress document, and will be updated over time

**Note** If you wish to connect to **Streamer.bot** from another machine and/or device, be sure to change the IP from `127.0.0.1` to your PC's internal LAN IP (example `192.168.0.25`)

## Requests
See the [Websocket Server - Requests](/Servers-Clients/WebSocket-Server/Requests) for more details

* [Subscribe *Subscribe to specific events*](/Servers-Clients/WebSocket-Server/Requests#subscribe)
* [UnSubscribe *UnSubscribe from specific events*](/Servers-Clients/WebSocket-Server/Requests#unsubscribe)
* [GetEvents *Retrieve a list of all events that may be emitted*](/Servers-Clients/WebSocket-Server/Requests#getevents)
* [GetActions *Retrieve a list of all available actions*](/Servers-Clients/WebSocket-Server/Requests#getactions)
* [DoAction *Trigger an action*](/Servers-Clients/WebSocket-Server/Requests#doaction)
* GetCredits
* TestCredits
* ClearCredits
* GetActiveViewers (0.56)
{.links-list}

## Events Emitted
See the [Websocket Server - Events](/Servers-Clients/WebSocket-Server/Events) for more details

