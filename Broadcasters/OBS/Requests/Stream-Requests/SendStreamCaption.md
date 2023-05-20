---
title: SendStreamCaption
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:40:20.194Z
tags: 
editor: markdown
dateCreated: 2022-08-05T19:31:31.198Z
---

## Overview
Sends CEA-608 caption text over the stream output.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`captionText` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Caption text

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
  "requestType": "SendStreamCaption",
  "requestData": {
    "captionText": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sendstreamcaption)
{.btn-grid .my-5}