---
title: SetInputAudioTracks
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:18:20.233Z
tags: 
editor: markdown
dateCreated: 2022-08-04T05:33:54.615Z
---

## Overview
Sets the enable state of audio tracks of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input
`inputAudioTracks` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Track settings to apply

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
  "requestType": "SetInputAudioTracks",
  "requestData": {
    "inputName": "",
    "inputAudioTracks": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputaudiotracks)
{.btn-grid .my-5}