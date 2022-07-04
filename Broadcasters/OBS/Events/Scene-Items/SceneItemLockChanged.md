---
title: SceneItemLockChanged
description: A scene item's locked status has been toggled.
published: true
date: 2022-07-03T21:40:08.968Z
tags: 
editor: markdown
dateCreated: 2022-06-28T17:48:06.836Z
---

# SceneItemLockChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SceneItemLockChanged`
| `obsEvent.item-id` | Scene item ID
| `obsEvent.item-locked` | New locked state of the item
| `obsEvent.item-name` | Name of the item removed from the scene
| `obsEvent.scene-name` | Name of the scene
| `obsEvent.update-type` | The update type of the OBS event in this case `SceneItemLockChanged`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sceneitemlockchanged)
* [<= Back](/en/Integrations/OBS/OBS-Events)
{.links-list}