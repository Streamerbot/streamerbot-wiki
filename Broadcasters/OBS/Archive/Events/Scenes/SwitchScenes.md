---
title: SwitchScenes
description: OBS Studio Events Reference (Archive)
published: true
date: 2022-10-29T22:34:23.182Z
tags: 
editor: markdown
dateCreated: 2022-06-27T01:09:06.949Z
---

## Variables
Name | Description
----:|:------------
`obsEvent.event` | The OBS event in this case `SwitchScenes`
`obsEvent.scene-name` | The name of the scene it switches to
`obsEvent.sources[#]` | The settings of the sources in the scene you switched to
`obsEvent.update-type` | The update type of the OBS event in this case `SwitchScenes`
`obsEvent._json` | Everything above in a json format

## Example
When this event is linked to an action you can add this for example:
```csharp
if ("obsEvent.scene-name" Equals "brb") do "disable channel points action" then "break"
if ("obsEvent.scene-name" Equals "game") do "enable channel points action" then "break"
```
This will disable channel points on your "brb" scene and enable it on your "game" scene.

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Archive *Go Back***](/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#switchscenes)
{.btn-grid my-5}