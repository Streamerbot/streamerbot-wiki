---
title: GetInputList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:15:20.707Z
tags: 
editor: markdown
dateCreated: 2022-08-01T03:04:59.472Z
---

## Overview
Gets an array of all inputs in OBS.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputKind` | `String`{.datatype} | <i class="mdi mdi-close-thick"></i> | Restrict the array to only inputs of the specified kind

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputs` | `Array<Object>`{.datatype} | Array of inputs

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
  "requestType": "GetInputList",
  "requestData": {
    "inputKind": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputlist)
{.btn-grid .my-5}