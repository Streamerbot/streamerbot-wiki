---
title: Sleep
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:05:09.862Z
tags: 
editor: markdown
dateCreated: 2022-08-07T08:41:22.866Z
---

## Overview
Sleeps for a time duration or number of frames. Only available in request batches with types `SERIAL_REALTIME` or `SERIAL_FRAME`.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sleepMillis` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Number of milliseconds to sleep for (if S`RIAL_REALTIME`mode) | `>= 0, <= 50000`{.datatype}
`sleepFrames` | `Number`{.datatype} | <i class="mdi mdi-check-bold"></i> | Number of frames to sleep for (if `SERIAL_FRAME`mode) | `>= 0, <= 10000`{.datatype}

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
  "requestType": "Sleep",
  "requestData": {
    "sleepMillis": ,
    "sleepFrames": 
  }
}
```

### C# Method
```csharp
CPH.ObsSendRaw("Sleep", "{'sleepMillis': , 'sleepFrames': }", 0);
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sleep)
{.btn-grid .my-5}