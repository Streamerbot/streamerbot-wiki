---
title: InputShowStateChanged
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:15:08.708Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:18:20.265Z
---

## Overview
An input's show state has changed.

When an input is showing, it means it's being shown by the preview or a dialog.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputName` | `String`{.datatype} | Name of the input
`obsEvent.videoShowing` | `Boolean`{.datatype} | Whether the input is showing

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--3"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputshowstatechanged)
{.btn-grid my-5}