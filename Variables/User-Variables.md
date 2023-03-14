---
title: User Variables
description: Variables reference
published: true
date: 2023-03-14T16:09:12.273Z
tags: 
editor: markdown
dateCreated: 2023-03-14T16:09:12.273Z
---

## Twitch
All user variables for Twitch{.subtitle}

Name | Description
----:|:------------
`user` | The user that followed the broadcaster
`userName` | The login name of the user that followed the broadcaster
`userId` | Unique user identifier
`userType` | pecifies which streaming service the triggering user is coming from <br> `twitch` or `youtube`
`isSubscribed` | Boolean value indicating the sender's subscription status <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
`userPreviousActive` | When the user was previously active
`eventSource` | specifies which streaming service the triggering event is coming from <br> `twitch` or `youtube`
{.vars-table}