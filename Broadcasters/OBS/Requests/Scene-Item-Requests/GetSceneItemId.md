---
title: GetSceneItemId
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:31:27.841Z
tags: 
editor: markdown
dateCreated: 2022-08-04T17:41:13.142Z
---

## Overview
Searches a scene for a source, and returns its id.

Scenes and Groups

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene or group to search in
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source to find
`searchOffset` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Number of matches to skip during search. >= 0 means first forward. -1 means last (top) item | `>= -1`{.datatype}

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
  "requestType": "GetSceneItemId",
  "requestData": {
    "sceneName": "",
    "sourceName": "",
    "searchOffset": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsceneitemid)
{.btn-grid .my-5}