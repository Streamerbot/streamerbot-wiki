---
title: SetSceneItemTransform
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:32:04.834Z
tags: 
editor: markdown
dateCreated: 2022-08-05T07:58:07.898Z
---

## Overview
Sets the transform and crop info of a scene item.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene the item is in
`sceneItemId` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Numeric ID of the scene item | `>= 0`{.datatype}
`sceneItemTransform` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Object containing scene item transform info to update

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
  "requestType": "SetSceneItemTransform",
  "requestData": {
    "sceneName": "",
    "sceneItemId": ,
    "sceneItemTransform": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setsceneitemtransform)
{.btn-grid .my-5}