---
title: UDP Server
description: 
published: true
date: 2022-07-09T19:58:48.500Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:46.760Z
---

By enabling the UDP server, this will allow other applications on your computer to communicate with [Streamer.bot](https://streamer.bot).

One use for this, is communications with the Voice Attack plugin!

There currently is only 1 UDP message that the bot will listen to, and that is `DoAction`

The packet is as follows

```json
{
  "request": "DoAction",
  "action": {
    "id": "<guid>",
    "name": "<name>"
  }
}
```

You can specify either the GUID of the action, or the name and have it run.