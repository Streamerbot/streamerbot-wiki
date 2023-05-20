---
title: ToggleStream
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:40:02.900Z
tags: 
editor: markdown
dateCreated: 2022-08-05T19:27:52.787Z
---

## Overview
Toggles the status of the stream output.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.outputActive` | `Boolean`{.datatype} | New state of the stream output

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--1"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "ToggleStream"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#togglestream)
{.btn-grid .my-5}