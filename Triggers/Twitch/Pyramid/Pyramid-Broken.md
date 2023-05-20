---
title: Pyramid Broken
description: Twitch Triggers Reference
published: true
date: 2023-04-27T15:23:33.081Z
tags: 
editor: markdown
dateCreated: 2023-04-27T15:22:36.285Z
---

## Overview
This triggers when a pyramid gets destroyed in Twitch chat.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `Chat Client`
Added in: | *N/A*{.version-badge}

## Variables
This includes the [User](/Variables/User-Variables) variables.

Name | Description
----:|:------------
`totalPyramidsBroken` | The total amount of pyramids the user has broken.
`pyramidWidth` | The total amount of pyramid layers.
`pyramidEmote` | The emote that was used in the pyramid.
`pyramidOwnerId` | The user id of the person who intiated the pyramid.
`pyramidOwnerUsername` | The user name of the person who intiated the pyramid.
`pyramidOwnerDisplayName` | The user display of the person who intiated the pyramid.
{.vars-table}

> The user variables are for the person who destroyed the pyramid.
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}