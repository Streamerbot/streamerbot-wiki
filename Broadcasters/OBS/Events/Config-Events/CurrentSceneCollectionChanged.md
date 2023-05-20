---
title: CurrentSceneCollectionChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:08:58.527Z
tags: 
editor: markdown
dateCreated: 2022-08-08T10:15:22.600Z
---

## Overview
The current scene collection has changed.

Note: If polling has been paused during `CurrentSceneCollectionChanging`, this is the cue to restart polling.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sceneCollectionName` | `String`{.datatype} | Name of the new scene collection

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--1"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#currentscenecollectionchanged)
{.btn-grid my-5}