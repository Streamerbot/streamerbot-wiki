---
title: GetSpecialInputs
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:15:39.778Z
tags: 
editor: markdown
dateCreated: 2022-08-01T03:10:43.510Z
---

## Overview
Gets the names of all special inputs.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.desktop1` | `String`{.datatype} | Name of the Desktop Audio input
`obsRaw.desktop2` | `String`{.datatype} | Name of the Desktop Audio 2 input
`obsRaw.mic1` | `String`{.datatype} | Name of the Mic/Auxiliary Audio input
`obsRaw.mic2` | `String`{.datatype} | Name of the Mic/Auxiliary Audio 2 input
`obsRaw.mic3` | `String`{.datatype} | Name of the Mic/Auxiliary Audio 3 input
`obsRaw.mic4` | `String`{.datatype} | Name of the Mic/Auxiliary Audio 4 input

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
  "requestType": "GetSpecialInputs"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getspecialinputs)
{.btn-grid .my-5}