---
title: SetCurrentSceneCollection
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-07-30T01:45:17.972Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:42:05.100Z
---

## Overview
Switches to a scene collection.

Note: This will block until the collection has finished changing.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneCollectionName` | `String`{.datatype} | `True`{.datatype} | Name of the scene collection to switch to

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--1"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Copy/Paste
```json
{
  "request-type": "SetCurrentSceneCollection",
  "sceneCollectionName": ""
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this event***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#SetCurrentSceneCollection)
{.btn-grid .my-5}