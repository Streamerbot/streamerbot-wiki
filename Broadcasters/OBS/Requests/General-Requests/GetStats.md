---
title: GetStats
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:04:33.233Z
tags: 
editor: markdown
dateCreated: 2022-07-25T18:13:25.840Z
---

## Overview
Gets statistics about OBS, obs-websocket, and the current session.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.cpuUsage` | `Number`{.datatype} | Current CPU usage in percent
`obsRaw.memoryUsage` | `Number`{.datatype} | Amount of memory in MB currently being used by OBS
`obsRaw.availableDiskSpace` | `Number`{.datatype} | Available disk space on the device being used for recording storage
`obsRaw.activeFps` | `Number`{.datatype} | Current FPS being rendered 
`obsRaw.averageFrameRenderTime` | `Number`{.datatype} | Average time in milliseconds that OBS is taking to render a frame
`obsRaw.renderSkippedFrames` | `Number`{.datatype} | Number of frames skipped by OBS in the render thread 
`obsRaw.renderTotalFrames` | `Number`{.datatype} | Total number of frames outputted by the render thread
`obsRaw.outputSkippedFrames` | `Number`{.datatype} | Number of frames skipped by OBS in the output thread 
`obsRaw.outputTotalFrames` | `Number`{.datatype} | Total number of frames outputted by the output thread
`obsRaw.webSocketSessionIncomingMessages` | `Number`{.datatype} | Total number of messages received by obs-websocket from the client 
`obsRaw.webSocketSessionOutgoingMessages` | `Number`{.datatype} | Total number of messages sent by obs-websocket to the client

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
  "requestType": "GetStats"
}
```

### C# Method
```csharp
CPH.ObsSendRaw("GetStats", "", 0);
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getstats)
{.btn-grid .my-5}