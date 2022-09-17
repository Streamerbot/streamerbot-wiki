---
title: UDP Interface
description: Run TwitchSpeaker stuff trough Streamer.bot
published: true
date: 2022-09-17T15:55:56.571Z
tags: 
editor: markdown
dateCreated: 2022-09-17T15:23:48.991Z
---

Port: `6669`

Payload Data (currently available):

## pause
```json
{
  "command": "pause"
}
```

***

## resume
```json
{
  "command": "resume"
}
```

***

## clear
```json
{
  "command": "clear"
}
```

***

## off
```json
{
  "command": "off"
}
```

***

## disable
```json
{
  "command": "disable"
}
```

***

## on
```json
{
  "command": "on"
}
```

***

## enable
```json
{
  "command": "enable"
}
```

***

## stop
```json
{
  "command": "stop"
}
```

***

## events (on)
```json
{
  "command": "events",
  "value": "",
  "state": "on"
}
```

**Example:**
```json
{
  "command": "events",
  "value": "<event name>",
  "state": "on"
}
```

***

## events (off)
```json
{
  "command": "events",
  "value": "",
  "state": "off"
}
```

**Example:**
```json
{
  "command": "events",
  "value": "<event name>",
  "state": "off"
}
```

***

## reg (add)
```json
{
  "command": "reg",
  "mode": "add",
  "user": "",
  "id": ""
}
```

**Example:**
```json
{
  "command": "reg",
  "mode": "add",
  "user": "%user%",
  "id": "%userId%"
}
```

***

## reg (del)
```json
{
  "command": "reg",
  "mode": "del",
  "user": "",
  "id": ""
}
```

**Example:**
```json
{
  "command": "reg",
  "mode": "del",
  "user": "%user%",
  "id": "%userId%"
}
```

***

## Profile
```json
{
  "command": "profile",
  "profile": ""
}
```

**Example:**
```json
{
  "command": "profile",
  "profile": "<profile name>"
}
```

***

## Profile (none)
```json
{
  "command": "profile", 
  "profile": "none"
}
```

**Example:**
```json
{
  "command": "profile",
  "profile": "none"
}
```

***

You can also send text to be spoken

 ```json
{
  "command": "speak",
  "id": "<id>",
  "voice": "<voice alias>",
  "message": "<msg>"
}
```