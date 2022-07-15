---
title: SceneCollectionListChanged
description: Triggered when a scene collection is created, added, renamed, or removed.
published: true
date: 2022-07-06T20:54:24.121Z
tags: 
editor: markdown
dateCreated: 2022-06-27T02:04:40.915Z
---

# SceneCollectionChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SceneCollectionListChanged`
| `obsEvent.sceneCollections[#].name` | The names of your scene collections
| `obsEvent.update-type	` | The update type of the OBS event in this case `SceneCollectionListChanged`
| `obsEvent._json` | Everything above in a json format
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#scenecollectionlistchanged)
* [<= Back](/en/Broadcasters/OBS/Events)
{.links-list}