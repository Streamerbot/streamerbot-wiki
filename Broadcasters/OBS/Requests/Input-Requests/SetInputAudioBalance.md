---
title: SetInputAudioBalance
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:17:29.468Z
tags: 
editor: markdown
dateCreated: 2022-08-02T06:30:54.049Z
---

## Overview
Sets the audio balance of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to set the audio balance of
`inputAudioBalance` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | New audio balance value | `>= 0.0, <= 1.0`{.datatype}

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
  "requestType": "SetInputAudioBalance",
  "requestData": {
    "inputName": "",
    "inputAudioBalance": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputaudiobalance)
{.btn-grid .my-5}