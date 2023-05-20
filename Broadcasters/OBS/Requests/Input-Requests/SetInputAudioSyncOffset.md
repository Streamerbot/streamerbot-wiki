---
title: SetInputAudioSyncOffset
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:17:47.424Z
tags: 
editor: markdown
dateCreated: 2022-08-02T07:40:42.028Z
---

## Overview
Sets the audio sync offset of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to set the audio sync offset of
`inputAudioSyncOffset` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | New audio sync offset in milliseconds | >= -950, <= 20000

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
  "requestType": "SetInputAudioSyncOffset",
  "requestData": {
    "inputName": "",
    "inputAudioSyncOffset": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputaudiosyncoffset)
{.btn-grid .my-5}