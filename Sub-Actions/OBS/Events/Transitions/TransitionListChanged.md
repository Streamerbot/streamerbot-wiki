---
title: TransitionListChanged
description: The list of available transitions has been modified. Transitions have been added, removed, or renamed.
published: true
date: 2022-06-28T23:46:46.652Z
tags: 
editor: markdown
dateCreated: 2022-06-27T02:32:10.168Z
---

# TransitionListChanged

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `TransitionListChanged`
| `obsEvent.transitions[#].name` | The name of all transitions
| `obsEvent.update-type	` | The update type of the OBS event in this case `TransitionListChanged`
| `obsEvent._json` | Everything above in a json format
* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#transitionlistchanged)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}