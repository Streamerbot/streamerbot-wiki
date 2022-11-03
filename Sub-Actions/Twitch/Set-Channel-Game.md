---
title: Set Channel Game
description: Twitch Sub-Action Reference
published: true
date: 2022-11-03T19:19:45.167Z
tags: twitch, set game, change game, subactions
editor: markdown
dateCreated: 2021-11-24T04:02:44.267Z
---

## Overview
This sub-action can modify the current game category displayed on your Twitch channel.

![overview.png](/Sub-Actions/Twitch/set-channel-game/overview.png =400x)

## Configuration
### Source
Name | Description
----:|:------------
`String` | Manual text entry of game title - allows for usage of variables.
`Specific Game` | Select a game from a list of titles provided by Twitch

### Title
Used for variables, but also can use text.

## Variables
Name | Description
----:|:------------
`gameSuccess` | If the Sub-Action succeeded <br> `True`/`False`
`gameName` | The name of the game
`gameId` | The id of the game
`gameBoxArt` | The url of the game boxart, can be used with browser sources in your broadcaster.
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}