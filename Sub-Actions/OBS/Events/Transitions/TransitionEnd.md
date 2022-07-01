---
title: TransitionEnd
description: A transition (other than "cut") has ended. Note: The `from-scene` field is not available in TransitionEnd.
published: true
date: 2022-06-28T23:47:50.109Z
tags: 
editor: markdown
dateCreated: 2022-06-27T02:42:12.078Z
---

# TransitionEnd

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `TransitionEnd`
| `obsEvent.duration` | The duration of the transition
| `obsEvent.name` | The name of the transition
| `obsEvent.to-scene` | On which scene the transition has ended
| `obsEvent.type	` | The type of transition that had began
| `obsEvent.update-type	` | The update type of the OBS event in this case `TransitionEnd`
| `obsEvent._json` | Everything above in a json format
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#transitionend)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}