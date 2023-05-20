---
title:  Charity
description: Twitch Events Reference
published: true
date: 2023-03-16T13:04:00.868Z
tags: v0.1.14
editor: markdown
dateCreated: 2022-09-26T15:58:17.808Z
---

## Overview
Charity Started, Completed, Progress and Donation events.

![twitch-charity-overview.png](/twitch-charity-overview.png =700x)

## Variables
> Twitch is providing amount values for Charity calls as whole numbers, so $42.00 will return as 4200.
{.is-warning}

### Donation Event
The Donation event occurs when someone has donated to your charity.

Name | Description
----:|:------------
`charity.amount.value` | The amount of the donation in decimal form e.g. `5.25` ($5.25).
`charity.amount.valueMinor` | The amount of the donation in non-decimal form e.g. `525` ($5.25).
`charity.amount.currency` | The 3 letter ISO currency code.
`charity.campaignId` | Twitch's internal ID for your campaign.
`charity.name` | The name of the charity you're supporting.
`charity.description` | The description of the charity you're supporting.
`charity.logo` | The URL to the logo of the charity you're supporting.
`charity.website` | The URL to the website of the charity you're supporting.
{.vars-table}

### Started Event
The Started event occurs when your charity event starts.

Name | Description
----:|:------------
`charity.startedAt` | The time and date the charity event started, format: `MM/dd/yyyy h:m:ss tt`.
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

### Progress Event
The donation event occurs when your charity event progresses.

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

### Completed Event
When the creator mannually stops the charity this event is emitted. Note: it won't trigger when the goal matches the progress.

Name | Description
----:|:------------
`charity.stoppedAt` | The time and date the charity event completed, format: `MM/dd/yyyy h:m:ss tt`.
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

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}