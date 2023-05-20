---
title: SetSourceFilterSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:24:14.378Z
tags: 
editor: markdown
dateCreated: 2022-08-04T14:59:06.616Z
---

## Overview
Sets the settings of a source filter.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source the filter is on
`filterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the filter to set the settings of
`filterSettings` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Object of settings to apply
`overlay` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | True == apply the settings on top of existing ones, False == reset the input to its defaults, then apply settings.

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
  "requestType": "SetSourceFilterSettings",
  "requestData": {
    "sourceName": "",
    "filterName": "",
    "overlay": ,
    "filterSettings": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setsourcefiltersettings)
{.btn-grid .my-5}