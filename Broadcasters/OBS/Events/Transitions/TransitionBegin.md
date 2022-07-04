---
title: TransitionBegin
description: A transition (other than "cut") has begun.
published: true
date: 2022-07-03T21:48:12.993Z
tags: 
editor: markdown
dateCreated: 2022-06-27T02:40:20.421Z
---

# TransitionBegin

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `TransitionBegin`
| `obsEvent.duration` | The duration of the transition
| `obsEvent.from-scene` | On which scene the transition had started
| `obsEvent.name` | The name of the transition
| `obsEvent.to-scene` | On which scene the transition has ended
| `obsEvent.type	` | The type of transition that had began
| `obsEvent.update-type	` | The update type of the OBS event in this case `TransitionBegin`
| `obsEvent._json` | Everything above in a json format
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#transitionbegin)
* [<= Back](/en/Integrations/OBS/OBS-Events)
{.links-list}