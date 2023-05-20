---
title: SetInputSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:16:30.940Z
tags: 
editor: markdown
dateCreated: 2022-08-01T04:00:10.499Z
---

## Overview
Sets the settings of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to set the settings of
`inputSettings` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Object of settings to apply
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
  "requestType": "SetInputSettings",
  "requestData": {
    "inputName": "",
    "overlay": ,
    "inputSettings": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputsettings)
{.btn-grid .my-5}