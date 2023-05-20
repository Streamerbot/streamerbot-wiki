---
title: SceneItemLockStateChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:17:23.813Z
tags: 
editor: markdown
dateCreated: 2022-08-08T16:30:07.385Z
---

## Overview
A scene item's lock state has changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sceneName` | `String`{.datatype} | Name of the scene the item is in
`obsEvent.sceneItemId` | `Number`{.datatype} | Numeric ID of the scene item
`obsEvent.sceneItemLocked` | `Boolean`{.datatype} | Whether the scene item is locked

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sceneitemlockstatechanged)
{.btn-grid my-5}