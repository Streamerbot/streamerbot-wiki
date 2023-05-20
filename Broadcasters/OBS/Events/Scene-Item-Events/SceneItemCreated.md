---
title: SceneItemCreated
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:17:33.797Z
tags: 
editor: markdown
dateCreated: 2022-08-08T16:16:15.917Z
---

## Overview
A scene item has been created.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sceneName` | `String`{.datatype} | Name of the scene the item was added to
`obsEvent.sourceName` | `String`{.datatype} | Name of the underlying source (input/scene)
`obsEvent.sceneItemId` | `Number`{.datatype} | Numeric ID of the scene item
`obsEvent.sceneItemIndex` | `Number`{.datatype} | Index position of the item

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sceneitemcreated)
{.btn-grid my-5}