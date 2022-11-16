---
title: HTTP Server
description: 
published: true
date: 2022-11-16T14:44:15.390Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:02.438Z
---

You'll be able to setup an HTTP listener within CPH to make HTTP queries to execute actions and query for data.

![HTTP Server Settings](https://user-images.githubusercontent.com/3193453/121987897-5ec18b00-cd67-11eb-9ec8-3786248b909a.png)

Most methods mirror the Websocket Server requests that you can make

## /GetActions (GET)
This is a very basic request, and will get you a list of the actions in CPH, this mirrors the Websocket server request.

```json
"actions": [
  {
    "id": "<action guid>",
    "name": "<action name>"
  },
]
```
## /DoAction (POST)
This will allow you to execute an action, it returns no data, only a 204 No Content response, it is a POST method and requires the following data

```json
{
  "action": {
    "id": "<guid>",
    "name": "<name>"
  },
  "args": {
    "key": "value",
  }
}
```

## /GetCredits (GET)
You can retrieve the credits data via this request.

Request results will be

```json
{
  "Events": {
    "Follows": [],
    "Cheers": [],
    "Subs": [],
    "ReSubs": [],
    "GiftSubs": [],
    "GiftBombs": [],
    "Raided": [],
    "RewardRedemptions": [],
    "GoalContributions": [],
    "GameUpdates": [],
    "Pyramids": []
  },
  "HypeTrainConductor": [],
  "HypeTrainContributors": [],
  "User": {
    "Editors": [],
    "Moderator": [],
    "Subscriber": [],
    "VIPs": [],
    "Users": [],
    "regulars": []
  },
  "Custom": {},
  "TopBits": {
    "All": [],
    "Month": [],
    "Week": []
  },
  "TopChannelRewards": []
}
```

## /TestCredits (GET)
This will provide a credits data but with dummy data filled in so you can do testing

## /ClearCredits (GET)
This will clear the credits, and return a 204 No Content response

## /ClearFirstWordsCache (GET)
This will clear the first words cache, and return a 204 No Content response