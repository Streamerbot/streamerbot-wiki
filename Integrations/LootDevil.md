---
title: LootDevil
description: The Wishlist Built for Creators
published: true
date: 2022-09-11T22:36:41.688Z
tags: v0.1.11
editor: markdown
dateCreated: 2022-08-31T01:57:24.360Z
---

## Overview
Safe and secure wishlists for streamers, influencers and creators. Accept gifts from your fans without sharing your name and address.

## Configuration
<span></span>

<h3 class="mdi mdi-account-cog"> Streamer.bot Website User Settings</h3>

![lootdevil-user-settings-copy-webhook-url.png](/intergrations/lootdevil/lootdevil-user-settings-copy-webhook-url.png)

Go to [here](https://streamer.bot/user/settings#lootdevil) on the streamer.bot website
- Copy the <span class="mdi mdi-content-copy"> LootDevil Webhook URL</span>

---

<h3 class="mdi mdi-gold"> LootDevil API Settings</h3>

![lootdevil-api-copy-paste-settings.png](/intergrations/lootdevil/lootdevil-api-copy-paste-settings.png)
Go to [here](https://lootdevil.com/integrations/api) on the LootDevil website

- Paste the <span class="mdi mdi-content-paste"> LootDevil Webhook URL</span>
- Copy the <span class="mdi mdi-content-copy"> Signing Secret</span>

---

<h3 class="mdi mdi-account-cog"> Streamer.bot Website User Settings</h3>

![lootdevil-user-settings-paste-webhook-secret.png](/intergrations/lootdevil/lootdevil-user-settings-paste-webhook-secret.png)

Paste the <span class="mdi mdi-content-paste"> Signing Secret</span> in the `LootDevil Webhook Secret`

---

<h3 class="mdi mdi-application-cog"> Streamer.bot Application Settings</h3>

![streamerbot-intergrations-streamerbot_website-lootdevil.png](/intergrations/lootdevil/streamerbot-intergrations-streamerbot_website-lootdevil.png)

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
#### LINKS

- [<img src="https://streamer.bot/logo.png"></img> **User Settings *The connection LootDevil settings***](https://streamer.bot/user/settings#lootdevil)
- [<img src="https://streamer.bot/img/integrations/lootdevil.png"></img> **Api Page *The Api page from LootDevil***](https://lootdevil.com/integrations/api)
{.btn-grid .my-5}
---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)
{.btn-grid .my-5}