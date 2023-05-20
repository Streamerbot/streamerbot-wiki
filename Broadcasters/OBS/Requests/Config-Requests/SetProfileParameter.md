---
title: SetProfileParameter
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:43.881Z
tags: 
editor: markdown
dateCreated: 2022-08-07T09:15:20.062Z
---

## Overview
Sets the value of a parameter in the current profile's configuration.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`parameterCategory` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Category of the parameter to set
`parameterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the parameter to set
`parameterValue` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Value of the parameter to set. Use `null` to delete

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
  "requestType": "SetProfileParameter",
  "requestData": {
    "parameterCategory": "",
    "parameterName": "",
    "parameterValue": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setprofileparameter)
{.btn-grid .my-5}