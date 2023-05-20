---
title: SetSceneName
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:14:58.954Z
tags: 
editor: markdown
dateCreated: 2022-07-31T13:02:57.103Z
---

## Overview
Sets the name of a scene (rename).

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene to be renamed
`newSceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | New name for the scene	

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
  "requestType": "SetSceneName",
  "requestData": {
    "sceneName": "",
    "newSceneName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setscenename)
{.btn-grid .my-5}