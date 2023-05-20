---
title: Follows Event
description: Twitch Events Reference
published: true
date: 2023-03-16T13:03:19.775Z
tags: 
editor: markdown
dateCreated: 2022-08-23T19:52:20.005Z
---

## Variables
Name | Description
----:|:------------
`user` | The user that followed the broadcaster
`userName` | The login name of the user that followed the broadcaster
`userId` | Unique user identifier
`userType` | pecifies which streaming service the triggering user is coming from *v0.1.8+*{.version-badge} <br> `twitch` or `youtube`
`isSubscribed` | Boolean value indicating the sender's subscription status <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
`eventSource` | specifies which streaming service the triggering event is coming from *v0.1.8+*{.version-badge} <br> `twitch` or `youtube`
{.vars-table}

> This will also include all the [Broadcaster Variables](/Variables/Broadcaster)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}