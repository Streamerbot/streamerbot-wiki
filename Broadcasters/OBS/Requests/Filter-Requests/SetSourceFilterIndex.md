---
title: SetSourceFilterIndex
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:24:14.894Z
tags: 
editor: markdown
dateCreated: 2022-08-04T14:49:07.644Z
---

## Overview
Sets the index position of a filter on a source.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source the filter is on
`filterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the filter
`filterIndex` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | New index position of the filter | `>= 0`{.datatype}

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
  "requestType": "SetSourceFilterIndex",
  "requestData": {
    "sourceName": "",
    "filterName": "",
    "filterIndex": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setsourcefilterindex)
{.btn-grid .my-5}