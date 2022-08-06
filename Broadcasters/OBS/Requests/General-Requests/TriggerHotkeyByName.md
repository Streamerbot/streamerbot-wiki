---
title: TriggerHotkeyByName
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-06T13:06:22.012Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:22:43.800Z
---

## Overview
Triggers a hotkey using its name. See `GetHotkeyList`
- [**GetHotkeyList Request Reference**](/en/Broadcasters/OBS/Requests/General-Requests/GetHotkeyList)
{.btn-grid .my-5}

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`hotkeyName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the hotkey to trigger	

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--3"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Copy/Paste {.tabset}
### OBS raw
```json
{
  "request-type": "TriggerHotkeyByName",
  "hotkeyName": ""
}
```

### C# Method
```csharp
CPH.ObsSendRaw("TriggerHotkeyByName", "{'hotkeyName': ''}", 0);
```
##
---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#triggerhotkeybyname)
{.btn-grid .my-5}