---
title: GetOutputList
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-07T09:32:00.347Z
tags: 
editor: markdown
dateCreated: 2022-08-05T14:15:24.931Z
---

## Overview
Gets the list of available outputs.

> The Variables aren't in the official OBS WebSocket Documentation so it can be wrong, the variables came from the OBS WebSocket source code. The Type and Description aren't available
{.is-danger}

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.outputName` | 
`obsRaw.outputKind` | 
`obsRaw.outputWidth` | 
`obsRaw.outputHeight` | 
`obsRaw.outputActive` | 

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
  "request-type": "GetOutputList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getoutputlist)
{.btn-grid .my-5}