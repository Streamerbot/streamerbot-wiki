---
title: CreateSourceFilter
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:57.398Z
tags: 
editor: markdown
dateCreated: 2022-08-04T13:18:30.319Z
---

## Overview
Creates a new filter, adding it to the specified source.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source to add the filter to
`filterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the new filter to be created
`filterKind` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | The kind of filter to be created
`filterSettings` | `Object`{.datatype} | <i class="mdi mdi-close-thick"></i> | Settings object to initialize the filter with

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
  "requestType": "CreateSourceFilter",
  "requestData": {
    "sourceName": "",
    "filterName": "",
    "filterKind": "",
    "filterSettings": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#createsourcefilter)
{.btn-grid .my-5}