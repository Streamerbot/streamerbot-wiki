---
title: Heartbeat
description: OBS Studio Events Reference
published: true
date: 2022-07-06T20:52:25.071Z
tags:
editor: markdown
dateCreated: 2022-06-27T20:47:31.411Z
---

# Heartbeat

## Variables

| Variable |  Type  | Description |
|---------:|:------:|:------------|
| `obsEvent.event` | *string*{.datatype} | The OBS event in this case `Heartbeat`
| `obsEvent.current-profile` | *string*{.datatype} | Current active profile
| `obsEvent.current-scene`| *string*{.datatype} | Current active scene
| `obsEvent.pulse` | *boolean*{.datatype} | Toggles between every JSON message as an "I am alive" indicator
| `obsEvent.recording` | *boolean*{.datatype} | Current recording state
| `obsEvent.stats` | *OBSStats*{.datatype} | OBS Stats
| `obsEvent.streaming` | *boolean*{.datatype} | Current streaming state
| `obsEvent.total-record-bytes` | *integer*{.datatype} | Total bytes recorded since the recording started
| `obsEvent.total-record-frames` | *integer*{.datatype} | Total frames recorded since the recording started
| `obsEvent.total-record-time` | *integer*{.datatype} | Total time (in seconds) since recording started
| `obsEvent.total-stream-bytes` | *integer*{.datatype} | Total bytes sent since the stream started
| `obsEvent.total-stream-frames` | *integer*{.datatype} | Total frames streamed since the stream started
| `obsEvent.total-stream-time` | *integer*{.datatype} | Total time (in seconds) since the stream started
| `obsEvent.update-type` | *string*{.datatype} | The update type of the OBS event in this case `Heartbeat`
| `obsEvent._json` | *string*{.datatype} | Everything above in a json format

---

- [<i class="mdi mdi-chevron-left"></i>**Back to the OBS events page*Go Back***](/en/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#heartbeat)
{.btn-grid my-5}
