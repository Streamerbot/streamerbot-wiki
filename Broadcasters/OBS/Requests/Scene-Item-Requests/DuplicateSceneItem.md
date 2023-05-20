---
title: DuplicateSceneItem
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:31:49.567Z
tags: 
editor: markdown
dateCreated: 2022-08-04T19:19:00.007Z
---

## Overview
Duplicates a scene item, copying all transform and crop info.

> Scenes only
{.is-warning}

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene the item is in
`sceneItemId` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Numeric ID of the scene item	| `>= 0`{.datatype}
`destinationSceneName` | `String`{.datatype} | <i class="mdi mdi-close-thick"></i> | Name of the scene to create the duplicated item in

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.sceneItemId` | `Number`{.datatype} | Numeric ID of the duplicated scene item

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
  "requestType": "DuplicateSceneItem",
  "requestData": {
    "sceneName": "",
    "sceneItemId": ,
    "destinationSceneName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#duplicatesceneitem)
{.btn-grid .my-5}