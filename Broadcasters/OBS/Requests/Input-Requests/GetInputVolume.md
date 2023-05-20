---
title: GetInputVolume
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:17:02.077Z
tags: 
editor: markdown
dateCreated: 2022-08-02T05:59:47.693Z
---

## Overview
Gets the current volume setting of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to get the volume of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputVolumeMul` | `Number`{.datatype} | Volume setting in mul
`obsRaw.inputVolumeDb` | `Number`{.datatype} | Volume setting in dB

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
  "requestType": "GetInputVolume",
  "requestData": {
    "inputName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputvolume)
{.btn-grid .my-5}