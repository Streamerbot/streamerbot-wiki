---
title: WebSocket Server Events
description: Documentation of events that are emitted by the Streamer.bot WebSocket Server
published: true
date: 2022-11-14T14:19:58.509Z
tags: websocket
editor: markdown
dateCreated: 2021-08-25T21:37:12.384Z
---

Below is the current list of events that are emitted by Streamer.bot

> Events are only emitted if they have been subscribed to
{.is-warning}

> Some events are not being broadcast as of **v0.1.7** despite being listed here and have been indicated.  There are some events which may also change, and provide more data then they currently do, this will be noted when they are updated
{.is-info}

Every packet sent by the Websocket Server follows the following schema

### Tab {.tabset}
#### Schema
```json
{
    "timeStamp": ISO 8601 DateTime,
    "event": {
        "source": string
        "type": string
    },
    "data": {.object.} /* see information below for what this can contain */
}
```

#### Example

```json
{
    "timeStamp": "2022-01-30T21:32:04.4588947-05:00",
    "event": {
        "source": "Twitch",
        "type": "ChatMessage"
    },
    "data": {.object.}
}
```

# Twitch

These are the Twitch events that will be broadcast, the examples provided are what will be in the `data` object.  The source will be Twitch, and the type will be tha name for the tab below

### Tab {.tabset}
#### Follow
```json
{
  "userId": 0000000,
  "userName": "<username>",
  "displayName": "<display name>",
  "isTest": true|false
}
```
#### Cheers
```json
{
  "message": {
    "msgId": "21605e47-16d2-4496-8001-509438e1b41c",
    "userId": 00000000
    "username": "<username>",
    "role": 1, /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
    "subscriber": true,
    "displayName": "<display name of cheerer
    "channel": "<channel>",
    "message": "<message that contained the cheer>",
    "isHighlighted": false,
    "isMe": false,
    "isCustomReward": false,
    "isAnonymous": false,
    "isReply": false,
    "bits": 42,
    "hasBits": true,
    "emotes": [],
    "cheerEmotes": [
      {
        "bits": 42,
        "color": "#979797",
        "type": "CheerEmote",
        "name": "Cheer",
        "startIndex": 0,
        "endIndex": 6,
        "imageUrl": "<url to cheer emote>"
      }
    ]
  }
}
```
#### Raid
```json
{
  "viewerCount": 42,
  "profileImage": "test.png",
  "userId": 0000000,
  "userName": "<username>",
  "displayName": "<display name>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

#### StreamUpdate
```json
{
  "channelId": 0000000000,
  "channel": "<user name of broadcaster>",
  "status": "Doing the things!", /* New title of the stream */
  "oldStatus": "This is a different title!", /* Old title of the stream */
  "oldGame": {
    "id": 516097,
    "name": "Deadside"
  },
  "game": {
    "id": 7658,
    "name": "Mario Party 8"
  }
}
```

#### Whisper
```json
{
  "message": {
    "msgId": "60",
    "userId": 00000000,
    "username": "<username>",
    "displayName": "<user's display name>",
    "message": "Test",
    "emotes": []
  }
}
```

#### FirstWord
```json
{
  "message": "test",
  "action": false,
  "user": {
    "id": 0000000000,
    "login": "<username>",
    "display_name": "<displayname>",
    "subscribed": true,
	  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  }
}
```

#### ChatMessage
```json
{
  "message": {
    "msgId": "a0d32df1-d3ca-4fd7-87fb-6c4e958550f0",
    "userId": 00000000,
    "username": "<username>",
    "role": 4,
    "subscriber": true,
    "displayName": "<display name>",
    "channel": "<broadcaster's channel name>",
    "message": "", /* The message the user sent */
    "isHighlighted": false,
    "isMe": false,
    "isCustomReward": false,
    "isAnonymous": false,
    "isReply": false,
    "bits": 0,
    "hasBits": false,
    "emotes": [
      {
        "id": "300400304",
        "type": "Twitch",
        "name": "nate121Raid",
        "startIndex": 5,
        "endIndex": 15,
        "imageUrl": "https://static-cdn.jtvnw.net/emoticons/v2/300400304/default/dark/2.0"
      }
    ],
    "cheerEmotes": []
  }
}
```

### Tab {.tabset}
#### Subs
```json
{
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "color": "#008D99",
  "emotes": [],
  "message": "",
  "userId": 00000000,
  "userName": "<username>",
  "displayName": "<display name>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```
#### ReSub
```json
{
  "cumulativeMonths": 25,
  "shareStreak": true,
  "streakMonths": 1,
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "color": "#FF4500",
  "emotes": [],
  "message": "",
  "userId": 162909743,
  "userName": "admiralai",
  "displayName": "AdmiralAI",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

#### GiftSub
```json
{
  "isAnonymous": false,
  "totalSubsGifted": 1,
  "cumulativeMonths": 4,
  "monthsGifted": 1,
  "fromSubBomb": false,
  "subBombCount": 1,
  "recipientUserId": 00000000,
  "recipientUsername": "<username of recipient>",
  "recipientDisplayName": "<display name of recipient>",
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "userId": 0000000000,
  "userName": "<username of gifter>",
  "displayName": "<displayname of gifter>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

#### GiftBomb
```json
{
  "isAnonymous": false,
  "gifts": 10,
  "totalGifts": 0,
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "userId": 0000000000,
  "userName": "<username of gifter>",
  "displayName": "<displayname of gifter>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

### Tab {.tabset}
#### HypeTrainStart
```json
{
  "level": 1,
  "levelGoal": 3500,
  "levelTotal": 3900,
  "totalGoal": 11500,
  "total": 11100,
  "percent": 1.1142857142857143
}
```

#### HypeTrainUpdate
```json
{
  "userId": 00000000,
  "level": 1,
  "contributors": 1,
  "levelGoal": 3500,
  "levelTotal": 3900,
  "totalGoal": 11500,
  "total": 11100,
  "percent": 1.1142857142857143
}
```

#### HypeTrainLevelUp
```json
{
  "prevLevel": 0,
  "level": 1,
  "contributors": 0,
  "levelGoal": 3500,
  "levelTotal": 3900,
  "totalGoal": 11500,
  "total": 11100,
  "percent": 1.1142857142857143
}
```

#### HypeTrainEnd
```json
 {
   "conductor": {
     "id": 0 /* the twitch user id of the conductor */
   },
   "level": 1,
   "contributorCount": 1,
   "contributors": [
     {
       "id": 00000000
     }
   ],
   "levelGoal": 3500,
   "levelTotal": 3900,
   "totalGoal": 11500,
   "total": 11100,
   "percent": 1.1142857142857143
 }
```

### Tab {.tabset}
#### RewardRedemption
```json
 {
   "id": "9d0911db-7884-4e0f-8cf4-c95c5765c2e5",
   "dateTime": "2022-01-31T03:10:23.3611616Z",
   "userId": 0000000000,
   "userName": "<user name of redeemer>",
   "displayName": "<display name of redeemer>",
   "channelId": 0000000, /* broadcaster channel id */
   "cost": 42,
   "rewardId": "41f257e9-9688-4944-9bf6-28cda1c3fa1f",
   "title": "Test Reward",
   "prompt": "",
   "inputRequired": false,
   "backgroundColor": "#63D0A9",
   "enabled": true,
   "paused": false,
   "subOnly": false
 }
```

#### RewardCreated
```json
{
  "id": "41f257e9-9688-4944-9bf6-28cda1c3fa1f",
  "name": "Test Reward",
  "prompt": "",
  "group": "",
  "cost": 42,
  "userInput": false,
  "persistCounter": false,
  "counter": 1,
  "persistUserCounter": false,
  "backgroundColor": "#63D0A9",
  "userCounters": {}
}
```

#### RewardUpdated
```json
{
  "dateTime": "2022-01-31T03:10:10.9796761Z",
  "channelId": 00000000,
  "cost": 42,
  "rewardId": "41f257e9-9688-4944-9bf6-28cda1c3fa1f",
  "title": "Test Reward",
  "prompt": "",
  "inputRequired": false,
  "backgroundColor": "#63D0A9",
  "enabled": true,
  "paused": true,
  "subOnly": false
}
```

#### RewardDeleted
```json
{
  "dateTime": "2022-01-31T03:18:07.6679489Z",
  "channelId": 00000000,
  "cost": 42,
  "rewardId": "d52a0894-586e-4943-9027-385e8ea04f79",
  "title": "Test Reward",
  "prompt": "",
  "inputRequired": false
}
```

#### CommunityGoalContribution
```json
{
  "dateTime": "",
  "channelId": 0,
  "id": "",
  "title": "",
  "description": "",
  "inStock": true,
  "amount": 0, /* total amount required to complete goal */
  "contributed": 0, /* how much has been contributed so far */
  "duration": 0,
  "startedAt": "",
  "endedAt": "",
  "daysLeft": 0,
  "userId": 00000000,
  "userName": "<username>",
  "displayName": "<user's display name>",
  "userContributed": 0, /* hopw much the user contributed */
  "userStreamContributed": 0, /* hopw much the user contributed this stream */
  "userTotalContributed": 0, /* hopw much the user contributed for the entire goal */
}
```

#### CommunityGoalEnded
```json
{
  "dateTime": "",
  "channelId": 0,
  "id": "",
  "title": "",
  "description": "",
  "inStock": true,
  "amount": 0, /* total amount required to complete goal */
  "contributed": 0, /* how much has been contributed so far */
  "duration": 0,
}
```

### Tab {.tabset}
#### PollCreated
```json
{
  "dateTime": "2022-01-30T22:20:28.5021247-05:00",
  "channelId": 00000000,
  "type": 1,
  "id": "6e3b2f5b-39f1-4b09-b9aa-9937a289571b",
  "title": "Test Poll",
  "startedAt": "2022-01-31T03:20:28.5218414Z",
  "duration": 60,
  "settings": {
    "multi_choice": {
      "is_enabled": true
    },
    "subscriber_only": {
      "is_enabled": false
    },
    "subscriber_multiplier": {
      "is_enabled": false
    },
    "bits_votes": {
      "cost": 0,
      "is_enabled": false
    },
    "channel_points_votes": {
      "cost": 0,
      "is_enabled": false
    }
  },
  "choices": [
    {
      "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
      "title": "Option 1",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    },
    {
      "choice_id": "f995c9fb-47ef-41e3-aeab-33ed5b2083e2",
      "title": "Option 2",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    }
  ],
  "votes": {
    "total": 0,
    "base": 0,
    "bits": 0,
    "channel_points": 0
  },
  "tokens": {
    "bits": 0,
    "channel_points": 0
  },
  "totalVotes": 0,
  "remainingDurationMilliseconds": 59984
}
```

#### PollUpdated
```json
{
  "dateTime": "2022-01-30T22:20:35.2286411-05:00",
  "channelId": 00000000,
  "type": 2,
  "id": "6e3b2f5b-39f1-4b09-b9aa-9937a289571b",
  "title": "Test Poll",
  "startedAt": "2022-01-31T03:20:28.5218414Z",
  "duration": 60,
  "settings": {
    "multi_choice": {
      "is_enabled": true
    },
    "subscriber_only": {
      "is_enabled": false
    },
    "subscriber_multiplier": {
      "is_enabled": false
    },
    "bits_votes": {
      "cost": 0,
      "is_enabled": false
    },
    "channel_points_votes": {
      "cost": 0,
      "is_enabled": false
    }
  },
  "choices": [
    {
      "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
      "title": "Option 1",
      "votes": {
        "total": 1,
        "base": 1,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 1
    },
    {
      "choice_id": "f995c9fb-47ef-41e3-aeab-33ed5b2083e2",
      "title": "Option 2",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    }
  ],
  "votes": {
    "total": 1,
    "base": 1,
    "bits": 0,
    "channel_points": 0
  },
  "tokens": {
    "bits": 0,
    "channel_points": 0
  },
  "totalVotes": 1,
  "remainingDurationMilliseconds": 53240
}
```

#### PollCompleted
```json
{
  "endedAt": "2022-01-31T03:21:28.5218414Z",
  "winningChoice": {
    "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
    "title": "Option 1",
    "votes": {
      "total": 1,
      "base": 1,
      "bits": 0,
      "channel_points": 0
    },
    "tokens": {
      "bits": 0,
      "channel_points": 0
    },
    "total_voters": 1
  },
  "dateTime": "2022-01-30T22:21:28.8137307-05:00",
  "channelId": 00000000,
  "type": 4,
  "id": "6e3b2f5b-39f1-4b09-b9aa-9937a289571b",
  "title": "Test Poll",
  "startedAt": "2022-01-31T03:20:28.5218414Z",
  "duration": 60,
  "settings": {
    "multi_choice": {
      "is_enabled": true
    },
    "subscriber_only": {
      "is_enabled": false
    },
    "subscriber_multiplier": {
      "is_enabled": false
    },
    "bits_votes": {
      "cost": 0,
      "is_enabled": false
    },
    "channel_points_votes": {
      "cost": 0,
      "is_enabled": false
    }
  },
  "choices": [
    {
      "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
      "title": "Option 1",
      "votes": {
        "total": 1,
        "base": 1,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 1
    },
    {
      "choice_id": "f995c9fb-47ef-41e3-aeab-33ed5b2083e2",
      "title": "Option 2",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    }
  ],
  "votes": {
    "total": 1,
    "base": 1,
    "bits": 0,
    "channel_points": 0
  },
  "tokens": {
    "bits": 0,
    "channel_points": 0
  },
  "totalVotes": 1,
  "remainingDurationMilliseconds": 0
}
```

### Tab {.tabset}
#### PredictionCreated
```json
{
  "outcomes": [
    {
      "id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    },
    {
      "id": "b26ab426-03c0-46a7-a109-313b8b1cda7a",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "dateTime": "2022-01-30T22:22:08.8207639-05:00",
  "channelId": 000000,
  "type": 1,
  "status": 1,
  "id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:22:08.8386896Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<username of creator>"
  },
  "predictionWindow": 60
}
```

#### PredictionUpdated
```json
{
  "outcomes": [
    {
      "id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
          "outcome_id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:22:52.1304709Z",
          "updated_at": "2022-01-31T03:22:52.1304709Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "b26ab426-03c0-46a7-a109-313b8b1cda7a",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "dateTime": "2022-01-30T22:22:53.2067849-05:00",
  "channelId": 00000000,
  "type": 2,
  "status": 1,
  "id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:22:08.8386896Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```

#### PredictionCompleted
```json
{
  "outcomes": [
    {
      "id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
          "outcome_id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:23:15.2948659Z",
          "updated_at": "2022-01-31T03:23:15.2948659Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "d9bf57ec-3817-458b-8728-f7d81e8abc51",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "winningOutcomeId": "8c0c876a-4c43-42eb-aee6-6dd787434610",
  "winningOutcome": {
    "id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
    "color": "BLUE",
    "title": "Outcome 1",
    "total_points": 10,
    "total_users": 1,
    "top_predictors": [
      {
        "event_id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
        "outcome_id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
        "channel_id": 00000000,
        "points": 10,
        "predicted_at": "2022-01-31T03:23:15.2948659Z",
        "updated_at": "2022-01-31T03:23:15.2948659Z",
        "user_id": 00000000,
        "user_display_name": "<user's display name>"
      }
    ]
  },
  "dateTime": "2022-01-30T22:23:25.8367758-05:00",
  "channelId": 00000000,
  "type": 2,
  "status": 4,
  "id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:23:07.8904015Z",
  "endedAt": "2022-01-31T03:23:25.1085385Z",
  "lockedAt": "2022-01-31T03:23:22.8303546Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "endedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "lockedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```

#### PredictionCanceled
```json
{
  "outcomes": [
    {
      "id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
          "outcome_id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:22:52.1304709Z",
          "updated_at": "2022-01-31T03:22:52.1304709Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "b26ab426-03c0-46a7-a109-313b8b1cda7a",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "dateTime": "2022-01-30T22:23:04.5190145-05:00",
  "channelId": 0000000,
  "type": 2,
  "status": 6,
  "id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:22:08.8386896Z",
  "endedAt": "2022-01-31T03:23:03.618273Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "endedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```

#### PredictionLocked
```json
{
  "outcomes": [
    {
      "id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
          "outcome_id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:23:15.2948659Z",
          "updated_at": "2022-01-31T03:23:15.2948659Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "d9bf57ec-3817-458b-8728-f7d81e8abc51",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "winningOutcomeId": "00000000-0000-0000-0000-000000000000",
  "dateTime": "2022-01-30T22:23:22.7880889-05:00",
  "channelId": 00000000,
  "type": 2,
  "status": 2,
  "id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:23:07.8904015Z",
  "lockedAt": "2022-01-31T03:23:22.8303546Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "lockedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```

# Streamlabs
These are the events that are broadcast from Streamlabs events.

### Tab {.tabset}
#### Donation
```json
{
  "from": "John",
  "amount": 74,
  "formattedAmount": "$74.00",
  "currency": "USD",
  "message": "This is a test donation for $74.00.",
  "isTest": true
}
```
#### Merchandise
```json
{
  "from": "John",
  "product": "T-shirt",
  "message": "This is a test merch",
  "image": "https://uploads.twitchalerts.com/000/105/166/207/891265-mockup-152840970714082-0.png",
  "isTest": true
}
```

# Application
These are the events **Streamer.bot** broadcasts when changes are made to Actions
### Tab {.tabset}
#### Added
```json
{
  "id": "9ed46f4e-a76b-4a1a-92b7-0a12a78a2c3a",
  "name": "Test Action",
  "group": "",
  "enabled": true
}
```

#### Updated
```json
{
  "id": "9ed46f4e-a76b-4a1a-92b7-0a12a78a2c3a",
  "name": "Test Action",
  "group": "Group",
  "enabled": true
}
```

#### Deleted
```json
{
  "id": "9ed46f4e-a76b-4a1a-92b7-0a12a78a2c3a",
  "name": "Test Action",
  "group": "Group",
  "enabled": true
}
```

# Command
### Tab {.tabset}
#### Message
```json
{
  "command": "!bots",
  "counter": 1,
  "userCounter": 1,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 4
  }
}
```

#### Whisper
```json
{
  "command": "!bots",
  "counter": 1,
  "userCounter": 1,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 4
  }
}
```

#### MessageCooldown
```json
{
  "command": "!bots",
  "cooldownLeft": 11,
  "globalCooldownLeft": 11,
  "userCooldownLeft": 0,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": false,
    "role": 1
  }
}
```

# Speech To Text
### Tab {.tabset}
#### Dictation
```json
{
  "text": "",
  "confidence": 0.0
  "alternatives": [
    {
      "text": "",
      "confidence": 0.0
    }
	]
}
```

#### Command
```json
{
  "text": "",
  "confidence": 0.0
  "alternatives": [
    {
      "text": "",
      "confidence": 0.0
    }
	]
}
```

# File Watcher
### Tab {.tabset}
#### Changed
Only `lines` or `data` will exist for a changed event, not both.
```json
{
  "fullPath": "", /* full path to the file that changed */
  "fileName": "", /* file name of the file that changed */
  "name": "", /* file name without extension of the file that changed */
  "lines": [ /* list of string of the contents of the file, line by line, if it has not been parsed as a json */
  ],
  "data": { /* json parsed contents of file, only top level key value pairs */
    "key": "value"
  }
}
```

#### Created
```json
{
  "fullPath": "", /* full path to the file that changed */
  "fileName": "", /* file name of the file that changed */
  "name": "", /* file name without extension of the file that changed */
}
```

#### Deleted
```json
{
  "fullPath": "", /* full path to the file that changed */
  "fileName": "", /* file name of the file that changed */
  "name": "", /* file name without extension of the file that changed */
}
```

# Quote
> These events are currently not broadcast, will be updated in a future version
{.is-danger}

* QuoteAdded
* QuoteShow
{.grid-list}

# Websocket Client
> These events are currently not broadcast, will be updated in a future version
{.is-danger}

* WebsocketClientOpen
* WebsocketClientClose
* WebsocketClientMessage
{.grid-list}


# StreamElements
### Tabs {.tabset}
#### Tip
```json
{
  "id": "f11cfa360fd44555b99d41e0d277f45e",
  "username": "<username of tipper as entered on streamelements>",
  "amount": 74,
  "currency": "USD",
  "message": "This is a test message",
  "isTest": false
}
```

# Websocket Custom Server
> These events are currently not broadcast, will be updated in a future version
{.is-danger}

* WebsocketCustomServerOpen
* WebsocketCustomServerClose
* WebsocketCustomServerMessage
{.grid-list}

# Misc
### Tabs {.tabset}
#### TimedAction
```json
{
  "id": "6d55b50d-8061-40fc-b988-da88f21b83bc",
  "name": "Test",
  "counter": 1
}
```

#### PyramidSuccess
```json
{
  "total": 4,
  "width": 3,
  "emote": "nate121Heart",
  "user": {
    "id": 0000000,
    "login": "<user name>",
    "display_name": "<user's display name>",
    "subscribed": true,
	  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  }
}
```

#### Custom
There is no fixed JSON format for data, as it is custom sent via the C# method.

# Donor Drive
### Tabs {.tabset}
#### Donation
```json
{
  "donation": {
    "displayName": "",
    "donorId": "",
    "links": {
      "recipient": ""
    },
    "eventId": 00000,
    "createdDateUtc": "",
    "recipientName": "",
    "message": "",
    "participantId": 00000,
    "amount": 0.0,
    "avatarImageUrl": "",
    "teamId": 000000,
    "donationId": ""
  }
}
```

#### Profile Updated
```json
{
  "profile": {
    "fundraisingGoal": 0.0,
    "eventName": "",
    "links": {
      "recipient": ""
    },
    "eventId": 00000,
    "sumDonations": 0.0,
    "createdDateUtc": "",
    "numAwardedBadges": 0,
    "captainDisplayName": "",
    "avatarImageUrl": "",
    "teamId": 00000,
    "sumPledges": 0.0,
    "numDonations": 0
  }
}
```

# Raw
### Tabs {.tabset}
#### Action
```json
{
  "id": "cc8a2cd1-eb33-45b0-9f16-f752abe6fbff",
  "name": "PyramidSuccess",
  "arguments": {
    "totalPyramids": 4,
    "pyramidWidth": 3,
    "pyramidEmote": "nate121Heart"
  },
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  }
}
```

#### SubAction
```json
{
  "parentId": "cc8a2cd1-eb33-45b0-9f16-f752abe6fbff",
  "parentName": "PyramidSuccess",
  "type": 10,
  "id": "29e34a9b-5856-4133-85eb-f812597c4d89",
  "name": "Message (Nice %pyramidWidth%-width %pyramidEmote%…)",
  "arguments": { /* arguments can and will vary depending on the type of subaction */
    "totalPyramids": 4,
    "pyramidWidth": 3,
    "pyramidEmote": "nate121Heart",
    "user": "<user's display name>", /* user who triggered action */
    "userName": "<username>", /* user who triggered action */
    "userId": 00000000, /* user who triggered action */
    "isSubscribed": true,
    "isModerator": false,
    "isVip": false,
    "broadcastUser": "nate1280",
    "broadcastUserName": "nate1280",
    "broadcastUserId": 00000000,
    "broadcasterIsAffiliate": true,
    "broadcasterIsPartner": false,
    "randomUser0": "<user's display name>",
    "randomUserName0": "<username>",
    "randomUserId0": 00000000,
    "randomUser1": "<user's display name>",
    "randomUserName1": "<username>",
    "randomUserId1": 00000000,
    "randomUser2": "<user's display name>",
    "randomUserName2": "<username>",
    "randomUserId2": 00000000
  },
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  }
}
```

### End Tab {.tabset}

---
- [<i class="mdi mdi-chevron-left"></i> **WebSocket Requests *Go Back***](/Servers-Clients/WebSocket-Server)
- [<i class="mdi mdi-upload-network primary--text"></i> **WebSocket Requests *Reference of all requests you can make to the Streamer.bot WebSocket API***](/Servers-Clients/WebSocket-Server/Events)
{.btn-grid .my-5}
