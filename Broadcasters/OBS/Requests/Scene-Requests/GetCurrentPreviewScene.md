---
title: GetCurrentPreviewScene
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:14:20.267Z
tags: 
editor: markdown
dateCreated: 2022-07-31T12:54:36.906Z
---

## Overview
Gets the current preview scene.

Only available when studio mode is enabled.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.currentPreviewSceneName` | `String`{.datatype} | Current preview scene

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--1"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "GetCurrentPreviewScene"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getcurrentpreviewscene)
{.btn-grid .my-5}