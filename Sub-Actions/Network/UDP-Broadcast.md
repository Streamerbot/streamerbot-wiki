---
title: UDP Broadcast
description: Network Sub-Actions Reference
published: true
date: 2022-12-04T19:15:47.753Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:25.751Z
---

![image](/119697611-46d1a800-be48-11eb-8e09-696fe4060a58.png)

Broadcast a UDP payload on a specified port

***

## Example: Send text to Twitch Speaker to be read out

```json
{
  "command": "speak",
  "id": "1234",
  "voice": "BotVoice",
  "message": "It's %user%"
}
```

Replace `BotVoice` with the alias you want TwitchSpeaker to use, and `message` with the text you would like spoken