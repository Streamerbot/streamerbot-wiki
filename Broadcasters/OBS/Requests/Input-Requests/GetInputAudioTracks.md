---
title: GetInputAudioTracks
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:18:13.909Z
tags: 
editor: markdown
dateCreated: 2022-08-02T11:11:43.011Z
---

## Overview
Gets the enable state of all audio tracks of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputAudioTracks` | `Object`{.datatype} | Object of audio tracks and associated enable states

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
  "requestType": "GetInputAudioTracks",
  "requestData": {
    "inputName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputaudiotracks)
{.btn-grid .my-5}