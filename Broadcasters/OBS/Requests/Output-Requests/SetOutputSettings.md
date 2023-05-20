---
title: SetOutputSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:35:27.897Z
tags: 
editor: markdown
dateCreated: 2022-08-05T19:22:35.284Z
---

## Overview
Sets the settings of an output.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`outputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Output name
`outputSettings` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Output settings

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--4"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "SetOutputSettings",
  "requestData": {
    "outputName": "",
    "outputSettings": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setoutputsettings)
{.btn-grid .my-5}