---
title: GetVersion
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-07-23T00:37:10.853Z
tags: 
editor: markdown
dateCreated: 2022-07-23T00:21:44.682Z
---

## Overview
Gets data about the current plugin and RPC version.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.obsVersion` | *string*{.datatype} | Current OBS Studio version
`obsRaw.obsWebSocketVersion` | *string*{.datatype} | Current obs-websocket version 
`obsRaw.rpcVersion` | *integer*{.datatype} | Current latest obs-websocket RPC version
`obsRaw.availableRequests` | `array<string>`{.datatype} | Array of available RPC requests for the currently negotiated RPC version 
`obsRaw.supportedImageFormats` | `array<string>`{.datatype} | Image formats available in `GetSourceScreenshot` and `SaveSourceScreenshot` requests.
`obsRaw.platform` | *string*{.datatype} | Name of the platform. Usually `windows`, `macos`, or `ubuntu` (linux flavor). Not guaranteed to be any of those
`obsRaw.platformDescription` | *string*{.datatype} | Description of the platform, like `Windows 11 (11.0)`

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--1"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Copy/Paste
```json
{
"request-type": "GetVersion"
}
```
---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this event***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getversion)
{.btn-grid my-5}