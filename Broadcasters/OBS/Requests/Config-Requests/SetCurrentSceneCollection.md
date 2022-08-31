---
title: SetCurrentSceneCollection
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-12T11:57:19.772Z
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
`sceneCollectionName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene collection to switch to

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--1"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "SetCurrentSceneCollection",
  "requestData": {
    "sceneCollectionName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setcurrentscenecollection)
{.btn-grid .my-5}