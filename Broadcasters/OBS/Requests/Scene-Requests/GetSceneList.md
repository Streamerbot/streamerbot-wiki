---
title: GetSceneList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:13:34.485Z
tags: 
editor: markdown
dateCreated: 2022-07-31T00:15:21.233Z
---

## Overview
Gets an array of all scenes in OBS.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.currentProgramSceneName` | `String`{.datatype} | Current program scene
`obsRaw.currentPreviewSceneName` | `String`{.datatype} | Current preview scene. `null` if not in studio mode
`obsRaw.scenes` | `Array<Object>`{.datatype} | Array of scenes

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
  "requestType": "GetSceneList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getscenelist)
{.btn-grid .my-5}