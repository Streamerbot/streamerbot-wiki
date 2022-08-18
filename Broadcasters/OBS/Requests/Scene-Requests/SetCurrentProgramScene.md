---
title: SetCurrentProgramScene
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T14:25:31.259Z
tags: 
editor: markdown
dateCreated: 2022-07-31T12:52:30.348Z
---

## Overview
Sets the current program scene.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Scene to set as the current program scene

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
  "requestType":  "SetCurrentProgramScene",
	"requestData": {	
  "sceneName": ""
	}
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setcurrentprogramscene)
{.btn-grid .my-5}