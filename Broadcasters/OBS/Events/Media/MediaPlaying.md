---
title: MediaPlaying
description: This event is only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.
published: true
date: 2022-07-03T21:10:43.990Z
tags: 
editor: markdown
dateCreated: 2022-06-28T16:20:32.304Z
---

# MediaPlaying

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `MediaPlaying`
| `obsEvent.sourceKind` | Source kind
| `obsEvent.sourceName` | Source name
| `obsEvent.update-type` | The update type of the OBS event in this case `MediaPlaying`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#mediaplaying)
* [<= Back](/en/Broadcasters/OBS/)
{.links-list}