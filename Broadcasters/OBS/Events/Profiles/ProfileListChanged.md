---
title: ProfileListChanged
description: Triggered when a profile is created, added, renamed, or removed.
published: true
date: 2022-07-03T21:36:52.154Z
tags: 
editor: markdown
dateCreated: 2022-06-27T09:34:31.158Z
---

# ProfileListChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `ProfileListChanged`
| `obsEvent.profiles[#]` | The name of all your profiles
| `obsEvent.update-type	` | The update type of the OBS event in this case `ProfileListChanged`
| `obsEvent._json` | Everything above in a json format
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#profilelistchanged)
* [<= Back](/en/Broadcasters/OBS/)
{.links-list}