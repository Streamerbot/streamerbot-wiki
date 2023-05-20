---
title: Ad Run
description: Twitch Triggers Reference
published: true
date: 2023-04-27T14:57:37.782Z
tags: 
editor: markdown
dateCreated: 2023-04-25T20:55:52.968Z
---

## Overview
This triggers when an ad starts to run. See the [Ad Midroll](/Trigger/Twitch/Ads/Ad-Mid-Roll) trigger if you want the trigger to run 5 seconds prior to the ad.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `PubSub`
Added in: | *v0.1.10*{.version-badge}

## Variables
Name | Description
----:|:------------
`adLength` | The length of the ad in seconds.
`adScheduled` | If this ad was scheduled. Returns `True` or `False`.
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}