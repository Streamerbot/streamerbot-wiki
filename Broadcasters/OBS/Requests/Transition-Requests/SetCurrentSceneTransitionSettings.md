---
title: SetCurrentSceneTransitionSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:37.230Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:46:57.979Z
---

## Overview
Sets the settings of the current scene transition.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`transitionSettings` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Settings object to apply to the transition. Can be `{}`
`overlay` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Whether to overlay over the current settings or replace them

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
  "requestType": "SetCurrentSceneTransitionSettings",
  "requestData": {
    "transitionSettings": "",
    "overlay": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setcurrentscenetransitionsettings)
{.btn-grid .my-5}