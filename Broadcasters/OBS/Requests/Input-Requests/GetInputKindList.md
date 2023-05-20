---
title: GetInputKindList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:15:30.334Z
tags: 
editor: markdown
dateCreated: 2022-08-01T03:07:55.282Z
---

## Overview
Gets an array of all available input kinds in OBS.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`unversioned` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | True == Return all kinds as unversioned, False == Return with version suffixes (if available)	

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputKinds` | `Array<String>`{.datatype} | Array of input kinds

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
  "requestType": "GetInputKindList",
  "requestData": {
    "unversioned": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputkindlist)
{.btn-grid .my-5}