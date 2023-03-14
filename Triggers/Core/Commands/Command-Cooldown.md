---
title: Command Cooldown
description: Commands Triggers Reference
published: true
date: 2023-03-14T16:24:24.254Z
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
`msgId` | The unique message id for this message
`rawInput` | The message entered, if the command was a Starts With, this will be removed 
`rawInputEscaped` | The message escaped
`rawInputUrlEncoded` | The message URL encoded
`input#` | The # word of the message entered, spaces are delimiters and variable names are 0 indexed, so `input0` would give the first word, `input1` would give the second, and so on
`inputEscaped#` | The indexed word escaped
`inputUrlEncoded#` | The indexed word URL encoded
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`counter` | A running total of how many times a command has been run since application launch (if `Persisted` is checked, the total will be saved and reloaded at launch)
`userCounter` | A running total of how many times a command has been run by this chat user since application launch (if `UserPersisted` is checked, the total will be saved and reloaded at launch)
`cooldownLeft` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left
`globalCooldownLeft` | How many seconds are left for the global cooldown of the command
`userCooldownLeft` | How many seconds are left for the user cooldown of the command
{.vars-table}

> These variable include the [User Variables](/en/Variables/User-Variables) and the [Broadcaster Variables](/en/Variables/Broadcaster)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Commands Triggers Reference *Go Back***](/Triggers/Core/Commands)
{.btn-grid .my-5}