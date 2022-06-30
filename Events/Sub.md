---
title: Subscription
description: First time subscribers to the channel
published: true
date: 2022-06-30T20:22:45.685Z
tags: 
editor: markdown
dateCreated: 2021-11-14T22:27:36.317Z
---

# Subscriptions

## Sub
This event triggers when a user first subscribes themselves to the channel and has not recieved any gift subs![sub.png](/sub.png)

Actions can be assigned to `Generic Action` which will trigger on every first subscription 
You can also assign actions to specific Tiers `Twitch Prime` `Tier 1` `Tier 2` `Tier3`

> If you assign actions to both generic and specific tiers both actions will play and if they are not in the same blocking queue they will overlap
{.is-warning}

## Re-Sub
This event triggers when a user subscribes themselves to the channel and has already had at least one month of subscription paid or gifted to them


![re-sub.png](/re-sub.png)

Actions can be assigned to `Generic Action` which will trigger on every first subscription 
You can also assign actions to specific Tiers `Twitch Prime` `Tier 1` `Tier 2` `Tier3`

> If you assign actions to both generic and specific tiers both actions may play and if they are not in the same blocking queue they will overlap
{.is-warning}

## Per Tier & Cumulative Months Ranges

You can define ranges to assign special actions that will trigger in place of the regular ones 

These ranges refer to the both the tier they subscribe at and the total time they have been subscribed for

