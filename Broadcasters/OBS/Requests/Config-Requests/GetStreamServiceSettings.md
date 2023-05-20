---
title: GetStreamServiceSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:57.098Z
tags: 
editor: markdown
dateCreated: 2022-07-30T05:35:58.203Z
---

## Overview
Gets the current stream service settings (stream destination).

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.streamServiceType` | `String`{.datatype} | Stream service type, like `rtmp_custom` or `rtmp_common`
`obsRaw.streamServiceSettings` | `Object`{.datatype} | Stream service settings

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--4"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "GetStreamServiceSettings"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getstreamservicesettings)
{.btn-grid .my-5}