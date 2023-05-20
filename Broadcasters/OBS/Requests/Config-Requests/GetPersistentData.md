---
title: GetPersistentData
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:06:55.989Z
tags: 
editor: markdown
dateCreated: 2022-08-07T09:03:06.574Z
---

## Overview
Gets the value of a "slot" from the selected persistent data realm.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`realm` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | The data realm to select. `OBS_WEBSOCKET_DATA_REALM_GLOBAL` or `OBS_WEBSOCKET_DATA_REALM_PROFILE`
`slotName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | The name of the slot to retrieve data from

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.slotValue` | `Any`{.datatype} | Value associated with the slot. `null` if not set

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
  "requestType": "GetPersistentData",
  "requestData": {
    "realm": "",
    "slotName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getpersistentdata)
{.btn-grid .my-5}