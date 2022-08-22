---
title: SetInputMute
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T14:48:10.754Z
tags: 
editor: markdown
dateCreated: 2022-08-01T07:27:25.820Z
---

## Overview
Sets the audio mute state of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to set the mute state of
`inputMuted` | `Boolean`{.datatype} | <i class="mdi mdi-check-bold"></i> | Whether to mute the input or not

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
  "requestType":  "SetInputMute",
  "requestData": {
  "inputName": "",
  "inputMuted": 
 }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputmute)
{.btn-grid .my-5}