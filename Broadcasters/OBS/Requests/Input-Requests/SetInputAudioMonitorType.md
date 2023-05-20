---
title: SetInputAudioMonitorType
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:18:07.325Z
tags: 
editor: markdown
dateCreated: 2022-08-02T07:50:54.471Z
---

## Overview
Sets the audio monitor type of an input.

The available audio monitor types are:

* `OBS_MONITORING_TYPE_NONE`
* `OBS_MONITORING_TYPE_MONITOR_ONLY`
* `OBS_MONITORING_TYPE_MONITOR_AND_OUTPUT`
{.links-list}

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to set the audio monitor type of
`monitorType` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Audio monitor type

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
  "requestType": "SetInputAudioMonitorType",
  "requestData": {
    "inputName": "",
  "monitorType": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputaudiomonitortype)
{.btn-grid .my-5}