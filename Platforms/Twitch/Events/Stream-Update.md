---
title: Stream Update
description: Twitch Events Reference
published: true
date: 2023-03-16T13:00:58.960Z
tags: twitch, events
editor: markdown
dateCreated: 2022-07-08T04:16:50.386Z
---

## Overview
The Stream Update event is triggered any time your stream category or title changes.

## Variables
The following variables are available from this event:

Name | Description
----:|:------------
`status` | Current stream title
`gameUpdate` | Boolean value denoting whether the game category has changed <br> `True / False`
`statusUpdate` | Boolean value denoting whether the stream title has changed <br> `True / False`
`gameId` | Stream's current game category ID
`gameName` | Stream's current game name
`oldStatus` | Previous stream status
`oldGameId` | Previous game category ID
`oldGameName` | Previous game name
`gameBoxArt` | URL for current game boxart image *v0.1.5+*{.version-badge}
`oldGameBoxArt` | URL for previous game boxart image *v0.1.5+*{.version-badge}
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}