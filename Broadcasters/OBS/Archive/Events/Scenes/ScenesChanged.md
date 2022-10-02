---
title: ScenesChanged
description: OBS Studio Events Reference
published: true
date: 2022-07-18T16:09:48.746Z
tags: 
editor: markdown
dateCreated: 2022-06-27T01:53:30.436Z
---

# ScenesChanged

## Variables

Name | Description | Notes
----:|:------------|:------
`obsEvent.event` | The OBS event in this case `ScenesChanged`
`obsEvent.scene-name` | The name of the scene it switches to
`obsEvent.scenes[#]` | The settings of all your OBS scenes | (**Note** this gives a lot of variables, it can be in the thousands)
`obsEvent.update-type	` | The update type of the OBS event in this case `ScenesChanged`
`obsEvent._json` | Everything above in a json format | (**Note** This variable can be empty, because the variable other wise would have been too long)

---

- [<i class="mdi mdi-chevron-left"></i>**Back to the OBS events page*Go Back***](/en/Broadcasters/OBS/Archive/Events)
---

- [<i class="mdi mdi-chevron-left"></i>**Back to the OBS events page*Go Back***](/en/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sceneschanged)
{.btn-grid my-5}
