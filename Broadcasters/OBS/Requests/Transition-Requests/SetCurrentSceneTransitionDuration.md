---
title: SetCurrentSceneTransitionDuration
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:33.403Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:42:03.954Z
---

## Overview
Sets the duration of the current scene transition, if it is not fixed.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`transitionDuration` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Duration in milliseconds | `>= 50, <= 20000`{.datatype}

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
  "requestType": "SetCurrentSceneTransitionDuration",
  "requestData": {
    "transitionDuration": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setcurrentscenetransitionduration)
{.btn-grid .my-5}