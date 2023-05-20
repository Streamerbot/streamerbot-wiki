---
title: GetTransitionKindList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:17.074Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:25:40.278Z
---

## Overview
Gets an array of all available transition kinds.

Similar to `GetInputKindList`

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.transitionKinds` | `Array<String>`{.datatype} | Array of transition kinds

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
  "requestType": "GetTransitionKindList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#gettransitionkindlist)
{.btn-grid .my-5}