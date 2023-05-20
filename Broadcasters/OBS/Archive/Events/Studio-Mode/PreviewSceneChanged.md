---
title: PreviewSceneChanged
description: OBS Studio Events Reference (Archive)
published: true
date: 2022-10-29T22:39:04.904Z
tags: 
editor: markdown
dateCreated: 2022-06-28T19:12:25.206Z
---

## Variables
| Variable | Type | Description |
|---------:|:----:|:------------|
`obsEvent.event` | *string*{.datatype} | The OBS event in this case `PreviewSceneChanged`
`obsEvent.scene-name` | *string*{.datatype} | Name of the scene being previewed
`obsEvent.sources[#].alignment` | *integer*{.datatype} | 	The point on the source that the item is manipulated from. The sum of `1=Left` or `2=Right`, and `4=Top` or `8=Bottom`, or omit to `center` on that axis.
`obsEvent.sources[#].cx` | *integer*{.datatype} | The `cx` of this source
`obsEvent.sources[#].cy` | *integer*{.datatype} | The `cy` of this source
`obsEvent.sources[#].id` | *integer*{.datatype} | Scene item ID
`obsEvent.sources[#].locked` | *boolean*{.datatype} | Whether or not this source item is locked and can't be moved around
`obsEvent.sources[#].muted` | *boolean*{.datatype} | Whether or not this source Item is muted
`obsEvent.sources[#].name` | *string*{.datatype} | The name of this Scene Item
`obsEvent.sources[#].render` | *boolean*{.datatype} | Visibility of the scene item
`obsEvent.sources[#].source_cx` | *integer*{.datatype} | The `cy` position of this source
`obsEvent.sources[#].source_cy` |	*integer*{.datatype} | The `cy` position of this source
`obsEvent.sources[#].type` | *string*{.datatype} | Source type
`obsEvent.sources[#].volume` | *float*{.datatype} | Source volume
`obsEvent.sources[#].x` | *double*{.datatype} | The `x` position of this source
`obsEvent.sources[#].y` | *double*{.datatype} | The `y` position of this source
`obsEvent.update-type` | *string*{.datatype} | The update type of the OBS event in this case `PreviewSceneChanged`
`obsEvent._json` | *string*{.datatype} | Everything above in a json format

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Archive *Go Back***](/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#previewscenechanged)
{.btn-grid my-5}