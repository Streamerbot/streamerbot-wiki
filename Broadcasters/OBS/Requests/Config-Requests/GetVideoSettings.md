---
title: GetVideoSettings
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-12T12:01:25.813Z
tags: 
editor: markdown
dateCreated: 2022-07-30T05:26:03.156Z
---

## Overview
Gets the current video settings.

Note: To get the true FPS value, divide the FPS numerator by the FPS denominator e.g. `60000/1001`

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.fpsNumerator` | `Number`{.datatype} | Numerator of the fractional FPS value
`obsRaw.fpsDenominator` | `Number`{.datatype} | Denominator of the fractional FPS value
`obsRaw.baseWidth` | `Number`{.datatype} | Width of the base (canvas) resolution in pixels
`obsRaw.baseHeight` | `Number`{.datatype} | Height of the base (canvas) resolution in pixels
`obsRaw.outputWidth	` | `Number`{.datatype} | Width of the output resolution in pixels
`obsRaw.outputHeight` | `Number`{.datatype} | Height of the output resolution in pixels

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--2"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json

```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getvideosettings)
{.btn-grid .my-5}