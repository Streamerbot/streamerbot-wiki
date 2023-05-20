---
title: InputAudioMonitorTypeChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:14:37.675Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:28:40.905Z
---

## Overview
The monitor type of an input has changed.

Available types are:
* OBS_MONITORING_TYPE_NONE
* OBS_MONITORING_TYPE_MONITOR_ONLY
* OBS_MONITORING_TYPE_MONITOR_AND_OUTPUT
{.links-list}

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputName` | `String`{.datatype} | Name of the input
`obsEvent.monitorType` | `String`{.datatype} | New monitor type of the input

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputaudiomonitortypechanged)
{.btn-grid my-5}