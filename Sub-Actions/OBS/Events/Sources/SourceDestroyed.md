---
title: SourceDestroyed
description: A source has been destroyed/removed. A source can be an input, a scene or a transition.
published: true
date: 2022-07-06T21:22:00.329Z
tags: 
editor: markdown
dateCreated: 2022-07-06T21:21:56.978Z
---

# SourceDestroyed

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SourceDestroyed`
| `obsEvent.sourceKind` | Source kind
| `obsEvent.sourceName` | Source name
| `obsEvent.sourceType` | Source type <span style="color:blue">Can be `input`, `scene`, `transition` or `filter`.</span>
| `obsEvent.update-type` | The update type of the OBS event in this case `SourceDestroyed`
| `obsEvent._json` | Everything above in a JSON format

* [Official OBS WebSocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sourcedestroyed)
* [<= Back](/en/Integrations/OBS/Events)
{.links-list}