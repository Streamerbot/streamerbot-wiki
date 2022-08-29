---
title: MediaStopped
description: This event is only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.
published: true
date: 2022-06-29T02:40:30.815Z
tags: 
editor: markdown
dateCreated: 2022-06-28T16:27:45.471Z
---

# MediaStopped

## Variables

Name | Description
----:|:------------
| `obsEvent.event` | The OBS event in this case `MediaStopped`
| `obsEvent.sourceKind` | Source kind
| `obsEvent.sourceName` | Source name
| `obsEvent.update-type` | The update type of the OBS event in this case `MediaStopped`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#mediastopped)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}