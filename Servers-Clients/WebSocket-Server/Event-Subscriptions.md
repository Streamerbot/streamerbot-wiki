---
title: Event Subscription
description: 
published: true
date: 2022-09-09T13:45:06.920Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:59.892Z
---

With [Version 0.0.52](/en/Changelogs/Archives/Version-0052), I have changed how events are broadcasted to clients connected to the WebSocket server.  Each client, after connecting will need to send a `Subscribe` command to the server with the events it would like to receive.  A sample request for subscribing is below, and all the events that are available is below that.  You can also always call `GetEvents` to get all the events you can subscribe to.

```json
{
    "request": "Subscribe",
    "events": {
        "Twitch": ["Cheer"]
    },
    "id": "<your id>"
}
```

These are the available events you can subscribe to.
```json
{
    "events": {
        "general": [
            "Custom"
        ],
        "twitch": [
            "Follow",
            "Cheer",
            "Sub",
            "ReSub",
            "GiftSub",
            "GiftBomb",
            "Raid",
            "HypeTrainStart",
            "HypeTrainUpdate",
            "HypeTrainLevelUp",
            "HypeTrainEnd",
            "RewardRedemption",
            "RewardCreated",
            "RewardUpdated",
            "RewardDeleted",
            "CommunityGoalContribution",
            "CommunityGoalEnded",
            "StreamUpdate",
            "Whisper",
            "FirstWord",
            "SubCounterRollover",
            "BroadcastUpdate",
            "StreamUpdateGameOnConnect",
            "PresentViewers",
            "PollCreated",
            "PollUpdated",
            "PollCompleted",
            "PredictionCreated",
            "PredictionUpdated",
            "PredictionCompleted",
            "PredictionCanceled",
            "PredictionLocked",
            "ChatMessage"
        ],
        "streamlabs": [
            "Donation",
            "Merchandise"
        ],
        "speechToText": [
            "Dictation",
            "Command"
        ],
        "command": [
            "Message",
            "Whisper"
        ],
        "fileWatcher": [
            "Changed",
            "Created",
            "Deleted"
        ],
        "quote": [
            "Added",
            "Show"
        ],
        "misc": [
            "TimedAction",
            "PyramidSuccess"
        ],
        "raw": [
            "Action",
            "SubAction"
        ],
        "websocketClient": [
            "Open",
            "Close",
            "Message"
        ],
        "streamElements": [
            "Tip"
        ]
    }
}
```