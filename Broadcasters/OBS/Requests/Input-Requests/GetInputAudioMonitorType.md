---
title: GetInputAudioMonitorType
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T14:42:59.083Z
tags: 
editor: markdown
dateCreated: 2022-08-02T07:46:11.809Z
---

## Overview
Gets the audio monitor type of an input.

The available audio monitor types are:

* `OBS_MONITORING_TYPE_NONE`
* `OBS_MONITORING_TYPE_MONITOR_ONLY`
* `OBS_MONITORING_TYPE_MONITOR_AND_OUTPUT`

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to get the audio monitor type of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.monitorType` | `String`{.datatype} | Audio monitor type

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
  "request-type": "GetInputAudioMonitorType",
  "inputName": ""
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputaudiomonitortype)
{.btn-grid .my-5}