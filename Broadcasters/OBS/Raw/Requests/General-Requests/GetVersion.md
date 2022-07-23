---
title: GetVersion
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-07-23T00:34:03.096Z
tags: 
editor: markdown
dateCreated: 2022-07-23T00:21:44.682Z
---

## Overview
Gets data about the current plugin and RPC version.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.obsVersion` | *string*{.datatype} | Description
`obsRaw.obsWebSocketVersion` | *string*{.datatype} | Description 
`obsRaw.rpcVersion` | *integer*{.datatype} | Description
`obsRaw.availableRequests` | `array<string>`{.datatype} | Description 
`obsRaw.supportedImageFormats` | `array<string>`{.datatype} | Description
`obsRaw.platform` | *string*{.datatype} | Description 
`obsRaw.platformDescription` | *string*{.datatype} | Description

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