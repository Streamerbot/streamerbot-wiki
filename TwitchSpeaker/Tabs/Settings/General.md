---
title: UDP Interface
description: Run TwitchSpeaker stuff trough Streamer.bot
published: true
date: 2022-09-17T15:23:48.991Z
tags: 
editor: markdown
dateCreated: 2022-09-17T15:23:48.991Z
---

Port: `6669`

Payload Data (currently available):

```json
{ "command": "pause" }
{ "command": "resume" }
{ "command": "clear" }
{ "command": "off" }
{ "command": "disable" }
{ "command": "on" }
{ "command": "enable" }
{ "command": "stop" }
{ "command": "events", "value": "", "state": "on" }
{ "command": "events", "value": "", "state": "off" }
{ "command": "reg", "mode": "add", "user": "%user%", "id": "%userId%" }
{ "command": "reg", "mode": "del", "user": "%user%", "id": "%userId%" }
{ "command": "profile", "profile": "none" }
{ "command": "profile", "profile": "<profile name>" 
 ```
 
 You can also send text to be spoken

 ```json
{
  "command": "speak",
  "id": "<id>",
  "voice": "<voice alias>",
  "message": "<msg>"
}
```