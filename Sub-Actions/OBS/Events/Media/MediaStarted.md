---
title: MediaStarted
description: These events are emitted by the OBS sources themselves. For example when the media file starts playing. The behavior depends on the type of media source being used.
published: true
date: 2022-06-29T02:40:41.902Z
tags: 
editor: markdown
dateCreated: 2022-06-28T16:33:33.821Z
---

# MediaStarted

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `MediaStarted`
| `obsEvent.sourceKind` | Source kind
| `obsEvent.sourceName` | Source name
| `obsEvent.update-type` | The update type of the OBS event in this case `MediaStarted`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#mediastarted)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}