---
title: Gift Subscription
description: Twitch Triggers Reference
published: true
date: 2023-06-07T08:46:36.644Z
tags: 
editor: markdown
dateCreated: 2023-06-07T08:46:36.644Z
---

## Overview
This triggers when someone gifts a subscription.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `Chat Client`
Added in: | *N/A*{.version-badge}

## Variables
This includes the [User](/Variables/User-Variables) variables.

Name | Description
----:|:------------
`recipientUser` | Recipient user's display name
`recipientUserName` | Recipient user's Twitch login name
`recipientId` | Recipient user's Twitch id
`totalSubsGifted` | Total number of subscriptions the user has gifted
`monthsGifted` | Number of prepaid months gifted <br> `1`, `3`, `6`, `12`
`fromGiftBomb` | Boolean value if this is a `giftBomb` <br> `True`/`False` 
`subBombCount` | A value to record the number of Gift Subs if part of a Bomb
`cumulativeMonths` | Total months recipient has been subscribed for <br> If 1 this is a new subscriber, any larger it is a re-sub
`badgeCount` | The count of the badges that the user has
`badges` | A list of all the badges that the user has
`anonymous` | Boolean value indicating the gift was anonymous <br> `True`/`False` 
`tier` | Subscription tier as a string <br> `tier 1`, `tier 2`, `tier 3`
`role` | What role the gifter has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}