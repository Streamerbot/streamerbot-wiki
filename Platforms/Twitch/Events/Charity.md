---
title:  Charity
description: Twitch Events Reference
published: true
date: 2022-10-30T13:09:04.569Z
tags: v0.1.14
editor: markdown
dateCreated: 2022-09-26T15:58:17.808Z
---

## Variables
### Donation Event
The donation event occurs when someone has donated to your charity.

Variable that are included are as follows:

Name | Description
----:|:------------
`baseAmount` | The amount of the donation as a whole number
`donationAmount` | The amount of the donation in decimal form
`charity.name` | The name of the charity you are supporting
`currency.code` | The 3 letter ISO currency code
`currency.exponent` | Divide base amount by 10 to the power of this number to get the decimal value
{.vars-table}

> Twitch is providing amount values for Charity calls as whole numbers, so $42.00 will return as 4200.
{.is-warning}

### Completed Event
When donations come through, a check is made if your current donation amount matches what your goal is, and will send a compelted event if this is true.

Variable that are included are as follows:

Name | Description
----:|:------------
`charity.id` | Twitch's internal ID for your campaign
`charity.timestamp` | The timestamp of the event
`charity.currency` | The 3 letter ISO currency code
`charity.donationTotal` | How much you have raised so far, asa  whole number
`charity.goalTarget` | Your campaign's target amount as a whole number
{.vars-table}

> Twitch is providing amount values for Charity calls as whole numbers, so $42.00 will return as 4200.
{.is-warning}