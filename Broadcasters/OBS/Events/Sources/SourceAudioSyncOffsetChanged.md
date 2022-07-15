---
title: SourceAudioSyncOffsetChanged
description: OBS Studio Events Reference
published: true
date: 2022-07-06T20:54:47.309Z
tags:
editor: markdown
dateCreated: 2022-06-28T15:18:29.858Z
---

# SourceAudioSyncOffsetChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SourceAudioSyncOffsetChanged`
| `obsEvent.sourceName` | Source name
| `obsEvent.syncOffset` | Audio sync offset of the source (in nanoseconds)
| `obsEvent.update-type` | The update type of the OBS event in this case `SourceAudioSyncOffsetChanged`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sourceaudiosyncoffsetchanged)
* [<= Back](/en/Broadcasters/OBS/Events)
{.links-list}