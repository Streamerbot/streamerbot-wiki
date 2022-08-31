---
title: Loot Devil
description: 
published: false
date: 2022-08-31T21:50:59.094Z
tags: v0.1.11
editor: markdown
dateCreated: 2022-08-31T01:57:24.360Z
---

## Overview
> **BUG:**
> The Loot Devil intergration doesn't work currently because of the API settings on the Loot Devil site not working
{.is-danger}

## Configuration
<span></span>

<h3 class="mdi mdi-account-cog" style="font-size: 20px; color: #A257ED; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 5px; text-align: center;"> Streamer.bot Website User Settings</h3>

Go to [/settings#lootdevil](https://streamer.bot/user/settings#lootdevil) on the streamer.bot website

Copy the `LootDevil Webhook URL`

---

<h3 class="mdi mdi-api" style="font-size: 20px; color: #4F46E5; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 5px; text-align: center;"> Loot Devil API Settings</h3>

Go to [lootdevil.com/integrations/api](https://lootdevil.com/integrations/api)

---

<h3 class="mdi mdi-account-cog" style="font-size: 20px; color: #A257ED; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 5px; text-align: center;"> Streamer.bot Website User Settings</h3>

---

<h3 class="mdi mdi-application-cog" style="font-size: 20px; color: #78D1FF; background-color: #181818; padding: 7px; margin: 0px 1px 0px 1px; border-radius: 5px; text-align: center;"> Streamer.bot Application Settings</h3>

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