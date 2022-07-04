---
title: Gift Bombs
description: 
published: true
date: 2022-06-30T20:33:23.648Z
tags: 
editor: markdown
dateCreated: 2021-12-12T22:44:55.140Z
---

# Gift Bombs

A Gift bomb event is the most typical event for subscription gifting and is triggered when a gift sub is purchased but no specific user is targeted, i.e. the recipient is random

A gift bomb happens when there are 2+ gift subs.  In Twitch Chat you'll see the message **so and so is gifting # subs to the community** followed by a slew of Gift Subs

![events-gift-bomb.png](/events-gift-bomb.png)

You can configure events to trigger on specific tiers or set to `Generic` to trigger on any tier
Different alerts can also be configured for `anonymous` and `non-anonymous` gifts or you can set to `Either` to trigger on both


## Ranges

The ranges here refer to the number of gift subs in this specific purchase.
Ranges can be `Generic` to match any Tier or can be set to count gifts of specific tiers only.
The Ranges can also be `Anonymous`, `Non-Anonymous` or `Either`

# Variables


Variable | Description
---------:|------------
`gifts` | Number of subscriptions in this gift bomb
`totalGifts` | Total number of subscriptions this user has gifted
`fromGiftBomb` | Boolean value if sub came from a gift bomb |  `True`/`False` 
`anonymous` | Boolean value indicating the gift was anonymous |  `True`/`False` 
`tier` | Subscription tier as a string | `tier 1`. `tier 2`, `tier 3`
