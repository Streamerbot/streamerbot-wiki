---
title: PressInputPropertiesButton
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:18:39.231Z
tags: 
editor: markdown
dateCreated: 2022-08-04T10:34:43.848Z
---

## Overview
Presses a button in the properties of an input.

Note: Use this in cases where there is a button in the properties of an input that cannot be accessed in any other way. For example, browser sources, where there is a refresh button.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input
`propertyName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the button property to press

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--4"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "PressInputPropertiesButton",
  "requestData": {
    "inputName": "",
    "propertyName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#pressinputpropertiesbutton)
{.btn-grid .my-5}