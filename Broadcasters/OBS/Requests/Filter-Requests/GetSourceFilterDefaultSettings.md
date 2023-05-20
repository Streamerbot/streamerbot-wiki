---
title: GetSourceFilterDefaultSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:53.388Z
tags: 
editor: markdown
dateCreated: 2022-08-04T13:13:18.116Z
---

## Overview
Gets the default settings for a filter kind.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`filterKind` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Filter kind to get the default settings for

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.defaultFilterSettings` | `String`{.datatype} | Object of default settings for the filter kind

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
  "requestType": "GetSourceFilterDefaultSettings",
  "requestData": {
    "filterKind": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsourcefilterdefaultsettings)
{.btn-grid .my-5}