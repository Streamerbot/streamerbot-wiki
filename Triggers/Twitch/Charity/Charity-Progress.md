---
title: Charity Progress
description: Twitch Triggers Reference
published: true
date: 2023-05-20T18:08:43.529Z
tags: 
editor: markdown
dateCreated: 2023-05-20T18:08:43.529Z
---

## Overview
When a charity event progresses.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `EventSub`
Added in: | *v0.1.15*{.version-badge}

## Variables
Name | Description
----:|:------------
`charity.currentAmount.value` | The current amount of the money raised in decimal form e.g. `5.25` ($5.25).
`charity.currentAmount.valueMinor` | The current amount of the money raised in non-decimal form e.g. `525` ($5.25).
`charity.currentAmount.currency` | The 3 letter ISO currency code for the current amount of money raised.
`charity.targetAmount.value` | The target amount of the money to be raised in decimal form e.g. `20` ($20.00).
`charity.targetAmount.valueMinor` | The target amount of the money to be raised in non-decimal form e.g. `2000` ($20.00).
`charity.targetAmount.currency` | The 3 letter ISO currency code for the target amount of money to be raised.
`charity.id` | Twitch's internal ID for your campaign.
`charity.name` | The name of the charity you're supporting.
`charity.description` | The description of the charity you're supporting.
`charity.logo` | The URL to the logo of the charity you're supporting.
`charity.website` | The URL to the website of the charity you're supporting.
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}