---
title: GetProfileList
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:07:14.000Z
tags: 
editor: markdown
dateCreated: 2022-07-30T01:51:54.223Z
---

## Overview
Gets an array of all profiles

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.currentProfileName` | `String`{.datatype} | The name of the current profile
`obsRaw.profiles` | `Array<String>`{.datatype} | Array of all available profiles

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
  "requestType": "GetProfileList"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getprofilelist)
{.btn-grid .my-5}