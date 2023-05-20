---
title: GetVersion
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:04:23.435Z
tags: 
editor: markdown
dateCreated: 2022-07-23T00:21:44.682Z
---

## Overview
Gets data about the current plugin and RPC version.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.obsVersion` | `String`{.datatype} | Current OBS Studio version
`obsRaw.obsWebSocketVersion` | `String`{.datatype} | Current obs-websocket version 
`obsRaw.rpcVersion` | `Number`{.datatype} | Current latest obs-websocket RPC version
`obsRaw.availableRequests` | `Array<String>`{.datatype} | Array of available RPC requests for the currently negotiated RPC version 
`obsRaw.supportedImageFormats` | `Array<String>`{.datatype} | Image formats available in `GetSourceScreenshot` and `SaveSourceScreenshot` requests.
`obsRaw.platform` | `String`{.datatype} | Name of the platform. Usually `windows`, `macos`, or `ubuntu` (linux flavor). Not guaranteed to be any of those
`obsRaw.platformDescription` | `String`{.datatype} | Description of the platform, like `Windows 11 (11.0)`

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
  "requestType": "GetVersion"
}
```

### C# Method
```csharp
CPH.ObsSendRaw("GetVersion", "", 0);
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getversion)
{.btn-grid .my-5}