---
title: GetSceneTransitionList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:21.520Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:28:27.288Z
---

## Overview
Gets an array of all scene transitions in OBS.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.currentSceneTransitionName` | `String`{.datatype} | Name of the current scene transition. Can be `null`
`obsRaw.currentSceneTransitionKind` | `String`{.datatype} | Kind of the current scene transition. Can be `null`
`obsRaw.transitions` | `Array<Object>`{.datatype} | Array of transitions

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
  "requestType": "GetSceneTransitionList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getscenetransitionlist)
{.btn-grid .my-5}