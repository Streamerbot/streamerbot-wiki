---
title: GetInputAudioSyncOffset
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:17:39.142Z
tags: 
editor: markdown
dateCreated: 2022-08-02T07:37:43.630Z
---

## Overview
Gets the audio sync offset of an input.

Note: The audio sync offset can be negative too!

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to get the audio sync offset of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputAudioSyncOffset` | `Number`{.datatype} | Audio sync offset in milliseconds

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
  "requestType": "GetInputAudioSyncOffset",
  "requestData": {
    "inputName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputaudiosyncoffset)
{.btn-grid .my-5}