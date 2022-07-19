---
title: WebSocket Server Requests
description: Documentation of requests that can be made to the Streamer.bot WebSocket Server
published: true
date: 2022-07-19T20:57:52.501Z
tags: websocket
editor: markdown
dateCreated: 2021-08-25T21:37:16.673Z
---

Requests can be made to the server, in JSON format, the basic format for a request is as follows:
```json
{
  "request": "<request>",
  "id": "<id>"
}
```




## Subscribe
This request is required to enable you to listen to events

### Tab {.tabset}
#### Request

```json
{
  "request": "Subscribe",
  "id": "<message id>",
  "events": {
    "<event category>": [
      "<event name>",
  		"<event name>",
  		"...",
		]
	},
}
```

#### Example

```json
{
  "request": "Subscribe",
  "id": "my-subscribe-events-id",
  "events": {
    "Twitch": [
      "Follow",
      "Cheer",
      "Sub",
      "Resub",
      "GiftSub",
      "GiftBomb"
		]
	},
}
```

## UnSubscribe
This request allows you to unsubscribe from any message events you are currently subscribed to

### Tab {.tabset}
#### Request

```json
{
  "request": "UnSubscribe",
  "id": "<message id>",
  "events": {
    "<event category>": [
      "<event name>",
  		"<event name>",
  		"...",
		]
	},
}
```

#### Example

```json
{
  "request": "UnSubscribe",
  "id": "my-unsubscribe-events-id",
  "events": {
    "Twitch": [
      "Follow",
      "Cheer",
      "Sub",
      "Resub",
      "GiftSub",
      "GiftBomb"
		]
	},
}
```


## GetEvents
This request will get you a list of all events that may be emitted

### Tab {.tabset}
#### Request

```json
{
  "request": "GetEvents",
  "id": "<message id>",
}
```

#### Response

```json
{
  "id": "<message id>",
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
      "ChatMessage",
      "Host"
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
    ],
    "websocketCustomServer": [
      "Open",
      "Close",
      "Message"
    ],
    "application": [
      "ActionAdded",
      "ActionUpdated",
      "ActionDeleted"
    ]
  },
  "status": "ok"
}
```


## GetActions
This request will get you a list of all the actions you have configured in your Streamer.bot instance
### Tab {.tabset}
#### Request

```json
{
  "request": "GetActions",
  "id": "<message id>"
}
```

#### Response

```json
{
  "id": "<message id>",
  "count": 00,
  "actions": [
    {
      "id": "<action guid>",
      "name": "<action name>"
    },
  ],
  "status": "ok"
}
```

## DoAction
This request will trigger an action that you provide

### Tab {.tabset}
#### Request

```json
{
  "request": "DoAction",
  "action": {
    "id": "<guid>",
    "name": "<name>"
  },
  "args": {
    "key": "value",
  },
  "id": "<id>"
}
```

#### Response

If the action is not found, an error will be returned, if the action was dispatched it will return success.
```json
{
  "id": "<id>",
  "status": "ok"
}
```


## Examples
Example Javascript code for interacting with the WebSocket Server

### Tab {.tabset}
#### Connect

Code to connect - this function is ideally called directly / indirectly from onload 
```js
function connectws() {
	if ("WebSocket" in window) {
		const ws = new WebSocket("ws://localhost:8080/");
	}
}
```

#### Reconnect

Code to attempt to reconnect (after 10 seconds) when disconnected:
```js
ws.onclose = function() { 
  // "connectws" is the function we defined previously
  setTimeout(connectws, 10000);
};
```

#### Subscribe

Code to subscribe to events - In this example: Follows, Cheers, Subs, Resubs, Gift Subs and Gift Bombs.
```js
ws.onopen = function() {
  ws.send(JSON.stringify(
  	{ 
      "request": "Subscribe", 
      "events": {
        "Twitch": [
          "Follow",
          "Cheer",
          "Sub",
          "Resub",
          "GiftSub",
          "GiftBomb"
        ] 
      },
      "id": "123"
    }
  ));
}
```

Code to Handle the above messages when received from the server:
```js
ws.onmessage = function (event) {
  // grab message and parse JSON
  const msg = event.data;
  const wsdata = JSON.parse(msg);
  
  // check for events to trigger
  if (wsdata.event.source === 'Twitch') {
    if (wsdata.event.type === 'Sub' || wsdata.event.type === 'ReSub') {
      alert(`trigger sub event for ${wsdata.data.displayName}`);
    } else if (wsdata.event.type === 'GiftSub') {
      alert(`trigger Gift sub event for ${wsdata.data.recipientDisplayName}`);
    } else if (wsdata.event.type === 'GiftBomb') {
      if (wsdata.data.isAnonymous === false) {
        alert(`trigger gift bomb event for ${wsdata.data.displayName} ${wsdata.data.gifts} subs`);
      } else {
        alert(`trigger gift bomb event for Anonymous ${wsdata.data.gifts} subs`);
      }
    } else if (wsdata.event.type === 'Follow') {
      alert(`trigger follow event for ${wsdata.data.displayName}`);
    } else if (wsdata.event.type === 'Cheer') {
      alert(`trigger cheer event for ${wsdata.data.message.displayName} ${wsdata.data.message.bits}`);
    }
  }
};
```