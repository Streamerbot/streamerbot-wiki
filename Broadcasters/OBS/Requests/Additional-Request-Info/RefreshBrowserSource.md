---
title: RefreshBrowserSource
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:52:45.836Z
tags: 
editor: markdown
dateCreated: 2022-09-01T12:19:55.650Z
---

## Overview
Refresh a browser source with the [PressInputPropertiesButton](/Broadcasters/OBS/Requests/Input-Requests/PressInputPropertiesButton) request

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the input
`propertyName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the button property to press

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
  "requestType": "PressInputPropertiesButton",
  "requestData": {
    "inputName": "",
    "propertyName": "refreshnocache"
  }
}
```
### C# Method
```csharp
CPH.ObsSendRaw("PressInputPropertiesButton", "{'inputName': '', 'propertyName': 'refreshnocache'}", 0);
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#pressinputpropertiesbutton)
{.btn-grid .my-5}