---
title: Charity Donation
description: Twitch Triggers Reference
published: true
date: 2023-05-20T18:06:54.147Z
tags: 
editor: markdown
dateCreated: 2023-05-20T18:06:54.147Z
---

## Overview
When a charity event gets a donation.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `EventSub`
Added in: | *v0.1.14*{.version-badge}

## Variables
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

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}