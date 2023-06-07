---
title: Gift Bomb
description: Twitch Triggers Reference
published: true
date: 2023-06-07T08:48:46.927Z
tags: 
editor: markdown
dateCreated: 2023-06-07T08:48:46.927Z
---

## Overview
This triggers when someone does a gift bomb.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `Chat Client`
Added in: | *N/A*{.version-badge}

## Variables
This includes the [User](/Variables/User-Variables) variables.

Name | Description
----:|:------------
`gifts` | Number of subscriptions in this gift bomb
`totalGifts` | Total number of subscriptions this user has gifted
`fromGiftBomb` | Boolean value if sub came from a gift bomb <br>  `True`/`False` 
`anonymous` | Boolean value indicating the gift was anonymous <br> `True`/`False` 
`tier` | The subscriptions tier <br> `tier 1`. `tier 2`, `tier 3`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}