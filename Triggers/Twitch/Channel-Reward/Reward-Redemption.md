---
title: Reward Redemption
description: Twitch Triggers Reference
published: true
date: 2023-05-20T18:17:47.989Z
tags: 
editor: markdown
dateCreated: 2023-05-20T18:15:16.142Z
---

## Overview
When someone redeems a reward redemption

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `PubSub`
Added in: | *v0.0.30*{.version-badge}

## Variables
This includes the [User](/Variables/User-Variables) variables and the [Broadcaster](/Variables/Broadcaster) variables.

Name | Description
----:|:------------
`redemptionId` | String identifier for this redemption (used to refund reward) <br> `4d9f236b-7486-481a-89af-1d03676d5275`
`rewardId` | String identifier for this reward <br> `44e86f71-8ace-4739-a123-3ff095489343`
`rewardName` | Name of the reward <br> `My Reward`
`rewardPrompt` | The verbiage shown on the channel point description *v0.1.5+*{.version-badge} <br> `My cool Reward Prompt`
`rewardCost` | The channel point cost of the redeemed reward *v0.1.5+*{.version-badge}  <br> `100`
`counter` | Number of times this reward has been redeemed <br> `1`
`userCounter` | Number of times the same user has redeemed this reward <br> `1`
`rawInput` | String text entered by the user (if required) <br> `https://streamer.bot/Test Unescaped Text $$$`
`rawInputEscaped` | String text entered by the user (escaped) <br> `https://streamer\.bot/Test Escaped Text \$\$\$`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}