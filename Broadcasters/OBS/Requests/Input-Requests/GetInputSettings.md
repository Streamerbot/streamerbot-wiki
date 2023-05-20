---
title: GetInputSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:16:22.187Z
tags: 
editor: markdown
dateCreated: 2022-08-01T03:30:14.263Z
---

## Overview
Gets the settings of an input.

Note: Does not include defaults. To create the entire settings object, overlay `inputSettings` over the `defaultInputSettings` provided by `GetInputDefaultSettings`.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to get the settings of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputSettings` | `Object`{.datatype} | Object of settings for the input
`obsRaw.inputKind` | `String`{.datatype} | The kind of the input

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
  "requestType": "GetInputSettings",
  "requestData": {
    "inputName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputsettings)
{.btn-grid .my-5}