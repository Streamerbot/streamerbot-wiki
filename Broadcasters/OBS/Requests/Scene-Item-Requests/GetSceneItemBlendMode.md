---
title: GetSceneItemBlendMode
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-05T08:51:36.065Z
tags: 
editor: markdown
dateCreated: 2022-08-05T08:48:10.781Z
---

## Overview
Gets the blend mode of a scene item.

Blend modes:
* [**OBS_BLEND_NORMAL**](){.disabled}
* [**OBS_BLEND_ADDITIVE**](){.disabled}
* [**OBS_BLEND_SUBTRACT**](){.disabled}
* [**OBS_BLEND_SCREEN**](){.disabled}
* [**OBS_BLEND_MULTIPLY**](){.disabled}
* [**OBS_BLEND_LIGHTEN**](){.disabled}
* [**OBS_BLEND_DARKEN**](){.disabled}
{.btn-grid .my-5}

Scenes and Groups

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene the item is in
`sceneItemId` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Numeric ID of the scene item	| `>= 0`{.datatype}

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.sceneItemBlendMode` | `String`{.datatype} | Current blend mode

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--2"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Copy/Paste
```json
{
  "request-type": "GetSceneItemBlendMode",
  "sceneName": "",
  "sceneItemId": 
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsceneitemblendmode)
{.btn-grid .my-5}