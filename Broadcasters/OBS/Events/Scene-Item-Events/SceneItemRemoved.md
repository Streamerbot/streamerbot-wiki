---
title: SceneItemRemoved
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:17:20.716Z
tags: 
editor: markdown
dateCreated: 2022-08-08T16:19:00.469Z
---

## Overview
A scene item has been removed.

This event is not emitted when the scene the item is in is removed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sceneName` | `String`{.datatype} | Name of the scene the item was removed from
`obsEvent.sourceName` | `String`{.datatype} | Name of the underlying source (input/scene)
`obsEvent.sceneItemId` | `Number`{.datatype} | Numeric ID of the scene item

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sceneitemremoved)
{.btn-grid my-5}