---
title: SetInputVolume
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:17:14.768Z
tags: 
editor: markdown
dateCreated: 2022-08-02T06:14:44.537Z
---

## Overview
Sets the volume setting of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to set the volume of
`inputVolumeMul` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | New volume level multiplier | `>= 0, <= 20`{.datatype}
`inputVolumeDb` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | New volume level in dB | `>= -100, <= 26`{.datatype}

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
  "requestType": "SetInputVolume",
  "requestData": {
    "inputName": "",
    "inputVolumeMul": ,
    "inputVolumeDb": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputvolume)
{.btn-grid .my-5}