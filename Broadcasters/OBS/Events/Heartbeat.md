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
| `obsEvent.event` | <kbd>string</kbd> | The OBS event in this case `Heartbeat`
| `obsEvent.current-profile` | <kbd>string</kbd> | Current active profile
| `obsEvent.current-scene`| <kbd>string</kbd> | Current active scene
| `obsEvent.pulse` | <kbd>boolean</kbd> | Toggles between every JSON message as an "I am alive" indicator
| `obsEvent.recording` | <kbd>boolean</kbd> | Current recording state
| `obsEvent.stats` | <kbd>OBSStats</kbd> | OBS Stats
| `obsEvent.streaming` | <kbd>boolean</kbd> | Current streaming state
| `obsEvent.total-record-bytes` | <kbd>integer</kbd> | Total bytes recorded since the recording started
| `obsEvent.total-record-frames` | <kbd>integer</kbd> | Total frames recorded since the recording started
| `obsEvent.total-record-time` | <kbd>integer</kbd> | Total time (in seconds) since recording started
| `obsEvent.total-stream-bytes` | <kbd>integer</kbd> | Total bytes sent since the stream started
| `obsEvent.total-stream-frames` | <kbd>integer</kbd> | Total frames streamed since the stream started
| `obsEvent.total-stream-time` | <kbd>integer</kbd> | Total time (in seconds) since the stream started
| `obsEvent.update-type` | <kbd>string</kbd> | The update type of the OBS event in this case `Heartbeat`
| `obsEvent._json` | <kbd>string</kbd> | Everything above in a json format

- [<i class="mdi mdi-chevron-left"></i>**Back to the OBS events page*Go Back***](/en/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#heartbeat)
{.btn-grid my-5}
