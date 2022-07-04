---
title: SourceOrderChanged
description: Scene items within a scene have been reordered.
published: true
date: 2022-07-03T21:41:27.477Z
tags: 
editor: markdown
dateCreated: 2022-06-28T16:47:50.777Z
---

# SourceOrderChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SourceOrderChanged`
| `obsEvent.scene-items[#].item-id` | Scene item unique ID
| `obsEvent.scene-items[#].source-name` | Item source name
| `obsEvent.scene-name` | Name of the scene where items have been reordered
| `obsEvent.update-type` | The update type of the OBS event in this case `SourceOrderChanged`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sourceorderchanged)
* [<= Back](/en/Integrations/OBS/OBS-Events)
{.links-list}