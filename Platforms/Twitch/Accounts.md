---
title: Twitch Accounts
description: Set up your Broadcaster and Bot accounts for Streamer.bot to interact with Twitch
published: true
date: 2023-03-27T18:36:00.251Z
tags: twitch
editor: markdown
dateCreated: 2021-08-25T21:32:56.848Z
---

![connect_to_twitch_.png](/quick-start/connect_to_twitch_.png =800x)

## Broadcaster Account

If you want streamer.bot to be able to monitor chat and Twitch! events, a `Broadcaster` account must be defined

Press `Connect to Twitch` to automatically obtain a token 

`Auto Connect` will set streamer.bot to connect to twitch with the defined account on startup

`Auto Reconnect` instructs streamer.bot to attempt reconnection in the case of any network interruption to the platform

***

## Bot Account

By default any [sub-actions](/Sub-Actions#main) will be sent through the Broadcaster account. If you want a secondary account to send these actions / messages it can be defined here in the same way

***

## Refresh Categories

Use this to pull a current list of available Twitch categories. These can be used as variables in [sub-actions](/Sub-Actions#main) for example to change scene if category is changed to a specific game