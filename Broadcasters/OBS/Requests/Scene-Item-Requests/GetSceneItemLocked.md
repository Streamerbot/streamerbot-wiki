---
title: GetSceneItemLocked
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:32:24.351Z
tags: 
editor: markdown
dateCreated: 2022-08-05T08:22:35.148Z
---

## Overview
Gets the lock state of a scene item.

Scenes and Groups

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene the item is in
`sceneItemId` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Numeric ID of the scene item	| `>= 0`{.datatype}

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.sceneItemLocked` | `Boolean`{.datatype} | Whether the scene item is locked. `true` for locked, `false` for unlocked

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--3"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "GetSceneItemLocked",
  "requestData": {
    "sceneName": "",
    "sceneItemId": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsceneitemlocked)
{.btn-grid .my-5}