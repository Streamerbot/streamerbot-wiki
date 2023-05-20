---
title: InputVolumeMeters
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:15:16.807Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:29:59.673Z
---

## Overview
A high-volume event providing volume levels of all active inputs every 50 milliseconds.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputs` | `Array<Object>`{.datatype} | Array of active inputs with their associated volume levels

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--4"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputvolumemeters)
{.btn-grid my-5}