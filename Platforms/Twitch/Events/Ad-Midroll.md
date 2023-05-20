---
title: Ad Midroll
description: Twitch Events Reference
published: true
date: 2023-03-16T13:04:34.166Z
tags: 
editor: markdown
dateCreated: 2023-02-05T17:04:50.686Z
---

## Overview
This event gets triggered 5 seconds before the ad starts, you cannot change this duration. If you want an event for when the ad starts, use the [Ad Run](/Platforms/Twitch/Events/Ad-Run) event

## Variables
Name | Description
----:|:------------
`ad.commercialId` | The ID of the ad that's about to run
`ad.jitterTime` | How long until the ad runs (ms)
`ad.warmupTime` | How long until the ad runs (ms)
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}