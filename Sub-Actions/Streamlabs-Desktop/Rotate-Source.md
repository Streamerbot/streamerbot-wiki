---
title: Rotate Source
description: 
published: true
date: 2021-08-28T02:04:51.357Z
tags: 
editor: markdown
dateCreated: 2021-08-26T12:55:40.989Z
---

Sets the rotation tranformation angle of a source to the specified angle

**NOTE** Rotation occours around the top left corner of the source not the center

![Rotate Source](/119569573-d292f800-bda6-11eb-8d36-bd9148d963b8.png)

### Connection

Any SLOBS connections you have configured in the [SLOBS](/SLOBS) tab will be listed to choose from

### Scene

If the selected SLOBS connection is currently connected, a dropdown list of available scenes will populate for selection, otherwise the scene name can be entered manually.

**NOTE** Scene names are case sensitive 

### Source

If the selected SLOBS connection is currently connected, a dropdown list of available sources will populate for selection, otherwise the source name can be entered manually.

**NOTE** Source names are case sensitive

### Alignment

Reports the currently configured alignment position.

### Rotation

By default this is an `Absolute` angle with 0 being normal rotation, valid range -360 -> +360, however as tranform is instant values outside -180 -> +180 will be visually the same. Negative values rotate the source counter-clockwise.

`Additive` option will make the rotation relative to its current transform rather than overwriting