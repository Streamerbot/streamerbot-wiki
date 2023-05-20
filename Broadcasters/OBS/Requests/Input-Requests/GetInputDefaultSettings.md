---
title: GetInputDefaultSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:16:13.650Z
tags: 
editor: markdown
dateCreated: 2022-08-01T03:27:11.633Z
---

## Overview
Gets the default settings for an input kind.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputKind` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Input kind to get the default settings for

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.defaultInputSettings` | `Object`{.datatype} | Object of default settings for the input kind

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
  "requestType": "GetInputDefaultSettings",
  "requestData": {
  "inputKind": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputdefaultsettings)
{.btn-grid .my-5}