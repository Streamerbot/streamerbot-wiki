---
title: SetSceneSceneTransitionOverride
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T14:26:02.612Z
tags: 
editor: markdown
dateCreated: 2022-07-31T13:10:17.178Z
---

## Overview
Gets the scene transition overridden for a scene.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene
`transitionName` | `String`{.datatype} | <i class="mdi mdi-close-thick"></i> | Name of the scene transition to use as override. Specify `null` to remove
`transitionDuration` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Duration to use for any overridden transition. Specify `null` to remove | >= 50, <= 20000

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
  "requestType":  "SetSceneSceneTransitionOverride",
	"requestData": {	
  "sceneName": "",
  "transitionName": "",
  "transitionDuration": 
	}
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setscenescenetransitionoverride)
{.btn-grid .my-5}