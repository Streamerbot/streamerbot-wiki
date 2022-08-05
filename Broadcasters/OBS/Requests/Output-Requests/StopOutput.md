---
title: StopOutput
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-05T14:58:31.214Z
tags: 
editor: markdown
dateCreated: 2022-08-05T14:58:31.214Z
---

## Overview
Stops an output.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`outputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Output name

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--4"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Copy/Paste
```json
{
  "request-type": "StopOutput",
  "outputName": ""
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#stopoutput)
{.btn-grid .my-5}