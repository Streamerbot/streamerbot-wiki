---
title: SceneItemTransformChanged
description: OBS Studio Events Reference (Archive)
published: true
date: 2022-10-29T22:33:39.711Z
tags: 
editor: markdown
dateCreated: 2022-06-28T18:13:10.114Z
---

## Variables
| Variable | type | Description |
|---------:|:----:|:------------|
`obsEvent.event` | *string*{.datatype} | The OBS event in this case `SceneItemTransformChanged`
`obsEvent.item-id` | *integer*{.datatype} | Scene item ID
`obsEvent.item-name` | *string*{.datatype} | Name of the item in the scene
`obsEvent.scene-name` | *string*{.datatype} | Name of the scene
`obsEvent.transform.bounds.alignment` | *integer*{.datatype} | Alignment of the bounding box
`obsEvent.transform.bounds.type` | *string*{.datatype} | Type of bounding box, Can be `OBS_BOUNDS_STRETCH`, `OBS_BOUNDS_SCALE_INNER`, `OBS_BOUNDS_SCALE_OUTER`, `OBS_BOUNDS_SCALE_TO_WIDTH`, `OBS_BOUNDS_SCALE_TO_HEIGHT`, `OBS_BOUNDS_MAX_ONLY` or `OBS_BOUNDS_NONE`.
`obsEvent.transform.bounds.x` | *double*{.datatype} | Width of the bounding box
`obsEvent.transform.bounds.y` | *double*{.datatype} | Height of the bounding box
`obsEvent.transform.crop.bottom` | *integer*{.datatype} | The number of pixels cropped off the bottom of the source before scaling
`obsEvent.transform.crop.left` | *integer*{.datatype} | The number of pixels cropped off the left of the source before scaling
`obsEvent.transform.crop.right` | *integer*{.datatype} | The number of pixels cropped off the right of the source before scaling
`obsEvent.transform.crop.top` | *integer*{.datatype} | The number of pixels cropped off the top of the source before scaling
`obsEvent.transform.height` | *double*{.datatype} | Scene item height (base source height multiplied by the vertical scaling factor)
`obsEvent.transform.locked` | *boolean*{.datatype} | If the source's transform is locked
`obsEvent.transform.position.alignment` | *integer*{.datatype} | The point on the source that the item is manipulated from. The sum of 1=Left or 2=Right, and 4=Top or 8=Bottom, or omit to centre on that axis
`obsEvent.transform.position.x` | *double*{.datatype} | The x position of the source from the left
`obsEvent.transform.position.y` | *double*{.datatype} | The y position of the source from the top
`obsEvent.transform.rotation` | *double*{.datatype} | The clockwise rotation of the item in degrees around the point of alignment
`obsEvent.transform.scale.filter` | *string*{.datatype} | The scale filter of the source. Can be `OBS_SCALE_DISABLE`, `OBS_SCALE_POINT`, `OBS_SCALE_BICUBIC`, `OBS_SCALE_BILINEAR`, `OBS_SCALE_LANCZOS` or `OBS_SCALE_AREA`
`obsEvent.transform.scale.x` | *double*{.datatype} | The x-scale factor of the source
`obsEvent.transform.scale.y` | *double*{.datatype} | The y-scale factor of the source
`obsEvent.transform.sourceHeight` | *integer*{.datatype} | Base source (without scaling) of the source
`obsEvent.transform.sourceWidth` | *integer*{.datatype} | Base width (without scaling) of the source
`obsEvent.transform.visible` | *boolean*{.datatype} | If the source is visible
`obsEvent.transform.width` | *double*{.datatype} | Scene item width (base source width multiplied by the horizontal scaling factor)
`obsEvent.update-type` | *string*{.datatype} | The update type of the OBS event in this case `SceneItemTransformChanged`
`obsEvent._json` | *string*{.datatype} | Everything above in a json format

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Archive *Go Back***](/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sceneitemtransformchanged)
{.btn-grid my-5}