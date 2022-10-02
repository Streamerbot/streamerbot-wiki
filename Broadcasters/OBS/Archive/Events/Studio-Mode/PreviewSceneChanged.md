---
title: PreviewSceneChanged
description: OBS Studio Events Reference
published: true
date: 2022-07-18T16:11:10.962Z
tags: 
editor: markdown
dateCreated: 2022-06-28T19:12:25.206Z
---

# PreviewSceneChanged

## Variables

| Variable | Type | Description |
|---------:|:----:|:------------|
`obsEvent.event` | <kbd>string</kbd> | The OBS event in this case `PreviewSceneChanged`
`obsEvent.scene-name` | <kbd>string</kbd> | Name of the scene being previewed
`obsEvent.sources[#].alignment` | <kbd>integer</kbd> | 	The point on the source that the item is manipulated from. The sum of `1=Left` or `2=Right`, and `4=Top` or `8=Bottom`, or omit to `center` on that axis.
`obsEvent.sources[#].cx` | <kbd>integer</kbd> | The `cx` of this source
`obsEvent.sources[#].cy` | <kbd>integer</kbd> | The `cy` of this source
`obsEvent.sources[#].id` | <kbd>integer</kbd> | Scene item ID
`obsEvent.sources[#].locked` | <kbd>boolean</kbd> | Whether or not this source item is locked and can't be moved around
`obsEvent.sources[#].muted` | <kbd>boolean</kbd> | Whether or not this source Item is muted
`obsEvent.sources[#].name` | <kbd>string</kbd> | The name of this Scene Item
`obsEvent.sources[#].render` | <kbd>boolean</kbd> | Visibility of the scene item
`obsEvent.sources[#].source_cx` | <kbd>integer</kbd> | The `cy` position of this source
`obsEvent.sources[#].source_cy` |	<kbd>integer</kbd> | The `cy` position of this source
`obsEvent.sources[#].type` | <kbd>string</kbd> | Source type
`obsEvent.sources[#].volume` | <kbd>float</kbd> | Source volume
`obsEvent.sources[#].x` | <kbd>double</kbd> | The `x` position of this source
`obsEvent.sources[#].y` | <kbd>double</kbd> | The `y` position of this source
`obsEvent.update-type` | <kbd>string</kbd> | The update type of the OBS event in this case `PreviewSceneChanged`
`obsEvent._json` | <kbd>string</kbd> | Everything above in a json format

---

- [<i class="mdi mdi-chevron-left"></i>**Back to the OBS events page*Go Back***](/en/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#previewscenechanged)
{.btn-grid my-5}
