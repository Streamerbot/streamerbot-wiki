---
title: GetRecordStatus
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:40:28.897Z
tags: 
editor: markdown
dateCreated: 2022-08-05T19:35:36.890Z
---

## Overview
Gets the status of the record output.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.outputActive` | `Boolean`{.datatype} | Whether the output is active
`obsRaw.ouputPaused` | `Boolean`{.datatype} | Whether the output is paused
`obsRaw.outputTimecode` | `String`{.datatype} | Current formatted timecode string for the output
`obsRaw.outputDuration` | `Number`{.datatype} | Current duration in milliseconds for the output
`obsRaw.outputBytes` | `Number`{.datatype} | Number of bytes sent by the output

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
  "requestType": "GetRecordStatus"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getrecordstatus)
{.btn-grid .my-5}