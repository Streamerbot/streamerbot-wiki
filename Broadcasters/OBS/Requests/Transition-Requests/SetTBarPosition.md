---
title: SetTBarPosition
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:46.696Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:59:11.613Z
---

## Overview
Sets the position of the TBar.

Very important note: This will be deprecated and replaced in a future version of obs-websocket.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`position` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | New position | `>= 0.0, <= 1.0`{.datatype}
`release` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Whether to release the TBar. Only set `false` if you know that you will be sending another position update

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
  "requestType": "SetTBarPosition",
  "requestData": {
    "position": "",
    "release": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#settbarposition)
{.btn-grid .my-5}