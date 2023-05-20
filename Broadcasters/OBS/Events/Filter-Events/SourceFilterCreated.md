---
title: SourceFilterCreated
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:09:42.819Z
tags: 
editor: markdown
dateCreated: 2022-08-08T15:59:15.093Z
---

## Overview
A filter has been added to a source.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.sourceName` | `String`{.datatype} | Name of the source the filter was added to
`obsEvent.filterName` | `String`{.datatype} | Name of the filter
`obsEvent.filterKind` | `String`{.datatype} | The kind of the filter
`obsEvent.filterIndex` | `Number`{.datatype} | Index position of the filter
`obsEvent.filterSettings` | `Object`{.datatype} | The settings configured to the filter when it was created
`obsEvent.defaultFilterSettings` | `Object`{.datatype} | The default settings for the filter

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#sourcefiltercreated)
{.btn-grid my-5}