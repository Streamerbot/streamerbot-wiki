---
title: Set Source Mute State
description: 
published: true
date: 2023-03-16T11:44:13.839Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:06.029Z
---

## Overview
Valid states are `Muted` `Not Muted` or `Toggle`

Sets a defined source to be muted or unmuted on the stream broadcast

![overview.png](/Sub-Actions/OBS/set-source-mute-state/overview.png =400x)

## Configuration
### Scene
If the selected OBS connection is currently connected, a dropdown list of available scenes will populate for selection, otherwise the scene name can be entered manually.

**NOTE** Scene names are case sensitive 

### Source
If the selected OBS connection is currently connected, a dropdown list of available sources will populate for selection, otherwise the source name can be entered manually.

**NOTE** Source names are case sensitive

### State
Name | Description
----:|:------------
`Muted` | Sets the mute state on your source to Muted
`Not Muted` | Sets the mute state on your source to Not Muted
`Toggle` | Toggles the mute state on your source between Muted and Not Muted

---

- [<i class="mdi mdi-chevron-left"></i> **OBS Studio Sub-Actions *Go Back***](/Sub-Actions/OBS)
{.btn-grid .my-5}