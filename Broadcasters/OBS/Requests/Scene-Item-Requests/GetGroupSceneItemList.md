---
title: GetGroupSceneItemList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:31:18.472Z
tags: 
editor: markdown
dateCreated: 2022-08-04T17:37:32.264Z
---

## Overview
Basically GetSceneItemList, but for groups.

Using groups at all in OBS is discouraged, as they are very broken under the hood.

> Groups only
{.is-warning}

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the group to get the items of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.sceneItems` | `Array<Object>`{.datatype} | Array of scene items in the group

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
  "requestType": "GetGroupSceneItemList",
  "requestData": {
    "sceneName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getgroupsceneitemlist)
{.btn-grid .my-5}