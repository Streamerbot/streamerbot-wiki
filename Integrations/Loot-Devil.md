---
title: Loot Devil (WIP)
description: 
published: false
date: 2022-08-31T08:34:19.042Z
tags: v0.1.11
editor: markdown
dateCreated: 2022-08-31T01:57:24.360Z
---

## Overview
> **BUG:**
> The Loot Devil intergration doesn't work currently because of the API settings on the Loot Devil site not working
{.is-danger}

## Configuration
- [Steamer.bot Loot Devil Connecting Page](https://streamer.bot/user/settings#lootdevil)
- [Loot Devil Api Page](https://lootdevil.com/integrations/api)
## Variables
### Gifted

```json
{
  "type": "Gift",
  "from": "John Doe",
  "message": "Thanks for all the content you create!",
  "amount": "100",
  "currency": "USD",
  "amount_formatted": "$100",
  "items": [
    {
      "name": "$100 tip",
      "price": "100",
      "price_formatted": "$100",
      "url": "https://lootdevil.com/username/gift/1",
      "image": "https://static.lootdevil.com/tip-jar-1.jpg"
    } 
  ]
}
```