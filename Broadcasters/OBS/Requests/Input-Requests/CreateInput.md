---
title: CreateInput
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:15:51.614Z
tags: 
editor: markdown
dateCreated: 2022-08-01T03:14:16.992Z
---

## Overview
Creates a new input, adding it as a scene item to the specified scene.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`sceneName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the scene to add the input to as a scene item
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the new input to created
`inputKind` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | The kind of input to be created
`inputSettings` | `Object`{.datatype} | <i class="mdi mdi-close-thick"></i> | Settings object to initialize the input with
`sceneItemEnabled` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Whether to set the created scene item to enabled or disabled

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.sceneItemId` | `Number`{.datatype} | ID of the newly created scene item

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--3"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "CreateInput",
  "requestData": {
    "sceneName": "",
    "inputName": "",
    "inputKind": "",
    "sceneItemEnabled": ,
    "inputSettings": {
      "": ""
    }
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#createinput)
{.btn-grid .my-5}