---
title: CurrentSceneCollectionChanging
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:09:03.262Z
tags: 
editor: markdown
dateCreated: 2022-08-08T10:14:03.526Z
---

## Overview
The current scene collection has begun changing.

Note: We recommend using this event to trigger a pause of all polling requests, as performing any requests during a scene collection change is considered undefined behavior and can cause crashes!

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sceneCollectionName` | `String`{.datatype} | Name of the current scene collection

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--1"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#currentscenecollectionchanging)
{.btn-grid my-5}