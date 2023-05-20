---
title: GetSceneSceneTransitionOverride
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:15:07.395Z
tags: 
editor: markdown
dateCreated: 2022-07-31T13:06:38.675Z
---

## Overview
Gets the scene transition overridden for a scene.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.transitionName` | `String`{.datatype} | Name of the overridden scene transition, else `null`
`obsRaw.transitionDuration` | `Number`{.datatype} | Duration of the overridden scene transition, else `null`

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
  "requestType": "GetSceneSceneTransitionOverride",
  "requestData": {
    "sceneName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getscenescenetransitionoverride)
{.btn-grid .my-5}