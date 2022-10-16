---
title: Discord Basic Webhook
description: Discord Sub-Action Reference
published: false
date: 2022-10-16T19:52:24.393Z
tags: 
editor: markdown
dateCreated: 2022-10-16T17:08:15.813Z
---

## Overview
This is the first of a few new Discord specific sub-actions that will be added.  Up first is a friendlier way to post to a webhook you setup in your discord.  This one only allows for basic text posting.

Username, content, and image can contain variables and will be parsed.

Username, and image are also optional

![overview.png](/discord-basic-webhook-02.png =400x)

## Configuration
### Scene
A dropdown list of available scenes will populate for selection, but the scene name can also be entered manually.

### Source
If the selected OBS connection is currently connected, a dropdown list of available sources will populate for selection, otherwise the source name can be entered manually.

### Mode
Name | Description
----:|:------------
`Horizontal` | Inverts the X axis
`Vertical` | Inverts the Y axis
`Both` | Inverts both X and Y axes

---

- [<i class="mdi mdi-chevron-left"></i> **Discord Sub-Actions *Go Back***](/en/Sub-Actions/Discord)
{.btn-grid .my-5}