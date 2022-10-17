---
title: Update
description: Channel Point Rewards Sub-Actions Reference
published: true
date: 2022-10-17T17:20:38.700Z
tags: twitch, channel-points, subactions
editor: markdown
dateCreated: 2022-06-11T05:05:44.509Z
---

## Overview
Modify the `Title`, `Prompt` and `Cost` of a channel point reward at once.

![update_reward.png](/update_reward.png)

## Configuration
### Reward
Select the reward you want to modify.

### Title
Enter the new title for your channel point reward.

This input accepts [variables](/en/Variables)

### Prompt
Enter the text to apply to your reward prompt.

This input field can span multiple lines and will also accept [variables](/en/Variables)

### Cost
Enter the amount you would like to set or modify

### Operator
| Values | Description |
|-------:|:------------|
|`None`| Set the cost to the amount entered
|`Add`| Add the amount entered to the current cost
|`Subtract`| Subtract the amount entered from the current cost
|`Multiply`| Multiplay the amount entered with the current cost
|`Divide`| Divice the current cost by the amount entered

### Reset to Original
Revert all reward settings to their original values.

## Variables
No variables generated.

---

- [<i class="mdi mdi-chevron-left"></i>**Rewards Sub-Actions *Go Back***](/en/Sub-Actions/Rewards)
- [<i class="mdi mdi-twitch text--twitch"></i>**Update Redemption Status *Up Next***](/en/Sub-Actions/Rewards/Update-Redemption-Status)
{.btn-grid .my-5}