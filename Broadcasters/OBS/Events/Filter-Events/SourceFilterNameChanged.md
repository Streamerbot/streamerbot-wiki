---
title: SourceFilterNameChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:10:21.702Z
tags: 
editor: markdown
dateCreated: 2022-08-08T16:07:20.398Z
---

## Overview
The name of a source filter has changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sourceName` | `String`{.datatype} | The source the filter is on
`obsEvent.oldFilterName` | `String`{.datatype} | Old name of the filter
`obsEvent.filterName` | `String`{.datatype} | New name of the filter

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sourcefilternamechanged)
{.btn-grid my-5}