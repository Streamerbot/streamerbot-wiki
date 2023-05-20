---
title: Gift Subscription
description: Twitch Events Reference
published: true
date: 2023-03-16T13:02:47.985Z
tags: twitch, events
editor: markdown
dateCreated: 2021-12-12T22:40:35.506Z
---

# Overview
A Gift Sub event is triggered when someone buys a subscription for a named person other than themselves.

![events-gift-sub.png](/events-gift-sub.png)

You can configure events to trigger on specific tiers or set to `Generic` to trigger on any tier
Different alerts can also be configured for `anonymous` and `non-anonymous` gifts or you can set to `Either` to trigger on both

## Multi-Month Gifting
Gift subs can also be sent at Tier 1 for 3, 6 or 12 months in advance, you can configure specific alerts for each of these, again they can be `Anonymous`, `Non-Anonymous` or `Either`

## Ranges
The ranges here refer to the total amount of gift subs at a particular tier that a user has given
Ranges can be `Generic` to match any Tier or can be set to count gifts of specific tiers only.

# Variables
Name | Description
----:|:------------
`recipientUser` | Recipient user's display name
`recipientUserName` | Recipient user's Twitch! login name
`recipientId` | Recipient user's Twitch! ID
`totalSubsGifted` | Total number of subscriptions this user has gifted
`monthsGifted` | Number of prepaid months gifted <br> `1`, `3`, `6`, `12`
`fromGiftBomb` | Boolean value if source was a `giftBomb` <br> `True`/`False` 
`subBombCount` | A value to record the number of Gift Subs if part of a Bomb
`cumulativeMonths` | Total months recipient has been subscribed for <br> If 1 this is a new subscriber, any larger it is a re-sub
`badgeCount` | *v0.1.8+*{.version-badge}
`badges` | *v0.1.8+*{.version-badge}
`anonymous` | Boolean value indicating the gift was anonymous <br> `True`/`False` 
`tier` | Subscription tier as a string <br> `tier 1`, `tier 2`, `tier 3`
`role` | What role the gifter has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`isSubscribed` | Boolean value indicating the sender's subscription status <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}