---
title: Pyramids
description: Execute an action when emote pyramids are completed
published: true
date: 2022-07-15T18:10:22.558Z
tags: settings, pyramids
editor: markdown
dateCreated: 2021-08-25T21:32:42.610Z
---

## Overview
Monitor chat for successful uninterrupted completion of an emote pyramid and execute an [Action](/Actions)

All [Twitch](https://twitch.tv), [BetterTwitchTV](https://betterttv.com/) and [FrankerFaceZ](https://www.frankerfacez.com/) emotes are supported.

![Pyramids Settings](/119623512-28e05500-be00-11eb-8340-5a02c1c94521.png =700x)

## Configuration
### Enabled
Toggle the enabled state of this feature.

### Minimum Width
Enter the minimum pyramid size before an event is triggered.

### Success Action
Select the action to execute

## Variables

The following variables are available to the excuted action:

| Value | Description |
|------:|:------------|
| `totalPyramids` | Total number of pyramids made by this user
| `pyramidEmote` | Name of the emote that completed the pyramid
| `pyramidWidth` | Width of the pyramid