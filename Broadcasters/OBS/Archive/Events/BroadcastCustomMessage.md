---
title: BroadcastCustomMessage
description: OBS Studio Events Reference (Archive)
published: true
date: 2022-10-29T22:23:27.085Z
tags: 
editor: markdown
dateCreated: 2022-06-27T20:56:37.417Z
---

## Overview
A custom broadcast message, sent by the server, requested by one of the websocket clients.

## Variables
Name | Description
----:|:------------
`obsEvent.event` | The OBS event in this case `BroadcastCustomMessage`
`data` | User-defined data
`realm` | Identifier provided by the sender
`obsEvent.update-type` | The update type of the OBS event in this case `BroadcastCustomMessage`
`obsEvent._json` | Everything above in a json format
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Archive *Go Back***](/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github grey--text"></i> **OBS WebSocket Documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#broadcastcustommessage)
{.btn-grid my-5}
