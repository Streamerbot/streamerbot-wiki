---
title: Command Cooldown
description: Commands Triggers Reference
published: true
date: 2023-03-14T16:25:44.418Z
tags: 
editor: markdown
dateCreated: 2023-03-14T16:24:24.254Z
---

## Overview
The HotKey Press trigger is used for when you press a key on one of your keyboards.

For a detailed guide on how Commands work in Streamer.bot see [this page](/Commands).

## Configuration
### Commands
Select a command from the Commands tab.

## Variables
Name | Description
----:|:------------
`command` | The command that was used
`commandId` | The ID of the command
`commandSource` | The command source <br> `twitch`/`youtube`
`commandType` | The type of the command e.g. `message`
`cooldownLeft` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left
`globalCooldownLeft` | How many seconds are left for the global cooldown of the command
`userCooldownLeft` | How many seconds are left for the user cooldown of the command
{.vars-table}

> These variable include the [User Variables](/en/Variables/User-Variables) and the [Broadcaster Variables](/en/Variables/Broadcaster)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Commands Triggers Reference *Go Back***](/Triggers/Core/Commands)
{.btn-grid .my-5}