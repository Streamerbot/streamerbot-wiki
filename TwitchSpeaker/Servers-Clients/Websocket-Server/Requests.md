---
title: Websocket Server Requests
description: Control TwitchSpeaker with its internal Websocket Server!
published: true
date: 2023-02-26T11:42:55.442Z
tags: 
editor: markdown
dateCreated: 2023-01-19T19:43:54.205Z
---

----:|:------------
Port | `7580` | not recommended to change

![overview.png](/twitchspeaker/server-clients/websocket-server/overview.png =700x)

The settings for this are under `Settings` -> `WebSocket Server`, be sure to set auto start to enabled, so it'll run when you start TwitchSpeaker.

Request format
```json
{
    "request": "<command>",
    "id": "<id>",
}
```

Much like **Streamer.bot**, **TwitchSpeaker** follows the same request format, where `request` is the command you wish to perform, and `id` is some identifier or nonce.

## Speak
This is probably the command that will be used the most, this will make TwitchSpeaker speak the `message` you want, using the `voice` specified
```json
{
    "request": "Speak",
    "voice": "EventVoice",
    "message": "This is a test message",
    "badWordFilter": true/false, // optional
    "id": "<id>"
}
```

## Events
This will let you enable or disable events being spoken
```json
{
    "request": "Events",
    "state": "[on|off]"
    "id": "<id>",
}
```

## Mode
This will let you change the speaking mode, from everything, to a command
```json
{
    "request": "Mode",
    "mode": "[all|command]"
    "id": "<id>",
}
```

> If there are no commands already setup, switching to command, will return a failure response
{.is-info}

## Stop
```json
{
    "request": "Stop"
    "id": "<id>",
}
```

## Off
```json
{
    "request": "Off"
    "id": "<id>",
}
```

## On
```json
{
    "request": "On"
    "id": "<id>",
}
```

## Enable
```json
{
    "request": "Enable"
    "id": "<id>",
}
```

## Disable
```json
{
    "request": "Disable"
    "id": "<id>",
}
```

## Pause Queue
```json
{
    "request": "Pause"
    "id": "<id>",
}
```

## Resume Queue
```json
{
    "request": "Resume"
    "id": "<id>",
}
```

## Clear Queue
```json
{
    "request": "Clear"
    "id": "<id>",
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**TwitchSpeaker *Go Back***](/TwitchSpeaker)
{.btn-grid .my-5}
