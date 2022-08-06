---
title: GetCurrentProgramScene
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-07-31T00:21:50.186Z
tags: 
editor: markdown
dateCreated: 2022-07-31T00:21:50.186Z
---

## Overview
Gets an array of all groups in OBS.

Groups in OBS are actually scenes, but renamed and modified. In obs-websocket, we treat them as scenes where we can.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.currentProgramSceneName` | `String`{.datatype} | Current program scene

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--1"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
```json
{
  "request-type": "GetCurrentProgramScene"
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getcurrentprogramscene)
{.btn-grid .my-5}