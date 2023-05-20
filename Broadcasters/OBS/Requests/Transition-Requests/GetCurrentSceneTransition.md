---
title: GetCurrentSceneTransition
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:23:27.084Z
tags: 
editor: markdown
dateCreated: 2022-08-04T11:31:28.026Z
---

## Overview
Gets information about the current scene transition.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.transitionName` | `String`{.datatype} | Name of the transition
`obsRaw.transitionKind` | `String`{.datatype} | Kind of the transition
`obsRaw.transitionFixed` | `Boolean`{.datatype} | Whether the transition uses a fixed (unconfigurable) duration
`obsRaw.transitionDuration` | `Number`{.datatype} | Configured transition duration in milliseconds. `null` if transition is fixed
`obsRaw.transitionConfigurable` | `Boolean`{.datatype} | Whether the transition supports being configured
`obsRaw.transitionSettings` | `Object`{.datatype} | Object of settings for the transition. `null` if transition is not configurable

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--2"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "GetCurrentSceneTransition"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getcurrentscenetransition)
{.btn-grid .my-5}