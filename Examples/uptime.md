---
title: Uptime
description: Display uptime in Streamer.bot.
published: true
date: 2022-07-09T19:57:47.677Z
tags: 
editor: markdown
dateCreated: 2022-04-25T01:53:55.843Z
---

# Uptime

## Description

Display uptime through Streamer.bot.

## Installation

Copy the text from the code box below into the `Import` box in Streamer.bot to add these to your action library:

```
TlM0RR+LCAAAAAAABACVU8tO4zAU3SPxD1YlNhFuHnXzYFchNCyYjoRgMRqxuLFv2kipk3FsCkL8O7E9VdPHLFjFPuf63HuOnY/LC0Imr6j6upWTGxJfO0DCBofd5Ll7qoeVB4Hroagf8D92T8iH/wxULWx1hkVZCSwo58AoYyhoURUJTQTL5iKZJ1nGvZY79NegsV2kaZo9ihLKBq2eVgb3+LmRHLFSreksM8Kg2cJ7/2ispQqafqSjQIp2s3BeTlneSm6UQqlPuRP/Bxm4EqMaO8la666/CUOBHLp6usFQb2vN16Hp9DB8GAS/fz0/3t4vlsu7hyDYD+5EXkHVNoPlP8f+0FGRT5zNinxIGGieFjPKyjmnRVqmFGfAeFrmwHJxdHCL9Wpt3UXT6JDR753tF0dRdkjsEj64KD+FFPhmtfbo5/X/wtH4ZvtOvPvl4uddEJA19KRElKTXCmFTyxWpWkWuvOmro+E7hRUO1yMWnLfGXVJ8Lpd8DqKoIKUx5IIyLjJa5lFF4xSrNMpEUqbw/Vy+m0o8SmW3fDl+Tz+sjHtUL+Nn2DTQ9ShGrCedkK/0P9CO/PwCSA64ncsDAAA=
```

## Configuration

Double click on the `subaction` `Fetch URL` and change `**YOURCHANNEL**` to your Twitch Channel name.

![uptime-fetch-url.png](/examples/uptime-fetch-url.png)

Double click on the `subaction` `Message` and change `**YOURCHANNEL**` to `%broadcastUser%`.

![message-uptime.png](/examples/message-uptime.png)

Create a `Command` called `!uptime` tied to the `Action` `UpTime` and set to `Exact`.

![command-uptime.png](/examples/command-uptime.png)