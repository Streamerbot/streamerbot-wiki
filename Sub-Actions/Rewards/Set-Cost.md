---
title: Set Cost
description: Channel Point Rewards Sub-Actions Reference
published: true
date: 2023-02-04T11:48:20.640Z
tags: subactions, rewards, channel-point-rewards
editor: markdown
dateCreated: 2021-11-02T04:07:26.868Z
---

## Overview
Change the cost of a channel point reward.

![overview.png](/Sub-Actions/Twitch/set-cost/overview.png =400x)

## Configuration
### Reward
Select the reward.

### Cost
Enter the amount you would like to set or modify

### Operator
Name | Description
----:|:------------
`None` | Set the cost to the amount entered
`Add` | Add the amount entered to the current cost
`Subtract` | Subtract the amount entered from the current cost
`Multiply` | Multiplay the amount entered with the current cost
`Divide` | Divice the current cost by the amount entered

### Reset to Original
This will automatically fill the `Cost` input with the original cost and set`Operator` to `None`.

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}