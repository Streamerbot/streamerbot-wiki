---
title: InputAudioBalanceChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:14:16.307Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:23:17.656Z
---

## Overview
The audio balance value of an input has changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputName` | `String`{.datatype} | Name of the affected input
`obsEvent.inputAudioBalance` | `Number`{.datatype} | New audio balance value of the input

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputaudiobalancechanged)
{.btn-grid my-5}