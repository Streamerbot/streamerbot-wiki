---
title: StreamElements
description: Streamer.bot integration with StreamElements
published: true
date: 2022-09-08T21:46:12.430Z
tags: integrations, streamelements
editor: markdown
dateCreated: 2022-05-13T04:07:00.154Z
---

![streamlabs-logo.png](https://streamer.bot/img/integrations/streamelements.png){.align-abstopright}
## Overview

The StreamElements integration allows you to connect Streamer.bot with your StreamElements account to receive tip and merch events.

![integrations-streamelements-events-018.png](/integrations-streamelements-events-018.png =800x)

## Configuration

You can find the configuration for this integration at `Integrations -> StreamElements -> Settings`

### Authentication
**The StreamElements integration now uses OAuth for authorizing against your account**

To connect Streamer.bot with your StreamElements account:
1. Navigate to the settings tab within the StreamElements integration
2. Click `Connect` and authorize **Streamer.bot** to connect to your account

## Events
The following StreamElements events are monitored by Streamer.bot and will allow you to execute actions with their content:

### Tips / Donations
The Tip event is fired any time a new donation is receieved through StreamElements{.subtitle}

Name | Description
----:|:------------
`tipUsername` | Username of the user as provided by StreamElements
`tipAvatar` | Avatar of the user
`tipAmount` | The amount of the tip
`tipCurrency` | 3 letter currency code
`tipMessage` | Any tip message the user included
`isTest` | Boolean value indicating the tip was a test |  `True`/`False`

### Merch
The Merch event is fired any time a new Merch sale is receieved through StreamElements{.subtitle}

Name | Description
----:|:------------
`merchUsername` | Username of the user as provided by StreamElements
`merchAvatar` | Avatar of the user
`merchAmount` | The amount of the purchase
`merchCurrency` | 3 letter currency code
`merchMessage` | Any message the user included
`merchQuantity` | The total number of items purchased
`merchItems` | The number of distinct items purchased

`merchItem#.name` | Name of the item purchased, where # is the index of the item (0 based)
`merchItem#.price` | Price of the item purchased, where # is the index of the item (0 based)
`merchItem#.quantity` | How many of the item was purchased, where # is the index of the item (0 based)

---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)
{.btn-grid .my-5}