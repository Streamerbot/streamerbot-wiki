---
title: ScenesChanged
description: Note: This event is not fired when the scenes are reordered.
published: true
date: 2022-06-28T20:28:25.467Z
tags: 
editor: markdown
dateCreated: 2022-06-27T01:53:30.436Z
---

# ScenesChanged

## Variables

| Variable | Description | Notes |
|---------:|:------------|-------|
| `obsEvent.event` | The OBS event in this case `ScenesChanged`
| `obsEvent.scene-name` | The name of the scene it switches to
| `obsEvent.scenes[#]` | The settings of all your OBS scenes | (**Note** this gives a lot of variables, it can be in the thousands)
| `obsEvent.update-type	` | The update type of the OBS event in this case `ScenesChanged`
| `obsEvent._json` | Everything above in a json format | (**Note** This variable can be empty, because the variable other wise would have been too long)
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sceneschanged)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}