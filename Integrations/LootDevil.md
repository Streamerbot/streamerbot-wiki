---
title: LootDevil
description: Integrate Streamer.bot with the LootDevil webhooks API
published: true
date: 2022-09-11T23:10:32.218Z
tags: integrations, v0.1.11, webhooks
editor: markdown
dateCreated: 2022-08-31T01:57:24.360Z
---

## Overview
[LootDevil](https://lootdevil.com) aims to provide safe and secure wishlists for creators, enabling you to accept gifts from your fans without sharing your name and address.

> This integration requires the [Streamer.bot Website Integration](/en/Integrations/Streamer-bot)
{.is-success}


## Configuration
### Webhook Setup

1. Navigate to your [User Settings](https://streamer.bot/user/settings#lootdevil) page on the Streamer.bot website
2. <kbd><i class="mdi mdi-content-copy"></i> Copy</kbd> the  LootDevil Webhook URL
3. Navigate to the [API Settings](https://lootdevil.com/integrations/api) page on the LootDevil website
4. <kbd><i class="mdi mdi-content-paste"></i> Paste</kbd> the URL copied from step 2 above into the `Webhook URL` field
5. <kbd><i class="mdi mdi-content-copy"></i> Copy</kbd> the LootDevil Signing Secret
6. Return to the [User Settings](https://streamer.bot/user/settings#lootdevil) page on the Streamer.bot website
7. <kbd><i class="mdi mdi-content-paste"></i> Paste</kbd> the secret copied from step 5 above into the `LootDevil Webhook Secret` field


### Streamer.bot Setup

Navigate to `Integrations -> Streamer.bot Website -> LootDevil` in the Streamer.bot application

![streamerbot-intergrations-streamerbot_website-lootdevil.png](/intergrations/lootdevil/streamerbot-intergrations-streamerbot_website-lootdevil.png =700x)

Here you can assign an action to `Gifted` events from LootDevil!

## Variables
### Gifted
Name | Description
----:|:------------
`timestamp` | Timestamp indicating when the event was triggered e.g. 12/23/2003 10:19:47 PM
`from` | The user that triggered this event
`message` | The user's message
`amount` | The amount of money spent formatted<br> `format:` `100`
`amount_formatted` | The amount of money spent formatted <br> `format:` `$100`
`currency` | Three letter formated currency <br> `format:` `USD`
`items[#].name` | The name of the item
`items[#].price` | The price of the item
`items[#].price_formatted` | The price of the item formatted
`items[#].url` | The url of the item
`items[#].image` | The image of the item
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)
{.btn-grid .my-5}