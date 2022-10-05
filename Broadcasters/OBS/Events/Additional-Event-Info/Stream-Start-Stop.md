---
title: Stream Start/Stop
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-05T11:54:38.373Z
tags: 
editor: markdown
dateCreated: 2022-10-05T11:43:52.981Z
---

## Overview
**Use the `StreamStateChanged` event**

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.outputActive` | `Boolean`{.datatype} | Whether the output is active
`obsEvent.outputState` | `String`{.datatype} | The specific state of the output

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

## Example

```json
if ("obsEvent.outputState" Equals "OBS_WEBSOCKET_OUTPUT_STARTED") do "disable channel points action" then "break"
if ("obsEvent.outputState" Equals "OBS_WEBSOCKET_OUTPUT_STOPPED") do "enable channel points action" then "break"
```
---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/en/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#streamstatechanged)
{.btn-grid my-5}