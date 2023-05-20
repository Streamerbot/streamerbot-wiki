---
title: SetCurrentProfile
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:16.735Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:58:02.450Z
---

## Overview
Switches to a profile.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`profileName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the profile to switch to

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
  "requestType": "SetCurrentProfile",
  "requestData": {
    "profileName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#setcurrentprofile)
{.btn-grid .my-5}