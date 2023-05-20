---
title: InputAudioTracksChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:14:46.065Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:26:16.792Z
---

## Overview
The audio tracks of an input have changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputName` | `String`{.datatype} | Name of the input
`obsEvent.inputAudioTracks` | `Object`{.datatype} | Object of audio tracks along with their associated enable states

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputaudiotrackschanged)
{.btn-grid my-5}