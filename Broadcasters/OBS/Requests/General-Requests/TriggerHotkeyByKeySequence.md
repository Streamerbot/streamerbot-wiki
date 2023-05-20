---
title: TriggerHotkeyByKeySequence
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:04:56.957Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:33:21.122Z
---

## Overview
Triggers a hotkey using a sequence of keys.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`keyId` | `String`{.datatype} | <i class="mdi mdi-close-thick"></i> | The OBS key ID to use. See [this](https://github.com/obsproject/obs-studio/blob/master/libobs/obs-hotkeys.h)
`keyModifiers` | `Object`{.datatype} | <i class="mdi mdi-close-thick"></i> | Object containing key modifiers to apply
`keyModifiers.shift` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Press Shift
`keyModifiers.control` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Press CTRL
`keyModifiers.alt` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Press ALT
`keyModifiers.command` | `Boolean`{.datatype} | <i class="mdi mdi-close-thick"></i> | Press CMD (Mac)

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
  "requestType": "TriggerHotkeyByKeySequence",
  "requestData": {
    "keyId": "",
    "keyModifiers.shift": ,
    "keyModifiers.control": ,
    "keyModifiers.alt": ,
    "keyModifiers.command": 
    "keyModifiers": {
      "": ""
    }
  }
}
```

### C# Method
```csharp
CPH.ObsSendRaw("TriggerHotkeyByKeySequence", "{'keyId': '', 'keyModifiers.shift': , 'keyModifiers.control': '', 'keyModifiers.alt': '', 'keyModifiers.command': '', 'keyModifiers': { '': '' }}", 0);
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#triggerhotkeybykeysequence)
{.btn-grid .my-5}