---
title: RemoveProfile
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:27.251Z
tags: 
editor: markdown
dateCreated: 2022-07-30T02:12:44.541Z
---

## Overview
Removes a profile. If the current profile is chosen, it will change to a different profile first.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`profileName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the profile to remove

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
  "requestType": "RemoveProfile",
  "requestData": {
    "profileName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#removeprofile)
{.btn-grid .my-5}