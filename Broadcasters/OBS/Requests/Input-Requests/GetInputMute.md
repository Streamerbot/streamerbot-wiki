---
title: GetInputMute
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:16:37.901Z
tags: 
editor: markdown
dateCreated: 2022-08-01T07:25:43.074Z
---

## Overview
Gets the audio mute state of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of input to get the mute state of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputMuted` | `Boolean`{.datatype} | Whether the input is muted

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
  "requestType": "GetInputMute",
  "requestData": {
    "inputName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputmute)
{.btn-grid .my-5}