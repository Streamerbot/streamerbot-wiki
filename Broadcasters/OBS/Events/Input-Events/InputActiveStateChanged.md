---
title: InputActiveStateChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:14:12.950Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:16:33.184Z
---

## Overview
An input's active state has changed.

When an input is active, it means it's being shown by the program feed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputName` | `String`{.datatype} | Name of the input
`obsEvent.videoActive` | `Boolean`{.datatype} | Whether the input is active

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputactivestatechanged)
{.btn-grid my-5}