---
title: Ad Mid Roll
description: Twitch Triggers Reference
published: true
date: 2023-04-25T21:12:30.551Z
tags: 
editor: markdown
dateCreated: 2023-04-25T21:00:23.693Z
---

## Overview
This triggers 5 seconds prior to the start of the ad. See the [Ad Run](/Trigger/Twitch/Ads/Ad-Run) trigger if you want it to trigger at ad start.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `PubSub`
Added in: | *v0.1.15*{.version-badge}

## Variables
Name | Description
----:|:------------
`ad.commercialId` | The ID of the ad that's about to run.
`ad.jitterTime` | How long until the ad runs in milliseconds.
`ad.warmupTime` | How long until the ad runs in milliseconds.
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}