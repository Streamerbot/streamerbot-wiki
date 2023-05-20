---
title: GetMediaInputStatus
description: OBS Studio Requests Reference (v5)
published: true
date: 2023-03-16T12:41:11.385Z
tags: 
editor: markdown
dateCreated: 2022-08-06T12:38:30.754Z
---

## Overview
Gets the status of a media input.

Media States:
* OBS_MEDIA_STATE_NONE
* OBS_MEDIA_STATE_PLAYING
* OBS_MEDIA_STATE_OPENING
* OBS_MEDIA_STATE_BUFFERING
* OBS_MEDIA_STATE_PAUSED
* OBS_MEDIA_STATE_STOPPED
* OBS_MEDIA_STATE_ENDED
* OBS_MEDIA_STATE_ERROR
{.links-list}

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`inputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the media input

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.mediaState` | `String`{.datatype} | State of the media input
`obsRaw.mediaDuration` | `Number`{.datatype} | Total duration of the playing media in milliseconds. `null` if not playing
`obsRaw.mediaCursor` | `Number`{.datatype} | Position of the cursor in milliseconds. `null` if not playing

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--2"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "GetMediaInputStatus",
  "requestData": {
      "inputName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getmediainputstatus)
{.btn-grid .my-5}