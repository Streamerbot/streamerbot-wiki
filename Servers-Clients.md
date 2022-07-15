---
title: Servers and Clients
description: 
published: true
date: 2022-07-09T19:55:04.255Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:22.739Z
---

# Servers / Clients

This tab contains the configuration options for external communication both in to and out of the streamer.bot application to enable interaction with [HTML Deck](/en/Extended-Features/HTML-Decks) functionality as well as with custom setups built by the community.

![servers-clients-018.png](/servers-clients-018.png)






Available as of [0.0.41](/Changelogs/Archives/Version-0041), websockets add another level to what you can do with Channel Points Handler

## Websocket Server
Connect to `Streamer.bot` with a websocket client, whether its from `JS`, or some other language, and react to events that happen within `Streamer.bot` in real time, and/or even from custom events you can emit from within the [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code)

See [Websocket Server](/Servers-Clients/WebSocket-Server) for more details on the Websocket Server

## Websocket Clients
Connect to other websocket servers and setup an action in [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code) to react to events that are emitted by the the server.  One example is to connect to the Data Puller Beat Saber mod and do various things depending on the data that is pushed out

**NOTE** Currently, due to the nature of the Websocket Client, the only real use for these is within the Execute C# code, sub-action will likely be created in due time.

See [Websocket Clients](/Servers-Clients/Websocket-Clients) for more details on the Websocket Clients