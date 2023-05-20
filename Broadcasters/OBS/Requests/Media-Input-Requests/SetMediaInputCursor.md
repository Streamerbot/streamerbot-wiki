---
title: SetMediaInputCursor
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:41:17.175Z
tags: 
editor: markdown
dateCreated: 2022-08-06T12:41:32.946Z
---

## Overview
Sets the cursor position of a media input.

This request does not perform bounds checking of the cursor position.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the media input
`mediaCursor` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | New cursor position to set | `>= 0	`{.datatype}

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
  "requestType": "SetMediaInputCursor",
  "requestData": {
    "inputName": "",
    "mediaCursor": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setmediainputcursor)
{.btn-grid .my-5}