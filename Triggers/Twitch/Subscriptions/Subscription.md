---
title: Subscription
description: Twitch Triggers Reference
published: true
date: 2023-06-07T08:42:31.771Z
tags: 
editor: markdown
dateCreated: 2023-06-07T08:40:56.500Z
---

## Overview
This triggers when you get a subscription.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `Chat Client`
Added in: | *N/A*{.version-badge}

## Variables
This includes the [User](/Variables/User-Variables) variables.

Name | Description
----:|:------------
`tier` | Subscription tier <br> `prime`, `tier 1`. `tier 2`, `tier 3`
`rawInput` | The message entered
`rawInputEscaped` | The message escaped
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`color` | User's color (if they have chosen one or a random one if not)
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}