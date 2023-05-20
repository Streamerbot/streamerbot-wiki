---
title: GetSourceScreenshot
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:08:12.837Z
tags: 
editor: markdown
dateCreated: 2022-07-30T23:14:02.903Z
---

## Overview
Gets a Base64-encoded screenshot of a source.

The `imageWidth` and `imageHeight` parameters are treated as "scale to inner", meaning the smallest ratio will be used and the aspect ratio of the original resolution is kept. If `imageWidth` and `imageHeight` are not specified, the compressed image will use the full resolution of the source.

**Compatible with inputs and scenes.**

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sourceName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the source to take a screenshot of
`imageFormat` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Image compression format to use. Use `GetVersion` to get compatible image formats
`imageWidth` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Width to scale the screenshot to | `>= 8, <= 4096`{.datatype}
`imageHeight` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Height to scale the screenshot to	 | `>= 8, <= 4096`{.datatype}
`imageCompressionQuality` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Compression quality to use. 0 for high compression, 100 for uncompressed. -1 to use "default" (whatever that means, idk) | `>= -1, <= 100`{.datatype}

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.imageData` | `String`{.datatype} | Base64-encoded screenshot

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
  "requestType": "GetSourceScreenshot",
  "requestData": {
    "sourceName": "",
    "imageFormat": "",
    "imageWidth": ,
    "imageHeight": ,
    "imageCompressionQuality": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getsourcescreenshot)
{.btn-grid .my-5}