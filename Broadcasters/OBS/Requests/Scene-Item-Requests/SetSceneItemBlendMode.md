---
title: SetSceneItemBlendMode
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:33:04.841Z
tags: 
editor: markdown
dateCreated: 2022-08-05T08:57:17.609Z
---

## Overview
Sets the blend mode of a scene item.

### Blend modes
* OBS_BLEND_NORMAL
* OBS_BLEND_ADDITIVE
* OBS_BLEND_SUBTRACT
* OBS_BLEND_SCREEN
* OBS_BLEND_MULTIPLY
* OBS_BLEND_LIGHTEN
* OBS_BLEND_DARKEN
{.links-list}

Scenes and Groups

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene the item is in
`sceneItemId` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Numeric ID of the scene item	| `>= 0`{.datatype}
`sceneItemBlendMode` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | New blend mode

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--2"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "SetSceneItemBlendMode",
  "requestData": {
    "sceneName": "",
    "sceneItemId": ,
    "sceneItemBlendMode": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setsceneitemblendmode)
{.btn-grid .my-5}