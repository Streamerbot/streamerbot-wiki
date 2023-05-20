---
title: SetCurrentSceneTransition
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:30.687Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:37:20.251Z
---

## Overview
Sets the current scene transition.

Small note: While the namespace of scene transitions is generally unique, that uniqueness is not a guarantee as it is with other resources like inputs.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`transitionName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the transition to make active

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
  "requestType": "SetCurrentSceneTransition",
  "requestData": {
    "transitionName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setcurrentscenetransition)
{.btn-grid .my-5}