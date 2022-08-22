---
title: RemoveScene
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T14:25:04.763Z
tags: 
editor: markdown
dateCreated: 2022-07-31T12:59:44.246Z
---

## Overview
Removes a scene from OBS.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene to remove	

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
  "requestType":  "RemoveScene",
	"requestData": {	
  "sceneName": ""
	}
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#removescene)
{.btn-grid .my-5}