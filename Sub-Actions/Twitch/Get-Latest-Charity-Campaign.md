---
title: Get Latest Charity Campaign
description: Twitch Sub-Actions Reference
published: true
date: 2023-04-25T17:19:55.762Z
tags: 
editor: markdown
dateCreated: 2022-11-03T19:38:18.188Z
---

## Overview
Fetches your latest Twitch Charity campaign and adds the information as variables.

![overview.png](/Sub-Actions/Twitch/get-latest-charity-campaign/overview.png =400x)

## Variables
Name | Description
----:|:------------
`campaignId` | Twitch's internal ID for your campaign.
`charity.name` | The name of the charity you are supporting.
`charity.description` | The description of the charity you are supporting.
`charity.logoUrl` | The logo of the charity you are supporting.
`charity.websiteUrl` | The website to the charity you are supporting.
`currentAmount` | How much you have raised so far, asa  whole number.
`targetAmount` | Your campaign's target amount as a whole number.
{.vars-table}

> Twitch is providing amount values for Charity calls as whole numbers, so $42.00 will return as 4200.
{.is-warning}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}