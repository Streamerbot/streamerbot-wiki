---
title: GetProfileParameter
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-07T09:12:19.306Z
tags: 
editor: markdown
dateCreated: 2022-08-07T09:12:19.306Z
---

## Overview
Gets a parameter from the current profile's configuration.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`parameterCategory` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Category of the parameter to get
`parameterName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the parameter to get

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.parameterValue` | `String`{.datatype} | Value associated with the parameter. `null` if not set and no default
`obsRaw.defaultParameterValue` | `String`{.datatype} | Default value associated with the parameter. `null` if no default

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--4"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "request-type": "GetProfileParameter",
  "parameterCategory": "",
  "parameterName": ""
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getprofileparameter)
{.btn-grid .my-5}