---
title: MediaNext
description: This event is only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.
published: true
date: 2022-07-03T21:10:27.114Z
tags: 
editor: markdown
dateCreated: 2022-06-28T16:29:57.611Z
---

# MediaNext

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `MediaNext`
| `obsEvent.sourceKind` | Source kind
| `obsEvent.sourceName` | Source name
| `obsEvent.update-type` | The update type of the OBS event in this case `MediaNext`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#medianext)
* [<= Back](/en/Integrations/OBS/OBS-Events)
{.links-list}