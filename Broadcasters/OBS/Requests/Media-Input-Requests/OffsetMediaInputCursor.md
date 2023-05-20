---
title: OffsetMediaInputCursor
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:41:23.058Z
tags: 
editor: markdown
dateCreated: 2022-08-06T12:49:16.248Z
---

## Overview
Offsets the current cursor position of a media input by the specified value.

This request does not perform bounds checking of the cursor position.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the media input
`mediaCursorOffset` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Value to offset the current cursor position by

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
  "requestType": "OffsetMediaInputCursor",
  "requestData": {
    "inputName": "",
    "mediaCursorOffset": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#offsetmediainputcursor)
{.btn-grid .my-5}