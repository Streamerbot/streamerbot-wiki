---
title: Gift Sub
description: 
published: true
date: 2022-06-30T20:31:52.670Z
tags: 
editor: markdown
dateCreated: 2021-12-12T22:40:35.506Z
---

# Gift Subs	

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

Variable | Description | Notes
---------:|------------
`recipientUser` | Recipient user's display name
`recipientUserName` | Recipient user's Twitch! login name
`recipientId` | Recipient user's Twitch! ID
`totalSubsGifted` | Total number of subscriptions this user has gifted
`monthsGifted` | Number of prepaid months gifted | `1`, `3`, `6`, `12`
`fromGiftBomb` | Boolean value if source was a `giftBomb` |  `True`/`False` 
`subBombCount` | A value to record the number of Gift Subs if part of a Bomb
`cumulativeMonths` | Total months recipient has been subscribed for | If 1 this is a new subscriber, any larger it is a re-sub
`badgeCount` | | <span style="color:blue">*(0.1.8+)*</span>
`badges` | | <span style="color:blue">*(0.1.8+)*</span>
`anonymous` | Boolean value indicating the gift was anonymous | `True`/`False` 
`tier` | Subscription tier as a string | `tier 1`, `tier 2`, `tier 3`
`role` | What role the gifter has `(1-4)` | 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`isSubscribed` | Boolean value indicating the sender's subscription status |  `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status |  `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status |  `True`/`False`
