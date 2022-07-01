---
title: SceneItemTransformChanged
description: A scene item's transform has been changed.
published: true
date: 2022-06-29T02:41:12.060Z
tags: 
editor: markdown
dateCreated: 2022-06-28T18:13:10.114Z
---

# SceneItemTransformChanged

## Variables

| Variable | type | Description |
|---------:|:----:|:------------|
| `obsEvent.event` | <kbd>string</kbd> | The OBS event in this case `SceneItemTransformChanged`
| `obsEvent.item-id` | <kbd>integer</kbd> | Scene item ID
| `obsEvent.item-name` | <kbd>string</kbd> | Name of the item in the scene
| `obsEvent.scene-name` | <kbd>string</kbd> | Name of the scene
| `obsEvent.transform.bounds.alignment` | <kbd>integer</kbd> | Alignment of the bounding box
| `obsEvent.transform.bounds.type` | <kbd>string</kbd> | Type of bounding box, Can be `OBS_BOUNDS_STRETCH`, `OBS_BOUNDS_SCALE_INNER`, `OBS_BOUNDS_SCALE_OUTER`, `OBS_BOUNDS_SCALE_TO_WIDTH`, `OBS_BOUNDS_SCALE_TO_HEIGHT`, `OBS_BOUNDS_MAX_ONLY` or `OBS_BOUNDS_NONE`.
| `obsEvent.transform.bounds.x` | <kbd>double</kbd> | Width of the bounding box
| `obsEvent.transform.bounds.y` | <kbd>double</kbd> | Height of the bounding box
| `obsEvent.transform.crop.bottom` | <kbd>integer</kbd> | The number of pixels cropped off the bottom of the source before scaling
| `obsEvent.transform.crop.left` | <kbd>integer</kbd> | The number of pixels cropped off the left of the source before scaling
| `obsEvent.transform.crop.right` | <kbd>integer</kbd> | The number of pixels cropped off the right of the source before scaling
| `obsEvent.transform.crop.top` | <kbd>integer</kbd> | The number of pixels cropped off the top of the source before scaling
| `obsEvent.transform.height` | <kbd>double</kbd> | Scene item height (base source height multiplied by the vertical scaling factor)
| `obsEvent.transform.locked` | <kbd>boolean</kbd> | If the source's transform is locked
| `obsEvent.transform.position.alignment` | <kbd>integer</kbd> | The point on the source that the item is manipulated from. The sum of 1=Left or 2=Right, and 4=Top or 8=Bottom, or omit to centre on that axis
| `obsEvent.transform.position.x` | <kbd>double</kbd> | The x position of the source from the left
| `obsEvent.transform.position.y` | <kbd>double</kbd> | The y position of the source from the top
| `obsEvent.transform.rotation` | <kbd>double</kbd> | The clockwise rotation of the item in degrees around the point of alignment
| `obsEvent.transform.scale.filter` | <kbd>string</kbd> | The scale filter of the source. Can be `OBS_SCALE_DISABLE`, `OBS_SCALE_POINT`, `OBS_SCALE_BICUBIC`, `OBS_SCALE_BILINEAR`, `OBS_SCALE_LANCZOS` or `OBS_SCALE_AREA`
| `obsEvent.transform.scale.x` | <kbd>double</kbd> | The x-scale factor of the source
| `obsEvent.transform.scale.y` | <kbd>double</kbd> | The y-scale factor of the source
| `obsEvent.transform.sourceHeight` | <kbd>integer</kbd> | Base source (without scaling) of the source
| `obsEvent.transform.sourceWidth` | <kbd>integer</kbd> | Base width (without scaling) of the source
| `obsEvent.transform.visible` | <kbd>boolean</kbd> | If the source is visible
| `obsEvent.transform.width` | <kbd>double</kbd> | Scene item width (base source width multiplied by the horizontal scaling factor)
| `obsEvent.update-type` | <kbd>string</kbd> | The update type of the OBS event in this case `SceneItemTransformChanged`
| `obsEvent._json` | <kbd>string</kbd> | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sceneitemtransformchanged)
* [<= Back](/en/Integrations/OBS/OBS-Events)
{.links-list}