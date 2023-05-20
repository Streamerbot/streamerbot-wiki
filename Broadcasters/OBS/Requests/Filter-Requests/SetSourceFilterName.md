---
title: SetSourceFilterName
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:24:03.188Z
tags: 
editor: markdown
dateCreated: 2022-08-04T14:28:55.687Z
---

## Overview
Sets the name of a source filter (rename).

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source the filter is on
`filterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Current name of the filter
`newFilterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | New name for the filter

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
  "requestType": "SetSourceFilterName",
  "requestData": {
    "sourceName": "",
    "filterName": "",
    "newFilterName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setsourcefiltername)
{.btn-grid .my-5}