---
title: SetVideoSettings
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:53.530Z
tags: 
editor: markdown
dateCreated: 2022-07-30T05:32:04.819Z
---

## Overview
Sets the current video settings.

Note: Fields must be specified in pairs. For example, you cannot set only `baseWidth` without needing to specify `baseHeight`.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`fpsNumerator` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Numerator of the fractional FPS value	 | `>= 1`{.datatype}
`fpsDenominator` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Denominator of the fractional FPS value	 | `>= 1	`{.datatype}
`baseWidth` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Width of the base (canvas) resolution in pixels	 | `>= 1, <= 4096	`{.datatype}
`baseHeight` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Height of the base (canvas) resolution in pixels	 | `>= 1, <= 4096	`{.datatype}
`outputWidth` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Width of the output resolution in pixels	 | `>= 1, <= 4096	`{.datatype}
`outputHeight` | `Number`{.datatype} | <i class="mdi mdi-close-thick"></i> | Height of the output resolution in pixels	 | `>= 1, <= 4096	`{.datatype}

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
  "requestType": "SetVideoSettings",
  "requestData": {
    "fpsNumerator": ,
    "fpsDenominator": ,
    "baseWidth": ,
    "baseHeight": ,
    "outputWidth": ,
    "outputHeight": 
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setvideosettings)
{.btn-grid .my-5}