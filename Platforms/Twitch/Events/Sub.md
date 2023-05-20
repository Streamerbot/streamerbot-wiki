---
title: Subscription
description: Twitch Events Reference
published: true
date: 2023-05-20T22:04:20.076Z
tags: twitch, events
editor: markdown
dateCreated: 2021-11-14T22:27:36.317Z
---

# Overview

## Sub
This event triggers when a user first subscribes themselves to the channel and has not recieved any gift subs.

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

# Variables
Name | Description
----:|:------------
`tier` | Subscription tier <br> `prime`, `tier 1`. `tier 2`, `tier 3`
`monthStreak` | Current subscription streak in months <br> *Not for sub event. Only for re-sub event.*{.small}
`cumulative` | Total number of months a user has been subscribed for <br> *Not for sub event. Only for re-sub event.*{.small}
`rawInput` | The message entered
`rawInputEscaped` | The message escaped
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`color` | User's color (if they have chosen one or a random one if not)
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}