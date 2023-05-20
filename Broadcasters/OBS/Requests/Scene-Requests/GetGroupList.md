---
title: GetGroupList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:13:43.775Z
tags: 
editor: markdown
dateCreated: 2022-07-31T00:18:06.079Z
---

## Overview
Gets an array of all groups in OBS.

Groups in OBS are actually scenes, but renamed and modified. In obs-websocket, we treat them as scenes where we can.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.groups` | `Array<String>`{.datatype} | Array of group names

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
  "requestType": "GetGroupList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getgrouplist)
{.btn-grid .my-5}