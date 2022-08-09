---
title: Get Scene Item Properties
description: 
published: true
date: 2022-08-09T17:48:10.093Z
tags: 
editor: markdown
dateCreated: 2022-06-28T01:36:29.236Z
---

| Variable | Type |Description |
|---------:|:----:|:-----------|
| `props.bounds.alignment` | `integer`{.datatype} | Alignment of the bounding box
| `props.bounds.type` | `string`{.datatype} | Type of bounding box, Can be `OBS_BOUNDS_STRETCH`, `OBS_BOUNDS_SCALE_INNER`, `OBS_BOUNDS_SCALE_OUTER`, `OBS_BOUNDS_SCALE_TO_WIDTH`, `OBS_BOUNDS_SCALE_TO_HEIGHT`, `OBS_BOUNDS_MAX_ONLY` or `OBS_BOUNDS_NONE`.
| `props.bounds.x` | `double`{.datatype} | Width of the bounding box
| `props.bounds.y` | `double`{.datatype} | Height of the bounding box
| `props.crop.bottom` | `integer`{.datatype} | The number of pixels cropped off the bottom of the source before scaling
| `props.crop.left` | `integer`{.datatype} | The number of pixels cropped off the left of the source before scaling
| `props.crop.right` | `integer`{.datatype} | The number of pixels cropped off the right of the source before scaling
| `props.crop.top` | `integer`{.datatype} | The number of pixels cropped off the top of the source before scaling
| `props.height` | `double`{.datatype} | Scene item height (base source height multiplied by the vertical scaling factor)
| `props.itemId` | `integer`{.datatype} | Scene Item ID
| `props.locked` | `boolean`{.datatype} | If the source's transform is locked
| `props.message-id` | `string`{.datatype} | The id of the message
| `props.muted` | `boolean`{.datatype} | If the source is muted
| `props.name` | `string`{.datatype} | Scene Item name
| `props.position.alignment` | `integer`{.datatype} | The point on the source that the item is manipulated from. The sum of 1=Left or 2=Right, and 4=Top or 8=Bottom, or omit to centre on that axis
| `props.position.x` | `double`{.datatype} | The x position of the source from the left
| `props.position.y` | `double`{.datatype} | The y position of the source from the top
| `props.rotation` | `double`{.datatype} | The clockwise rotation of the item in degrees around the point of alignment
| `props.scale.filter` | `string`{.datatype} | The scale filter of the source. Can be `OBS_SCALE_DISABLE`, `OBS_SCALE_POINT`, `OBS_SCALE_BICUBIC`, `OBS_SCALE_BILINEAR`, `OBS_SCALE_LANCZOS` or `OBS_SCALE_AREA`
| `props.scale.x` | `double`{.datatype} | The x-scale factor of the source
| `props.scale.y` | `double`{.datatype} | The y-scale factor of the source
| `props.sourceHeight` | `integer`{.datatype} | Base source (without scaling) of the source
| `props.sourceWidth` | `integer`{.datatype} | Base width (without scaling) of the source
| `props.status` | `string`{.datatype} | The status of the sub-action
| `props.visible` | `boolean`{.datatype} | If the source is visible
| `props.width` | `double`{.datatype} | Scene item width (base source width multiplied by the horizontal scaling factor)
| `props.groupChildren[#].<one of these above>` | `mixed`{.datatype} | List of children (if this item is a group)
| `props._json` | `string`{.datatype} | Everything above in a json format