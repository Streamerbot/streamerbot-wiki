---
title: TransitionBegin
description: OBS Studio Events Reference
published: true
date: 2022-07-06T20:55:56.449Z
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
* [<= Back](/en/Broadcasters/OBS/Events)
{.links-list}