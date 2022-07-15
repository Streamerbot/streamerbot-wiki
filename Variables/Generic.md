---
title: Generic
description: 
published: true
date: 2022-07-04T17:12:08.851Z
tags: 
editor: markdown
dateCreated: 2022-06-30T19:57:33.363Z
---

# Generic

Generic variables are available to most event sources, so consider these the minimum you can use. Other sources will expand on these with variables specific to that event or sub-action

Variable | Description | Notes
---------:|------------
`user` | User's Display Name | (**Note** this is case sensitive when using in a comparison)
`userType` | Specifies which streaming service the triggering user is coming from| *v0.1.8+*{.version-badge}  `twitch`,`youtube`
`userName` | User's Login Name |(**Note** this is all lowercase when using in a comparison for Twitch)
`userId` | Triggering user's unique ID
`isSubscribed` | Boolean for Twitch subscription status of triggering user | `True` / `False`
`isVip` | Boolean for Twitch VIP status of triggering user | `True` / `False`
`isModerator` | Boolean for Twitch moderator status of triggering user | `True` / `False`
`randomUser0` | The `username` of a random user present in chat |  *v0.1.0 - v0.1.7*{.version-badge} Adds random Twitch users automatically <p>*v0.1.8+*{.version-badge} Requires use of the `Add Random Users` sub-action</span>
`randomUserName0` | The Display name of a random user present in chat |  *v0.1.0 - v0.1.7*{.version-badge} Adds random Twitch users automatically <p>*v0.1.8+*{.version-badge} Requires use of the `Add Random Users` sub-action</span>
`__source` | The name of the event triggering the action
`date` | current system date | Accepts any standard formatting notation eg. `%date:yyyy/MM/dd%` or `%date:dddd, dd MMMM yyyy%`
`time` | current system time | Accepts any standard formtting notation eg. `HH-mm`
`actionId` | The unique ID number of the first action called |  *v0.1.8+*{.version-badge} 
`runningActionId` | The instance ID number of the action in the queue | *v0.1.8+*{.version-badge} 
`eventSource` | a string value to specify which platform generated the event| *v0.1.8+*{.version-badge} `twitch`, `youtube`