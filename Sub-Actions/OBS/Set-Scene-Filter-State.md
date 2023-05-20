---
title: Set Scene Filter State
description: OBS Studio Sub-Action Reference
published: true
date: 2023-03-16T11:46:08.706Z
tags: 
editor: markdown
dateCreated: 2021-08-26T13:05:02.947Z
---

## Overview
Sets the enabled state of a specified filter on a source. Valid states are `Visible`, `Invisible` or `Toggle`

![overview.png](/Sub-Actions/OBS/set-scene-filter-state/overview.png =400x)

## Configuration
### Scene
If the selected OBS connection is currently connected, a dropdown list of available scenes will populate for selection, otherwise the scene name can be entered manually.

**NOTE** Scene names are case sensitive 

### Filter
If the selected OBS connection is currently connected, a dropdown list of available filters will populate for selection, otherwise the filter name can be entered manually.

**NOTE** Filter names are case sensitive

### State
Name | Description
----:|:------------
`Visible` | Sets the filter state on your scene to Visible
`Hidden` | Sets the filter state on your scene to Hidden
`Toggle` | Toggles the filter state on your scene between Visible and Hidden

---

- [<i class="mdi mdi-chevron-left"></i> **OBS Studio Sub-Actions *Go Back***](/Sub-Actions/OBS)
{.btn-grid .my-5}