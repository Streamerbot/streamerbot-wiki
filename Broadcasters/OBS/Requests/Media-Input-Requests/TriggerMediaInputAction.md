---
title: TriggerMediaInputAction
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:41:28.476Z
tags: 
editor: markdown
dateCreated: 2022-08-06T12:58:00.986Z
---

## Overview
Triggers an action on a media input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the media input
`mediaAction` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Identifier of the `ObsMediaInputAction` enum

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
  "requestType": "TriggerMediaInputAction",
  "requestData": {
    "inputName": "",
    "mediaAction": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#triggermediainputaction)
{.btn-grid .my-5}