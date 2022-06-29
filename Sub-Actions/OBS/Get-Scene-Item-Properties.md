---
title: Get Scene Item Properties
description: 
published: true
date: 2022-06-28T02:16:56.197Z
tags: 
editor: markdown
dateCreated: 2022-06-28T01:36:29.236Z
---

# Get Scene Item Properties
With the Get Scene Item Properties sub-action you can get these properties below from a source or a group.

| Variable | Type |Description |
|---------:|:----:|:-----------|
| `props.bounds.alignment` | <kbd>integer</kbd> | Alignment of the bounding box
| `props.bounds.type` | <kbd>string</kbd> | Type of bounding box, Can be `OBS_BOUNDS_STRETCH`, `OBS_BOUNDS_SCALE_INNER`, `OBS_BOUNDS_SCALE_OUTER`, `OBS_BOUNDS_SCALE_TO_WIDTH`, `OBS_BOUNDS_SCALE_TO_HEIGHT`, `OBS_BOUNDS_MAX_ONLY` or `OBS_BOUNDS_NONE`.
| `props.bounds.x` | <kbd>double</kbd> | Width of the bounding box
| `props.bounds.y` | <kbd>double</kbd> | Height of the bounding box
| `props.crop.bottom` | <kbd>integer</kbd> | The number of pixels cropped off the bottom of the source before scaling
| `props.crop.left` | <kbd>integer</kbd> | The number of pixels cropped off the left of the source before scaling
| `props.crop.right` | <kbd>integer</kbd> | The number of pixels cropped off the right of the source before scaling
| `props.crop.top` | <kbd>integer</kbd> | The number of pixels cropped off the top of the source before scaling
| `props.height` | <kbd>double</kbd> | Scene item height (base source height multiplied by the vertical scaling factor)
| `props.itemId` | <kbd>integer</kbd> | Scene Item ID
| `props.locked` | <kbd>boolean</kbd> | If the source's transform is locked
| `props.message-id` | <kbd>string</kbd> | The id of the message
| `props.muted` | <kbd>boolean</kbd> | If the source is muted
| `props.name` | <kbd>string</kbd> | Scene Item name
| `props.position.alignment` | <kbd>integer</kbd> | The point on the source that the item is manipulated from. The sum of 1=Left or 2=Right, and 4=Top or 8=Bottom, or omit to centre on that axis
| `props.position.x` | <kbd>double</kbd> | The x position of the source from the left
| `props.position.y` | <kbd>double</kbd> | The y position of the source from the top
| `props.rotation` | <kbd>double</kbd> | The clockwise rotation of the item in degrees around the point of alignment
| `props.scale.filter` | <kbd>string</kbd> | The scale filter of the source. Can be `OBS_SCALE_DISABLE`, `OBS_SCALE_POINT`, `OBS_SCALE_BICUBIC`, `OBS_SCALE_BILINEAR`, `OBS_SCALE_LANCZOS` or `OBS_SCALE_AREA`
| `props.scale.x` | <kbd>double</kbd> | The x-scale factor of the source
| `props.scale.y` | <kbd>double</kbd> | The y-scale factor of the source
| `props.sourceHeight` | <kbd>integer</kbd> | Base source (without scaling) of the source
| `props.sourceWidth` | <kbd>integer</kbd> | Base width (without scaling) of the source
| `props.status` | <kbd>string</kbd> | The status of the sub-action
| `props.visible` | <kbd>boolean</kbd> | If the source is visible
| `props.width` | <kbd>double</kbd> | Scene item width (base source width multiplied by the horizontal scaling factor)
| `props.groupChildren[#].<one of these above>` | <kbd>mixed</kbd> | List of children (if this item is a group)
| `props._json` | <kbd>string</kbd> | Everything above in a json format