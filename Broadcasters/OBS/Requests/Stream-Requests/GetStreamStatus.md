---
title: GetStreamStatus
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:39:57.918Z
tags: 
editor: markdown
dateCreated: 2022-08-05T19:26:28.238Z
---

## Overview
Gets the status of the stream output.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.outputActive` | `Boolean`{.datatype} | Whether the output is active
`obsRaw.outputReconnecting` | `Boolean`{.datatype} | Whether the output is currently reconnecting
`obsRaw.outputTimecode` | `String`{.datatype} | Current formatted timecode string for the output
`obsRaw.outputDuration` | `Number`{.datatype} | Current duration in milliseconds for the output
`obsRaw.outputCongestion` | `Number`{.datatype} | Congestion of the output
`obsRaw.outputBytes` | `Number`{.datatype} | Number of bytes sent by the output
`obsRaw.outputSkippedFrames` | `Number`{.datatype} | Number of frames skipped by the output's process
`obsRaw.outputTotalFrames` | `Number`{.datatype} | Total number of frames delivered by the output's process

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
  "requestType": "GetStreamStatus"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getstreamstatus)
{.btn-grid .my-5}