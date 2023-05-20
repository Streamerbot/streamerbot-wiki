---
title: Get Scene Item Properties
description: OBS Studio Sub-Action Reference
published: true
date: 2023-03-16T11:45:51.368Z
tags: 
editor: markdown
dateCreated: 2022-06-28T01:36:29.236Z
---

## Overview

![overview.png](/Sub-Actions/OBS/get-scene-item-properties/overview.png =400x)

## Variables
Name | Type | Description
----:|:----:|:------------
`props.bounds.alignment` | `Number`{.datatype} | Alignment of the bounding box
`props.bounds.type` | `String`{.datatype} | Type of bounding box, Can be `OBS_BOUNDS_STRETCH`, `OBS_BOUNDS_SCALE_INNER`, `OBS_BOUNDS_SCALE_OUTER`, `OBS_BOUNDS_SCALE_TO_WIDTH`, `OBS_BOUNDS_SCALE_TO_HEIGHT`, `OBS_BOUNDS_MAX_ONLY` or `OBS_BOUNDS_NONE`.
`props.bounds.x` | `Number`{.datatype} | Width of the bounding box
`props.bounds.y` | `Number`{.datatype} | Height of the bounding box
`props.crop.bottom` | `Number`{.datatype} | The number of pixels cropped off the bottom of the source before scaling
`props.crop.left` | `Number`{.datatype} | The number of pixels cropped off the left of the source before scaling
`props.crop.right` | `Number`{.datatype} | The number of pixels cropped off the right of the source before scaling
`props.crop.top` | `Number`{.datatype} | The number of pixels cropped off the top of the source before scaling
`props.height` | `Number`{.datatype} | Scene item height (base source height multiplied by the vertical scaling factor)
`props.itemId` | `Number`{.datatype} | Scene Item ID
`props.locked` | `Boolean`{.datatype} | If the source's transform is locked
`props.message-id` | `String`{.datatype} | The id of the message
`props.muted` | `Boolean`{.datatype} | If the source is muted
`props.name` | `String`{.datatype} | Scene Item name
`props.position.alignment` | `Number`{.datatype} | The point on the source that the item is manipulated from. The sum of 1=Left or 2=Right, and 4=Top or 8=Bottom, or omit to centre on that axis
`props.position.x` | `Number`{.datatype} | The x position of the source from the left
`props.position.y` | `Number`{.datatype} | The y position of the source from the top
`props.rotation` | `Number`{.datatype} | The clockwise rotation of the item in degrees around the point of alignment
`props.scale.filter` | `String`{.datatype} | The scale filter of the source. Can be `OBS_SCALE_DISABLE`, `OBS_SCALE_POINT`, `OBS_SCALE_BICUBIC`, `OBS_SCALE_BILINEAR`, `OBS_SCALE_LANCZOS` or `OBS_SCALE_AREA`
`props.scale.x` | `Number`{.datatype} | The x-scale factor of the source
`props.scale.y` | `Number`{.datatype} | The y-scale factor of the source
`props.sourceHeight` | `Number`{.datatype} | Base source (without scaling) of the source
`props.sourceWidth` | `Number`{.datatype} | Base width (without scaling) of the source
`props.status` | `String`{.datatype} | The status of the sub-action
`props.visible` | `Boolean`{.datatype} | If the source is visible
`props.width` | `Number`{.datatype} | Scene item width (base source width multiplied by the horizontal scaling factor)
`props.groupChildren[#].<one of these above>` | `Mixed`{.datatype} | List of children (if this item is a group)
`props._json` | `String`{.datatype} | Everything above in a json format

---

- [<i class="mdi mdi-chevron-left"></i> **OBS Studio Sub-Actions *Go Back***](/Sub-Actions/OBS)
{.btn-grid .my-5}