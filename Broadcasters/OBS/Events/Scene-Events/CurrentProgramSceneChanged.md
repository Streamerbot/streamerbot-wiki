---
title: CurrentProgramSceneChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:17:49.327Z
tags: 
editor: markdown
dateCreated: 2022-08-08T10:38:18.513Z
---

## Overview
The current program scene has changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sceneName` | `String`{.datatype} | Name of the scene that was switched to

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--1"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

## Example
```json
if ("obsEvent.sceneName" Equals "brb") do "disable channel points action" then "break"
if ("obsEvent.sceneName" Equals "game") do "enable channel points action" then "break"
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#currentprogramscenechanged)
{.btn-grid my-5}