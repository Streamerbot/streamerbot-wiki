---
title: ScreenshotSaved
description: OBS Studio Events Reference (v5)
published: true
date: 2023-01-10T05:27:40.519Z
tags: 
editor: markdown
dateCreated: 2023-01-10T05:27:38.734Z
---

## Overview
A screenshot has been saved.

**Note:** Triggered for the screenshot feature available in `Settings -> Hotkeys -> Screenshot Output` ONLY. Applications using `Get/SaveSourceScreenshot` should implement a `CustomEvent` if this kind of inter-client communication is desired.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.savedScreenshotPath` | `String`{.datatype} | Path of the saved image file

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--2"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.1.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#screenshotsaved)
{.btn-grid my-5}