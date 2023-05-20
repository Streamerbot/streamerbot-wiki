---
title: SceneTransitionVideoEnded
description: OBS Studio Events Reference (v5)
published: true
date: 2023-03-16T12:52:11.528Z
tags: 
editor: markdown
dateCreated: 2022-08-08T15:46:51.838Z
---

## Overview
A scene transition's video has completed fully.

Useful for stinger transitions to tell when the video actually ends. [SceneTransitionEnded](/Broadcasters/OBS/Events/Transition-Events/SceneTransitionEnded) only signifies the cut point, not the completion of transition playback.

Note: Appears to be called by every transition, regardless of relevance.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.transitionName` | `String`{.datatype} | Scene transition name

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#scenetransitionvideoended)
{.btn-grid my-5}