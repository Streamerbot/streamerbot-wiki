---
title: RecordingStopping
description: A request to stop recording has been issued.
published: true
date: 2022-07-03T21:38:15.347Z
tags: 
editor: markdown
dateCreated: 2022-06-27T18:03:51.600Z
---

# RecordingStopping

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `RecordingStopping`
| `obsEvent.rec-timecode` | The length of the recording formatted like hh:mm:ss.sss |
| `obsEvent.recordingFilename` | Absolute path to the file of the current recording. |
| `obsEvent.update-type` | The update type of the OBS event in this case `RecordingStopping`
| `obsEvent._json` | Everything above in a json format

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#recordingstopping)
* [<= Back](/en/Broadcasters/OBS/
{.links-list}