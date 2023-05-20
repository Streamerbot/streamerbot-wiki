---
title: SourceAudioMixersChanged
description: OBS Studio Events Reference (Archive)
published: true
date: 2022-10-29T22:23:55.066Z
tags: 
editor: markdown
dateCreated: 2022-06-28T15:35:36.718Z
---

## Variables
Name | Description
----:|:------------
`obsEvent.event` | The OBS event in this case `SourceAudioMixersChanged`
`obsEvent.hexMixersValue` | Raw mixer flags (little-endian, one bit per mixer) as an hexadecimal value
`obsEvent.mixers[#].enabled` | Routing status
`obsEvent.mixers[#].id`	| Mixer number
`obsEvent.sourceName` | Source name
`obsEvent.update-type` | The update type of the OBS event in this case `SourceAudioMixersChanged`
`obsEvent._json` | Everything above in a json format

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Archive *Go Back***](/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sourceaudiomixerschanged)
{.btn-grid my-5}
