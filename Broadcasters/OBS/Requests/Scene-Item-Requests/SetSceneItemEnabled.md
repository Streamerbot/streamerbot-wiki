---
title: SetSceneItemEnabled
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:32:17.715Z
tags: 
editor: markdown
dateCreated: 2022-08-05T08:17:08.157Z
---

## Overview
Sets the enable state of a scene item.

Scenes and Groups

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene the item is in
`sceneItemId` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Numeric ID of the scene item | `>= 0`{.datatype}
`sceneItemEnabled` | `Boolean`{.datatype} | <i class="mdi mdi-check-bold"></i> | New enable state of the scene item

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
  "requestType": "SetSceneItemEnabled",
  "requestData": {
    "sceneName": "",
    "sceneItemId": ,
    "sceneItemEnabled": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setsceneitemenabled)
{.btn-grid .my-5}