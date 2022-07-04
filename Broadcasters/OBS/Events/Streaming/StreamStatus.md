---
title: StreamStatus
description: Emitted every 2 seconds when stream is active.
published: true
date: 2022-07-03T21:46:32.398Z
tags: 
editor: markdown
dateCreated: 2022-06-27T13:51:20.162Z
---

# StreamStatus

## Variables

| Variable |  Type  | Description |
|---------:|:------:|:------------|
| `obsEvent.event` | <kbd>string</kbd> | The OBS event in this case `StreamStatus`  
| `obsEvent.average-frame-time` | <kbd>double</kbd> | Average frame time (in milliseconds)
| `obsEvent.bytes-per-sec` | <kbd>integer</kbd> | Amount of data per second (in bytes) transmitted by the stream encoder.
| `obsEvent.cpu-usage`| <kbd>double</kbd> |  Current CPU usage (percentage)
| `obsEvent.fps` | <kbd>double</kbd> | Current framerate
| `obsEvent.free-disk-space` | <kbd>double</kbd> | Free recording disk space (in megabytes)

| `obsEvent.kbits-per-sec` | <kbd>integer</kbd> | Amount of data per second (in kilobits) transmitted by the stream encoder.
| `obsEvent.memory-usage` | <kbd>double</kbd> | Current RAM usage (in megabytes)
| `obsEvent.num-dropped-frames` | <kbd>integer</kbd> | Number of frames dropped by the encoder since the stream started.
| `obsEvent.num-total-frames` | <kbd>integer</kbd> | Total number of frames transmitted since the stream started
| `obsEvent.output-skipped-frames` | <kbd>integer</kbd> | Number of frames skipped due to encoding lag
| `obsEvent.output-total-frames` | <kbd>integer</kbd> | Numbers of frames outputted | 
| `obsEvent.preview-only` | <kbd>boolean</kbd> | Answer to preview only
| `obsEvent.recording` | <kbd>boolean</kbd> | If you're recording
| `obsEvent.recording-paused` | <kbd>boolean</kbd> | If your recording is paused
| `obsEvent.render-missed-frames` | <kbd>integer</kbd> | Number of frames missed due to rendering lag
| `obsEvent.render-total-frames` | <kbd>integer</kbd> | Number of frames rendered
| `obsEvent.replay-buffer-active` | <kbd>boolean</kbd> | If your replay buffer is active
| `obsEvent.strain` | <kbd>double</kbd> | Percentage of dropped frames
| `obsEvent.stream-timecode` | <kbd>hh:mm:ss.ssss</kbd> | The stream timecode
| `obsEvent.streaming` | <kbd>boolean</kbd> | A boolean answer to if you're streaming
| `obsEvent.total-stream-time` | <kbd>integer</kbd> | The seconds that you have streamed
| `obsEvent.update-type` | <kbd>string</kbd> | The update type of the OBS event in this case `StreamStopping`
| `obsEvent._json` | <kbd>string</kbd> | Everything above in a json format 

* [Official OBS websocket documentation about this](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#StreamStatus)
* [<= Back](/en/Broadcasters/OBS/
{.links-list}