---
title: GetMonitorList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:43:03.288Z
tags: 
editor: markdown
dateCreated: 2022-08-06T18:29:40.159Z
---

## Overview
Gets a list of connected monitors and information about them.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.monitors` | `Array<Object>`{.datatype} | a list of detected monitors with some information

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
  "requestType": "GetMonitorList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getmonitorlist)
{.btn-grid .my-5}