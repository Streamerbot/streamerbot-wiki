---
title: ProfileChanged
description: Triggered when switching to another profile or when renaming the current profile.
published: true
date: 2022-07-03T21:36:44.114Z
tags: 
editor: markdown
dateCreated: 2022-06-27T09:32:13.600Z
---

# ProfileChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `ProfileChanged`
| `obsEvent.profile` | The name of the profile it changed to
| `obsEvent.update-type	` | The update type of the OBS event in this case `ProfileChanged`
| `obsEvent._json` | Everything above in a json format
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#profilechanged)
* [<= Back](/en/Broadcasters/OBS/)
{.links-list}