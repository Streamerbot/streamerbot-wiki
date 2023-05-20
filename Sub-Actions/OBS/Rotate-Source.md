---
title: Rotate Source
description: OBS Studio Sub-Action Reference
published: true
date: 2023-03-16T11:42:33.289Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:33:46.410Z
---

## Overview
Sets the rotation tranformation angle of a source to the specified angle
**NOTE** Rotation occours around the alignment position defined in OBS itself. By default this is the top left corner of the source not the center

![overview.png](/Sub-Actions/OBS/rotate-source/overview.png =400x)

## Configuration
### Scene
If the selected OBS connection is currently connected, a dropdown list of available scenes will populate for selection, otherwise the scene name can be entered manually.

**NOTE** Scene names are case sensitive 

### Source
If the selected OBS connection is currently connected, a dropdown list of available sources will populate for selection, otherwise the source name can be entered manually.

**NOTE** Source names are case sensitive

### Alignment
Reports the currently configured alignment position.

### Rotation
By default this is an `Absolute` angle with 0 being normal rotation, valid range -360 -> +360, however as tranform is instant values outside -180 -> +180 will be visually the same. Negative values rotate the source counter-clockwise.

`Additive` option will make the rotation relative to its current transform rather than overwriting

---

- [<i class="mdi mdi-chevron-left"></i> **OBS Studio *Go Back***](/Sub-Actions/OBS)
{.btn-grid .my-5}