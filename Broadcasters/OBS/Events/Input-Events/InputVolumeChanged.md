---
title: InputVolumeChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:15:13.076Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:21:50.821Z
---

## Overview
An input's volume level has changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputName` | `String`{.datatype} | Name of the input
`obsEvent.inputVolumeMul` | `Number`{.datatype} | New volume level in multimap
`obsEvent.inputVolumeDb` | `Number`{.datatype} | New volume level in dB

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputvolumechanged)
{.btn-grid my-5}