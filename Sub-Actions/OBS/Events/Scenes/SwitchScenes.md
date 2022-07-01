---
title: SwitchScenes
description: Indicates a scene change.
published: true
date: 2022-06-28T20:27:34.585Z
tags: 
editor: markdown
dateCreated: 2022-06-27T01:09:06.949Z
---

# SwitchScenes

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SwitchScenes`
| `obsEvent.scene-name` | The name of the scene it switches to
| `obsEvent.sources[#]` | The settings of the sources in the scene you switched to
| `obsEvent.update-type	` | The update type of the OBS event in this case `SwitchScenes`
| `obsEvent._json` | Everything above in a json format
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#switchscenes)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}