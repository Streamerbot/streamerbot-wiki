---
title: Pulsoid
description: 
published: true
date: 2022-06-26T23:25:24.681Z
tags: 
editor: markdown
dateCreated: 2022-06-01T04:14:54.410Z
---

# Pulsoid

No longer an extension written in C#, Pulsoid support is now a native part of **Streamer.bot**

![pulsoid-integration.png](/pulsoid-integration.png)

After connecting your account, by clicking **Connect to Pulsoid** and following the prompts in your browser.  You can assign an action to the `Heart Rate` Event, and when Pulsoid broadcasts a heart beat, this action will run.

> When Pulsoid is broadcasting your heart rate, this event can fire once every second, so be sure whatever action you use runs fast enough so it won't cause a backlog in an action queue.  It is also recommended that whatever action you are running be placed in a blocking queue.
{.is-warning}

## Available Variables

| Variable | Description |
|   ---:|-------------|
| `measuredAt` | Time the measurement was taken |
| `heartRate` | Heart Rate value |