---
title: BroadcastCustomMessage
description: A custom broadcast message, sent by the server, requested by one of the websocket clients.
published: true
date: 2022-07-03T21:08:56.416Z
tags: 
editor: markdown
dateCreated: 2022-06-27T20:56:37.417Z
---

# BroadcastCustomMessage

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `BroadcastCustomMessage`
| `data` | User-defined data
| `realm` | Identifier provided by the sender
| `obsEvent.update-type` | The update type of the OBS event in this case `BroadcastCustomMessage`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#broadcastcustommessage)
* [<= Back](/en/Broadcasters/OBS/Events)
{.links-list}