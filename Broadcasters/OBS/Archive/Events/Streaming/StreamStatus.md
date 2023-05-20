---
title: StreamStatus
description: OBS Studio Events Reference (Archive)
published: true
date: 2022-10-29T22:38:15.368Z
tags: 
editor: markdown
dateCreated: 2022-06-27T13:51:20.162Z
---

## Variables

| Variable |  Type  | Description |
|---------:|:------:|:------------|
`obsEvent.event` | *string*{.datatype} | The OBS event in this case `StreamStatus`
`obsEvent.average-frame-time` | *double*{.datatype} | Average frame time (in milliseconds)
`obsEvent.bytes-per-sec` | *integer*{.datatype} | Amount of data per second (in bytes) transmitted by the stream encoder.
`obsEvent.cpu-usage`| *double*{.datatype} |  Current CPU usage (percentage)
`obsEvent.fps` | *double*{.datatype} | Current framerate
`obsEvent.free-disk-space` | *double*{.datatype} | Free recording disk space (in megabytes)

`obsEvent.kbits-per-sec` | *integer*{.datatype} | Amount of data per second (in kilobits) transmitted by the stream encoder.
`obsEvent.memory-usage` | *double*{.datatype} | Current RAM usage (in megabytes)
`obsEvent.num-dropped-frames` | *integer*{.datatype} | Number of frames dropped by the encoder since the stream started.
`obsEvent.num-total-frames` | *integer*{.datatype} | Total number of frames transmitted since the stream started
`obsEvent.output-skipped-frames` | *integer*{.datatype} | Number of frames skipped due to encoding lag
`obsEvent.output-total-frames` | *integer*{.datatype} | Numbers of frames outputted |
`obsEvent.preview-only` | *boolean*{.datatype} | Answer to preview only
`obsEvent.recording` | *boolean*{.datatype} | If you're recording
`obsEvent.recording-paused` | *boolean*{.datatype} | If your recording is paused
`obsEvent.render-missed-frames` | *integer*{.datatype} | Number of frames missed due to rendering lag
`obsEvent.render-total-frames` | *integer*{.datatype} | Number of frames rendered
`obsEvent.replay-buffer-active` | *boolean*{.datatype} | If your replay buffer is active
`obsEvent.strain` | *double*{.datatype} | Percentage of dropped frames
`obsEvent.stream-timecode` | *hh:mm:ss.ssss*{.datatype} | The stream timecode
`obsEvent.streaming` | *boolean*{.datatype} | A boolean answer to if you're streaming
`obsEvent.total-stream-time` | *integer*{.datatype} | The seconds that you have streamed
`obsEvent.update-type` | *string*{.datatype} | The update type of the OBS event in this case `StreamStopping`
`obsEvent._json` | *string*{.datatype} | Everything above in a json format

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Archive *Go Back***](/Broadcasters/OBS/Archive/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#StreamStatus)
{.btn-grid my-5}