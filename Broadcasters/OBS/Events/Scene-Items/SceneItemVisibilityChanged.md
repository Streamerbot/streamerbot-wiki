---
title: SceneItemVisibilityChanged
description: A scene item's visibility has been toggled.
published: true
date: 2022-07-03T21:40:53.401Z
tags: 
editor: markdown
dateCreated: 2022-06-28T17:45:20.166Z
---

# SceneItemVisibilityChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SceneItemVisibilityChanged`
| `obsEvent.item-id` | Scene item ID
| `obsEvent.item-name` | Name of the item removed from the scene
| `obsEvent.item-visible` | New visibility state of the item.
| `obsEvent.scene-name` | Name of the scene
| `obsEvent.update-type` | The update type of the OBS event in this case `SceneItemVisibilityChanged`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sceneitemvisibilitychanged)
* [<= Back](/en/Broadcasters/OBS/)
{.links-list}