---
title: GetInputVolume
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-07-20T17:56:54.547Z
tags: 
editor: markdown
dateCreated: 2022-07-19T18:07:05.123Z
---

## Overview
Gets the current volume setting of an input.

## Request Fields
Name | Type | Description | Value Restrictions | Default Behavior |
----:|:----:|:------------|:------------------:|:----------------:|
`inputName` | *string*{.datatype} | Name of the input to get the volume of	 | *None*{.datatype} | *N/A*{.datatype}
## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsRaw.inputVolumeMul` | *integer*{.datatype} | Volume setting in mul
`obsRaw.inputVolumeDb` | *integer*{.datatype} | Volume setting in dB

## Data Fields
|:---|:---:
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/en/Broadcasters/OBS/Raw/v5Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this event***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#scenecreated)
{.btn-grid my-5}