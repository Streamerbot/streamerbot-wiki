---
title: SetInputName
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:16:06.925Z
tags: 
editor: markdown
dateCreated: 2022-08-01T03:20:18.286Z
---

## Overview
Sets the name of an input (rename).

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Current input name	
`newInputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | New name for the input	

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
  "requestType": "SetInputName",
  "requestData": {
    "inputName": "",
    "newInputName": ""
  }
}
```

### C# Method
```csharp
CPH.ObsSendRaw("SetInputName", "{'inputName': '', 'newInputName': ''}", 0);
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setinputname)
{.btn-grid .my-5}