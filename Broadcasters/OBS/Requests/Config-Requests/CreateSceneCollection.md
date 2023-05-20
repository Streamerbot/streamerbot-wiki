---
title: CreateSceneCollection
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:09.644Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:48:24.108Z
---

## Overview
Creates a new scene collection, switching to it in the process.

Note: This will block until the collection has finished changing.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneCollectionName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name for the new scene collection	

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
  "requestType": "CreateSceneCollection",
  "requestData": {
    "sceneCollectionName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#createscenecollection)
{.btn-grid .my-5}