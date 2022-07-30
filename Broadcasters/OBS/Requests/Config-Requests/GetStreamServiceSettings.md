---
title: GetStreamServiceSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-07-30T05:35:58.203Z
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

## Copy/Paste
```json
{
  "request-type": "GetStreamServiceSettings"
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getstreamservicesettings)
{.btn-grid .my-5}