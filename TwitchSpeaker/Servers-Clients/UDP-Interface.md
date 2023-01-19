---
title: UDP Interface
description: Control TwitchSpeaker with Streamer.bot or other applications over a UDP connection
published: false
date: 2023-01-15T15:56:50.516Z
tags: 
editor: markdown
dateCreated: 2022-09-17T15:23:48.991Z
---

----:|:------------
Port | `6669` (the port can't be changed)

## speak
```json
{
  "command": "speak",
  "id": "<id>",
  "voice": "<voice alias>",
  "message": "<msg>"
}
```

## pause
```json
{
  "command": "pause"
}
```
  
## resume
```json
{
  "command": "resume"
}
```

## clear
```json
{
  "command": "clear"
}
```

## off
```json
{
  "command": "off"
}
```

## disable
```json
{
  "command": "disable"
}
```

## on
```json
{
  "command": "on"
}
```

## enable
```json
{
  "command": "enable"
}
```

## stop
```json
{
  "command": "stop"
}
```

## events (on)
```json
{
  "command": "events",
  "value": "<event name>",
  "state": "on"
}
```

## events (off)
```json
{
  "command": "events",
  "value": "<event name>",
  "state": "off"
}
```

## reg (add)
```json
{
  "command": "reg",
  "mode": "add",
  "user": "%user%",
  "id": "%userId%"
}
```

## reg (del)
```json
{
  "command": "reg",
  "mode": "del",
  "user": "%user%",
  "id": "%userId%"
}
```

## profile
```json
{
  "command": "profile",
  "profile": "<profile name>"
}
```

## profile (none)
```json
{
  "command": "profile", 
  "profile": "none"
}
```

## set (sticky)
Added in v0.0.49
```json
{
  "command": "set",
  "method": "sticky",
  "value": true
}
{
  "command": "set",
  "method": "sticky",
  "value": false
}
```

## set (nickname)
Added in v0.0.49
```json
{
  "command": "set",
  "method": "nickname",
  "username": "%user%",
  "nickname": "somestring"
}
```

## assign (last)
Added in v0.0.49
```json
{
  "command": "assign",
  "method": "last",
  "username": "%user%"
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**TwitchSpeaker *Go Back***](/TwitchSpeaker)
{.btn-grid .my-5}
