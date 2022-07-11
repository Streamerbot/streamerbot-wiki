---
title: Set Channel Game
description: Twitch Sub-Action Reference
published: true
date: 2022-07-11T23:26:26.579Z
tags: twitch, set game, change game, subactions
editor: markdown
dateCreated: 2021-11-24T04:02:44.267Z
---

## Overview

This sub-action can modify the current game category displayed on your Twitch channel.

![set_channel_game_-select_game_.png](/set_channel_game_-select_game_.png)

> **WARNING**
> Moderator privileges are required on your bot account for this sub-action to work!
{.is-warning}

## Configuration

### Source

| Value | Description |
|------:|:------------|
`String` | Manual text entry of game title - allows for usage of [variables](/en/Variables). <br/> For Example, using the `%rawInput%` variable from a `!setgame` command used by your moderators.
`Specific Game` | Select a game from a list of titles provided by Twitch


## Variables
No variables generated.

<section class="btn-grid my-5">
    
  [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/en/Sub-Actions/Twitch)
  
  [<i class="mdi mdi-twitch text--twitch"></i>**Set Channel Title *Up Next***](/en/Sub-Actions/Twitch/Set-Title)
  
</section>