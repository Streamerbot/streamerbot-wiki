---
title: GetSceneCollectionList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:02.694Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:39:03.276Z
---

## Overview
Gets an array of all scene collections

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.currentSceneCollectionName` | `String`{.datatype} | The name of the current scene collection
`obsRaw.sceneCollections` | `Array<String>`{.datatype} | Array of all available scene collections

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
  "requestType": "GetSceneCollectionList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getscenecollectionlist)
{.btn-grid .my-5}