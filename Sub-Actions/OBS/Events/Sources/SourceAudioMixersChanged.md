---
title: SourceAudioMixersChanged
description: Audio mixer routing changed on a source.
published: true
date: 2022-07-06T21:21:42.967Z
tags: 
editor: markdown
dateCreated: 2022-07-06T21:21:39.731Z
---

# SourceAudioMixersChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SourceAudioMixersChanged`
| `obsEvent.hexMixersValue` | Raw mixer flags (little-endian, one bit per mixer) as an hexadecimal value
| `obsEvent.mixers[#].enabled` | Routing status
| `obsEvent.mixers[#].id`	| Mixer number
| `obsEvent.sourceName` | Source name
| `obsEvent.update-type` | The update type of the OBS event in this case `SourceAudioMixersChanged`
| `obsEvent._json` | Everything above in a JSON format

* [Official OBS WebSocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sourceaudiomixerschanged)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}