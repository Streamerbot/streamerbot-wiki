---
title: Generic
description: 
published: true
date: 2022-07-01T17:53:37.014Z
tags: 
editor: markdown
dateCreated: 2022-06-30T19:57:33.363Z
---

# Generic

Generic variables are available to most event sources, so consider these the minimum you can use. Other sources will expand on these with variables specific to that event or sub-action

Variable | Description | Notes
---------:|------------
`user` | User's Display Name | (**Note** this is case sensitive when using in a comparison)
`userType` | Specifies which streaming service the triggering user is coming from| <span style="color:cyan">*(0.1.8+)*</span>  `twitch`,`youtube`
`userName` | User's Login Name |(**Note** this is all lowercase when using in a comparison for Twitch)
`userId` | Triggering user's unique ID
`isSubscribed` | Boolean for Twitch subscription status of triggering user | `True` / `False`
`isVip` | Boolean for Twitch VIP status of triggering user | `True` / `False`
`isModerator` | Boolean for Twitch moderator status of triggering user | `True` / `False`
`randomUser0` | The `username` of a random user present in chat |  <span style="color:cyan">*(0.1.8+ does not include random users by default)*</span>
`randomUserName0` | The Display name of a random user present in chat |  <span style="color:cyan">*(0.1.8+ does not include random users by default)*</span>
`__source` | The name of the event triggering the action
`date` | current system date | Accepts any standard formatting notation eg. `%date:yyyy/MM/dd%` or `%date:dddd, dd MMMM yyyy%`
`time` | current system time | Accepts any standard formtting notation eg. `HH-mm`
`actionId` | The unique ID number of the first action called |  <span style="color:cyan">*(0.1.8+)*</span>
`runningActionId` | The instance ID number of the action in the queue | <span style="color:cyan">*(0.1.8+)*</span>
`eventSource` | a string value to specify which platform generated the event| <span style="color:cyan">*(0.1.8+)*</span> `twitch`, `youtube`