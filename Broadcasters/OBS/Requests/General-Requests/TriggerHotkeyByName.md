---
title: TriggerHotkeyByName
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-07-30T01:23:03.524Z
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
`hotkeyName` | `String`{.datatype} | `True`{.datatype} | Name of the hotkey to trigger	

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--3"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Copy/Paste
```json
{
  "request-type": "TriggerHotkeyByName",
  "hotkeyName": ""
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this event***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#TriggerHotkeyByName)
{.btn-grid .my-5}