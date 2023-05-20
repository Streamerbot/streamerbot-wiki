---
title: StreamStateChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:17:58.167Z
tags: 
editor: markdown
dateCreated: 2022-08-08T18:05:38.373Z
---

## Overview
The state of the stream output has changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.outputActive` | `Boolean`{.datatype} | Whether the output is active
`obsEvent.outputState` | `String`{.datatype} | The specific state of the output

### obsEvent.outputState
Name | Description
----:|:------------
`OBS_WEBSOCKET_OUTPUT_STOPPING` | You have send the request to stop streaming
`OBS_WEBSOCKET_OUTPUT_STOPPED` | You have successfully stopped streaming
`OBS_WEBSOCKET_OUTPUT_STARTING` | You have send the request to start streaming
`OBS_WEBSOCKET_OUTPUT_STARTED` | You have successfully started streaming

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

## Example
```json
if ("obsEvent.outputState" Equals "OBS_WEBSOCKET_OUTPUT_STARTED") do "<start streaming action>" then "break"
if ("obsEvent.outputState" Equals "OBS_WEBSOCKET_OUTPUT_STOPPED") do "<stop streaming action>" then "break"
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#streamstatechanged)
{.btn-grid my-5}