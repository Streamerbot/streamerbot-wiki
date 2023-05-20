---
title: InputCreated
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:14:50.000Z
tags: 
editor: markdown
dateCreated: 2022-08-08T11:12:12.294Z
---

## Overview
An input has been created.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.inputName` | `String`{.datatype} | Name of the input
`obsEvent.inputKind` | `String`{.datatype} | The kind of the input
`obsEvent.unversionedInputKind` | `String`{.datatype} | The unversioned kind of input (aka no `_v2` stuff)
`obsEvent.inputSettings` | `Object`{.datatype} | The settings configured to the input when it was created
`obsEvent.defaultInputSettings` | `Object`{.datatype} | The default settings for the input

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#inputcreated)
{.btn-grid my-5}