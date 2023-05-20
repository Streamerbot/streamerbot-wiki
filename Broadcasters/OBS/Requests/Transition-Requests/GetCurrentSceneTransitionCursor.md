---
title: GetCurrentSceneTransitionCursor
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:40.138Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:49:36.239Z
---

## Overview
Gets the cursor position of the current scene transition.

Note: `transitionCursor` will return 1.0 when the transition is inactive.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.transitionCursor` | `Number`{.datatype} | Cursor position, between 0.0 and 1.0

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
  "requestType": "GetCurrentSceneTransitionCursor"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getcurrentscenetransitioncursor)
{.btn-grid .my-5}