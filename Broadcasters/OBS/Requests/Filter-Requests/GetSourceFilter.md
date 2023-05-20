---
title: GetSourceFilter
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:24:06.244Z
tags: 
editor: markdown
dateCreated: 2022-08-04T14:32:57.537Z
---

## Overview
Gets the info for a specific source filter.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Description
`filterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Description

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.filterEnabled` | `Boolean`{.datatype} | Whether the filter is enabled
`obsRaw.filterIndex` | `Number`{.datatype} | Index of the filter in the list, beginning at 0
`obsRaw.filterKind` | `String`{.datatype} | The kind of filter
`obsRaw.filterSettings` | `Object`{.datatype} | Settings object associated with the filter

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
  "requestType": "GetSourceFilter",
  "requestData": {
    "sourceName": "",
    "filterName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsourcefilter)
{.btn-grid .my-5}