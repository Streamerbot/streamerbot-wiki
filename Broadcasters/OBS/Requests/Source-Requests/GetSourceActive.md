---
title: GetSourceActive
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:08:09.273Z
tags: 
editor: markdown
dateCreated: 2022-07-30T23:07:34.159Z
---

## Overview
Gets the active and show state of a source.

**Compatible with inputs and scenes.**

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source to get the active state of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.videoActive` | `Boolean`{.datatype} | Whether the source is showing in Program
`obsRaw.videoShowing` | `Boolean`{.datatype} | Whether the source is showing in the UI (Preview, Projector, Properties)

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
  "requestType": "GetSourceActive",
  "requestData": {
    "sourceName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsourceactive)
{.btn-grid .my-5}