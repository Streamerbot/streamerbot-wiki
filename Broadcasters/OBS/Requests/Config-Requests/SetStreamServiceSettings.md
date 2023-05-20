---
title: SetStreamServiceSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:08:04.511Z
tags: 
editor: markdown
dateCreated: 2022-07-30T05:39:02.218Z
---

## Overview
Sets the current stream service settings (stream destination).

Note: Simple RTMP settings can be set with type `rtmp_custom` and the settings fields `server` and `key`.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`streamServiceType` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Type of stream service to apply e.g. `rtmp_common` or `rtmp_custom`
`streamServiceSettings` | `Object`{.datatype} | <i class="mdi mdi-check-bold"></i> | Settings to apply to the service

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
  "requestType": "SetStreamServiceSettings",
  "requestData": {
    "streamServiceType": "",
    "streamServiceSettings": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setstreamservicesettings)
{.btn-grid .my-5}