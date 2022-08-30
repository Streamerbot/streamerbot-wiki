---
title: Credits
description: 
published: true
date: 2022-07-09T19:58:59.684Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:30.409Z
---

Define the events you wish to monitor here 

The script from SLCB has finally been brought over into CPH. It can be configured to include only certain events and information, and the resulting information can be retrieved by using a command on the websocket server.

This feature will likely be evolving, so consider this a first pass implementation to get something in place, it should be feature parity (and then some) with the script.  The only thing I believe that is missing are top gift subs, but I unfortunately do not track this information, and there is no way to get this from twitch that I can see.  Adding new features and capabilities to this is always possible.

![Credits Settings](/119622018-ac00ab80-bdfe-11eb-8207-d08f42b43e87.png)

Credits uses websockets to dynamically build lists of viewers that participate in chat, moderate the channel, donate bits, subscribe etc.

This can then be used as a Browser source in OBS for an Outtro Scene to thank your community

***

There are 2 new websocket server requests to be used when dealing with requests, as follows:

## GetCredits
```json
{
  "request": "GetCredits",
  "id": "someid"
}
```

When sending the above request to `CPH` you will get back a response that looks like, some keys may not be present depending on how you have it configured, and what events/etc come through.

```json
{
  "id": "credits",
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
  "TopChannelRewards": [],
  "status": "ok"
}
```

To get you started, you can use the following javascript within html to connect to the websocket and get the data. A more robust example will be posted in the nook at some point I hope.

```js
// Create WebSocket connection.
const socket = new WebSocket('ws://localhost:8080');

socket.onmessage = function (event) {
    console.log('Message from server: ', event.data);
	var msg = JSON.parse(event.data);
	if (msg["id"] == "credits")
	{
		// msg now contains all the data you need to work on
		
		// close the socket
		socket.close();
	}
}

socket.onopen = function (event) {
	var msg = { "request": "GetCredits", "id": "credits" };
	socket.send(JSON.stringify(msg));
};
```

## TestCredits
```json
{
  "request": "TestCredits",
  "id": "someid"
}
```
When sending the above request to `CPH` you will get back a response that is filled with data filled from users that CPH has seen, and will take on the format from GetCredits

## ClearCredits
```json
{
  "request": "ClearCredits",
  "id": "someid"
}
```