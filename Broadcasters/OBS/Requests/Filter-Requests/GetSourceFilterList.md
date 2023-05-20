---
title: GetSourceFilterList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:50.614Z
tags: 
editor: markdown
dateCreated: 2022-08-04T13:09:52.283Z
---

## Overview
Gets an array of all of a source's filters.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source	

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.filters` | `Array<Object>	`{.datatype} | Array of filters

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
  "requestType": "GetSourceFilterList",
  "requestData": {
    "sourceName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsourcefilterlist)
{.btn-grid .my-5}