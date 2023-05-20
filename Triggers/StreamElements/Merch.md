---
title: Merch
description: StreamElements Triggers Reference
published: true
date: 2023-03-16T11:14:22.311Z
tags: 
editor: markdown
dateCreated: 2023-03-15T20:26:58.297Z
---

## Overview
This triggers when someone buys your merch from StreamElements.

For a detailed guide about StreamElements see [this page](/Integrations/StreamElements).

## Variables
Name | Description
----:|:------------
`merchUsername` | Username of the user as provided by StreamElements (may not be from Twitch)
`merchAvatar` | The URL of the user's avatar
`merchAmount` | The amount of the purchase
`merchCurrency` | The 3 letter payment currency code
`merchMessage` | The message that the user may has included
`merchQuantity` | The total number of items purchased
`merchItems` | The number of distinct items purchased
`merchItem#.name` | Name of the item purchased, where # is the index of the item (0 based)
`merchItem#.price` | Price of the item purchased, where # is the index of the item (0 based)
`merchItem#.quantity` | How many of the item was purchased, where # is the index of the item (0 based)
{.vars-table}

> Change the `#` to a number from 0 to the end of the merch items. So e.g. `%merchItem0.name%`, `%merchItem1.name%`, `%merchItem2.name%`
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**StreamElements Triggers Reference *Go Back***](/Triggers/StreamElements)
- [<i class="mdi mdi-cash primary--text"></i> **Tip *Next Up***](/Triggers/StreamElements/Tip)
{.btn-grid .my-5}