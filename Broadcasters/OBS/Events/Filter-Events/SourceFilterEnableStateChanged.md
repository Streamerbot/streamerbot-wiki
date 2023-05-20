---
title: SourceFilterEnableStateChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:10:10.481Z
tags: 
editor: markdown
dateCreated: 2022-08-08T16:09:22.980Z
---

## Overview
A source filter's enable state has changed.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sourceName` | `String`{.datatype} | Name of the source the filter is on
`obsEvent.filterName` | `String`{.datatype} | Name of the filter
`obsEvent.filterEnabled` | `Boolean`{.datatype} | Whether the filter is enabled

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sourcefilterenablestatechanged)
{.btn-grid my-5}