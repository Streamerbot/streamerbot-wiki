---
title: Hype Train
description: Twitch Events Reference
published: true
date: 2023-03-16T13:02:31.431Z
tags: twitch, events
editor: markdown
dateCreated: 2022-01-22T02:59:47.855Z
---

## Overview
In this tab you can assign actions to the various levels of the hype train. 

To get to this tab you need to click through the following tabs, First click the `Settings` tab next click on the `Events` tab then finally click the `Hype Train` tab. You should now see a window just like the image below.

![hypetrain.png](/hypetrain.png =700x)

In this Tab you can see 5 sections: Start, Progression, Level Up, and Finish. Each section will be explained below in their own sections. 

## Test Section 
On the right in this tab is the test section where you can test all that you have just set up. You can test the events, level goal and level total these will let you test the variations and the progression actions you have. Total will let you test the finished event you have set.

## Variables
### Start
Name | Description
----:|:------------
`level` | The current Hype Train level e.g. `3`
`startedAt` | The time the hype train started e.g. `8/25/2020 8:30:27 PM`
`expiresAt` | The time the hype train expires e.g. `8/25/2020 8:32:27 PM`
`duration` | The duration of the hype train e.g. `120`
`percent` | The amount of percentage for the current level e.g. `80%`
`percentDecimal` | The amount of decimal percentage for the current level e.g. `0.8`
`top.bits.user` | The best cheerer of this hype train display name
`top.bits.userName` | The best cheerer of this hype train login name
`top.bits.userId` | The best cheerer of this hype train user id
`top.bits.total` | The amount of bits from the best cheerer of this hype train
`top.subscription.user` | The most amount of giftsubs given by user in this hype train display name
`top.subscription.userName` | The most amount of giftsubs given by user in this hype train login name
`top.subscription.userId` | The most amount of giftsubs given by user in this hype train user id
`top.subscription.total` | The most amount of giftsubs given by user in this hype train giftsub count
`top.other.user` | The user display name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userName` | The user login name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userId` | The user id of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.total` | The toal amount of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`id` | The unique hype train id

### Progression
Name | Description
----:|:------------
`level` | The current Hype Train level e.g. `3`
`startedAt` | The time the hype train started e.g. `8/25/2020 8:30:27 PM`
`expiresAt` | The time the hype train expires e.g. `8/25/2020 8:32:27 PM`
`duration` | The duration of the hype train e.g. `120`
`percent` | The amount of percentage for the current level e.g. `80%`
`percentDecimal` | The amount of decimal percentage for the current level e.g. `0.8`
`contributors` | The amount of contributors of the hype train e.g. `10`
`user` | The user that progresses the hype train display name
`userName` | The user that progresses the hype train login name
`userId` | The user that progresses the hype train user id
`userType` | twitch
`isSubscribed` | If the user that progresses the hype train is a subscriber `True`/`False`
`isModerator` | If the user that progresses the hype train is a moderator `True`/`False`
`isVip` | If the user that progresses the hype train is a vip `True`/`False`
`userPreviousActive` | The time that the user was previously active e.g. `8/25/2020 8:10:27 PM`
`top.bits.user` | The best cheerer of this hype train display name
`top.bits.userName` | The best cheerer of this hype train login name
`top.bits.userId` | The best cheerer of this hype train user id
`top.bits.total` | The amount of bits from the best cheerer of this hype train
`top.subscription.user` | The most amount of giftsubs given by user in this hype train display name
`top.subscription.userName` | The most amount of giftsubs given by user in this hype train login name
`top.subscription.userId` | The most amount of giftsubs given by user in this hype train user id
`top.subscription.total` | The most amount of giftsubs given by user in this hype train giftsub count
`top.other.user` | The user display name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userName` | The user login name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userId` | The user id of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.total` | The toal amount of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`id` | The unique hype train id

### Level Up
Name | Description
----:|:------------
`prevLevel`	| The previous Hype Train level e.g. `2`
`level` | The current Hype Train level e.g. `3`
`startedAt` | The time the hype train started e.g. `8/25/2020 8:30:27 PM`
`expiresAt` | The time the hype train expires e.g. `8/25/2020 8:32:27 PM`
`duration` | The duration of the hype train e.g. `120`
`percent` | The amount of percentage for the current level e.g. `80%`
`percentDecimal` | The amount of decimal percentage for the current level e.g. `0.8`
`contributors` | The amount of contributors of the hype train e.g. `10`
`user` | The user that progresses the hype train display name
`userName` | The user that progresses the hype train login name
`userId` | The user that progresses the hype train user id
`userType` | twitch
`isSubscribed` | If the user that progresses the hype train is a subscriber `True`/`False`
`isModerator` | If the user that progresses the hype train is a moderator `True`/`False`
`isVip` | If the user that progresses the hype train is a vip `True`/`False`
`userPreviousActive` | The time that the user was previously active e.g. `8/25/2020 8:10:27 PM`
`top.bits.user` | The best cheerer of this hype train display name
`top.bits.userName` | The best cheerer of this hype train login name
`top.bits.userId` | The best cheerer of this hype train user id
`top.bits.total` | The amount of bits from the best cheerer of this hype train
`top.subscription.user` | The most amount of giftsubs given by user in this hype train display name
`top.subscription.userName` | The most amount of giftsubs given by user in this hype train login name
`top.subscription.userId` | The most amount of giftsubs given by user in this hype train user id
`top.subscription.total` | The most amount of giftsubs given by user in this hype train giftsub count
`top.other.user` | The user display name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userName` | The user login name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userId` | The user id of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.total` | The toal amount of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`id` | The unique hype train id

### Finish
Name | Description
----:|:------------
`level` | The current Hype Train level e.g. `3`
`startedAt` | The time the hype train started e.g. `8/25/2020 8:30:27 PM`
`percent` | The amount of percentage for the current level e.g. `80%`
`percentDecimal` | The amount of decimal percentage for the current level e.g. `0.8`
`contributors` | The amount of contributors of the hype train e.g. `10`
`top.bits.user` | The best cheerer of this hype train display name
`top.bits.userName` | The best cheerer of this hype train login name
`top.bits.userId` | The best cheerer of this hype train user id
`top.bits.total` | The amount of bits from the best cheerer of this hype train
`top.subscription.user` | The most amount of giftsubs given by user in this hype train display name
`top.subscription.userName` | The most amount of giftsubs given by user in this hype train login name
`top.subscription.userId` | The most amount of giftsubs given by user in this hype train user id
`top.subscription.total` | The most amount of giftsubs given by user in this hype train giftsub count
`top.other.user` | The user display name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userName` | The user login name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userId` | The user id of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.total` | The toal amount of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`id` | The unique hype train id

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}