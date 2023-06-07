---
title: Stream Update
description: Twitch Triggers Reference
published: true
date: 2023-06-07T14:28:39.894Z
tags: 
editor: markdown
dateCreated: 2023-06-07T14:28:39.894Z
---

## Overview
This triggers when the title or the description changes on your stream. 

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `PubSub`
Added in: | *v0.0.30*{.version-badge}

## Variables
Name | Description
----:|:------------
`status` | The current stream title
`gameUpdate` | Boolean value denoting whether the game category has changed <br> `True / False`
`statusUpdate` | Boolean value denoting whether the stream title has changed <br> `True / False`
`gameId` | The current game id
`gameName` | The current game name
`oldStatus` | The old stream status
`oldGameId` | The old game id
`oldGameName` | The previous game name
`gameBoxArt` | The URL for current game boxart image
`oldGameBoxArt` | The URL for previous game boxart image
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}