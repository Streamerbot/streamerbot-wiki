---
title: BroadcastCustomEvent
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T13:58:02.844Z
tags: 
editor: markdown
dateCreated: 2022-08-07T08:24:52.588Z
---

## Overview
Broadcasts a `CustomEvent` to all WebSocket clients. Receivers are clients which are identified and subscribed.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`eventData` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Data payload to emit to all receivers

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
  "requestType":  "BroadcastCustomEvent",
	"requestData": {	
  "eventData": {
    "": ""
  }
	}
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#broadcastcustomevent)
{.btn-grid .my-5}