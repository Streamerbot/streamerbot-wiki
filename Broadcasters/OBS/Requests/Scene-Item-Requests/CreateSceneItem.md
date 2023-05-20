---
title: CreateSceneItem
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:31:35.702Z
tags: 
editor: markdown
dateCreated: 2022-08-04T19:09:39.728Z
---

## Overview
Creates a new scene item using a source.

> Scenes only
{.is-warning}

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene to create the new item in
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source to add to the scene
`sceneItemEnabled` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Enable state to apply to the scene item on creation

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.sceneItemId` | `Number`{.datatype} | Numeric ID of the scene item

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
  "requestType": "CreateSceneItem",
  "requestData": {
    "sceneName": "",
    "sourceName": "",
    "sceneItemEnabled": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#createsceneitem)
{.btn-grid .my-5}