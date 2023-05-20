---
title: OpenSourceProjector
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:43:19.557Z
tags: 
editor: markdown
dateCreated: 2022-08-06T18:36:36.176Z
---

## Overview
Opens a projector for a source.

Note: This request serves to provide feature parity with 4.x. It is very likely to be changed/deprecated in a future release.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source to open a projector for
`monitorIndex` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Monitor index, use `GetMonitorList` to obtain index | -1: Opens projector in windowed mode
`projectorGeometry` | `String`{.datatype} | <i class="mdi mdi-close-thick"></i> | Size/Position data for a windowed projector, in Qt Base64 encoded format. Mutually exclusive with `monitorIndex`

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
  "requestType": "OpenSourceProjector",
  "requestData": {
    "sourceName": "",
    "monitorIndex": ,
    "projectorGeometry": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#opensourceprojector)
{.btn-grid .my-5}