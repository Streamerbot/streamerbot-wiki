---
title: GetInputAudioBalance
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-11T14:42:12.234Z
tags: 
editor: markdown
dateCreated: 2022-08-02T06:19:44.006Z
---

## Overview
Gets the audio balance of an input.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input to get the audio balance of

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.inputAudioBalance` | `Number`{.datatype} | Audio balance value from 0.0-1.0

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
  "request-type": "GetInputAudioBalance",
  "inputName": ""
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getinputaudiobalance)
{.btn-grid .my-5}