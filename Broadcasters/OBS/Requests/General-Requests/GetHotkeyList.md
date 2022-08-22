---
title: GetHotkeyList
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T13:58:49.490Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:16:17.936Z
---

## Overview
Gets an array of all hotkey names in OBS

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.hotkeys` | `Array<String>`{.datatype} | Array of hotkey names

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
  "request-type": "GetHotkeyList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#gethotkeylist)
{.btn-grid .my-5}