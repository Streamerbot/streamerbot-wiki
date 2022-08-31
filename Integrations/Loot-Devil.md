---
title: Loot Devil (WIP)
description: 
published: false
date: 2022-08-31T11:38:18.779Z
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
Name | Description
----:|:------------
`__source` | LootDevilGifted
`timestamp` | 8/31/2022 11:33:36 AM
`from` | John Doe
`message` | Thanks for all the content you create!
`amount` | 100
`amount_formatted` | $100
`currency` | USD
`items[#].name` | $100 tip
`items[#].price` | 100
`items[#].price_formatted` | $100
`items[#].url` | https://lootdevil.com/username/gift/1
`items[#].image` | https://static.lootdevil.com/tip-jar-1.jpg

## Other
---

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

__source	LootDevilGifted
timestamp	8/31/2022 11:33:36 AM
from	John Doe
message	Thanks for all the content you create!
amount	100
amount_formatted	$100
currency	USD
items[0].name	$100 tip
items[0].price	100
items[0].price_formatted	$100
items[0].url	https://lootdevil.com/username/gift/1
items[0].image	https://static.lootdevil.com/tip-jar-1.jpg
actionId	458f22e4-c129-4372-b563-d498e99d36ec
eventSource	lootdevil
runningActionId	e1f320e7-be3f-43fd-b62c-d7cdb8f9d485