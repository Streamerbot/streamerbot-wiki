---
title: Gift Bombs
description: Twitch Events Reference
published: true
date: 2023-03-16T13:02:54.990Z
tags: twitch, events
editor: markdown
dateCreated: 2021-12-12T22:44:55.140Z
---

> If you want to know who those subs are gifted to, you need to use the Gift Sub event with the variable `recipientUser`
{.is-info}

## Overview
A Gift bomb event is the most typical event for subscription gifting and is triggered when a gift sub is purchased but no specific user is targeted, i.e. the recipient is random

A gift bomb happens when there are 2+ gift subs.  In Twitch Chat you'll see the message **so and so is gifting # subs to the community** followed by a slew of Gift Subs

![events-gift-bomb.png](/events-gift-bomb.png)

You can configure events to trigger on specific tiers or set to `Generic` to trigger on any tier
Different alerts can also be configured for `anonymous` and `non-anonymous` gifts or you can set to `Either` to trigger on both


### Ranges
The ranges here refer to the number of gift subs in this specific purchase.
Ranges can be `Generic` to match any Tier or can be set to count gifts of specific tiers only.
The Ranges can also be `Anonymous`, `Non-Anonymous` or `Either`

## Variables
Name | Description
----:|:------------
`gifts` | Number of subscriptions in this gift bomb
`totalGifts` | Total number of subscriptions this user has gifted
`fromGiftBomb` | Boolean value if sub came from a gift bomb <br>  `True`/`False` 
`anonymous` | Boolean value indicating the gift was anonymous <br> `True`/`False` 
`tier` | Subscription tier as a string <br> `tier 1`. `tier 2`, `tier 3`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}