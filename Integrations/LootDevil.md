---
title: LootDevil
description: The Wishlist Built for Creators
published: false
date: 2022-09-01T09:28:05.459Z
tags: v0.1.11
editor: markdown
dateCreated: 2022-08-31T01:57:24.360Z
---

## Overview
Safe and secure wishlists for streamers, influencers and creators. Accept gifts from your fans without sharing your name and address.

## Configuration
<span></span>

<h3 class="mdi mdi-account-cog" style="font-size: 20px; color: #A257ED; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 12px; text-align: center;"> Streamer.bot Website User Settings</h3>

![lootdevil-user-settings-copy-webhook-url.png](/intergrations/lootdevil/lootdevil-user-settings-copy-webhook-url.png)

Go to [here](https://streamer.bot/user/settings#lootdevil) on the streamer.bot website
- Copy the <span class="mdi mdi-content-copy" style="color: #A257ED; background-color: #111111; padding: 1px 7px 1px 7px; margin: 0px 1px 0px 1px; border-radius: 5px;"> LootDevil Webhook URL</span>

---

<h3 class="mdi mdi-gold" style="font-size: 20px; color: #4F46E5; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 12px; text-align: center;"> LootDevil API Settings</h3>

![lootdevil-api-copy-paste-settings.png](/intergrations/lootdevil/lootdevil-api-copy-paste-settings.png)
Go to [here](https://lootdevil.com/integrations/api) on the LootDevil website

- Paste the <span class="mdi mdi-content-paste" style="color: #4F46E5; background-color: #111111; padding: 1px 7px 1px 7px; margin: 0px 1px 0px 1px; border-radius: 5px;"> LootDevil Webhook URL</span>
- Copy the <span class="mdi mdi-content-copy" style="color: #4F46E5; background-color: #111111; padding: 1px 7px 1px 7px; margin: 0px 1px 0px 1px; border-radius: 5px;"> Signing Secret</span>

---

<h3 class="mdi mdi-account-cog" style="font-size: 20px; color: #A257ED; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 12px; text-align: center;"> Streamer.bot Website User Settings</h3>

![lootdevil-user-settings-paste-webhook-secret.png](/intergrations/lootdevil/lootdevil-user-settings-paste-webhook-secret.png)

Paste the <span class="mdi mdi-content-paste" style="color: #A257ED; background-color: #111111; padding: 1px 7px 1px 7px; margin: 0px 1px 0px 1px; border-radius: 5px;"> Signing Secret</span>

---

<h3 class="mdi mdi-application-cog" style="font-size: 20px; color: #78D1FF; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 12px; text-align: center;"> Streamer.bot Application Settings</h3>

![streamerbot-intergrations-streamerbot_website-lootdevil.png](/intergrations/lootdevil/streamerbot-intergrations-streamerbot_website-lootdevil.png)

- [Steamer.bot Loot Devil Connecting Page](https://streamer.bot/user/settings#lootdevil)
- [Loot Devil Api Page](https://lootdevil.com/integrations/api)

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