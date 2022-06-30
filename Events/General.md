---
title: General
description: 
published: true
date: 2022-06-30T17:36:17.655Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:31:30.022Z
---

The `General` tab covers 10 Simple events and a single action can be assigned to each; `Follows`, `Whispers`, `Present Viewers`, `Chat Message`, `Announcement`, `First Words`, `Message Deleted`, `User Timed Out`, `User Banned` and `Ad Run`

![twitch-events-general-0110.png](/twitch-events-general-0110.png)

Event | Description | Notes
---|---
`Follows` | When someone follows your channel, perform this [action](Actions)
`Whispers` | When someone whispers you directly perform this action | If the whisper itself contains a command, the command action will trigger instead of this generic one
`Present Viewers` | Triggers automatically every 5 minutes | Populates a dictionary of [variables](/en/Variables#present-viewers) for each user in chat
`Chat Message` | When any chat message is recieved that does not contain a command | If the message contains a command, the command action will trigger instead of this generic one
`Announcement` | When an announcement is made is chat
`First Words` | The first message a particular user sends to chat within the `Auto Reset` window | This runs alongside the `Chat Message` event so if you have actions set for both, they will both run
`Message Deleted` | When a message gets deleted from chat | When this event is triggered, the `message` argument will be populated with the message being deleted
`User Timed Out` | When a user present in chat gets timed out | This event will populate the `duration` argument with the time-out length
`User Banned` | When a user is banned from the channel | This action will trigger on any user being banned, however if the user has never been present in chat while Streamer.bot is running there will be no username data
`Ad Run` | When a commercial is triggered on your channel by any source


## Variables 
## {.tabset}
### Follow
Variable | Description | Notes
---------:|------------
`isTest` | Boolean value indicating if the follow event came from the internal Test button | `True`/`False` 

### [Chat Message](/en/Events/General) / Whispers & First Words

Variable | Description| Notes
---------:|------------|---
`msgId` | Twitch's message ID 
`role` | What role the user has `(1-4)` | 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`isSubscribed` | Boolean value indicating the user's subscription status |  `True`/`False`
`color` | User's color (if they have chosen one or a random one if not)
`colorR` | Red value of the `color` variable
`colorG` | Green value of the `color` variable
`colorB` | Blue value of the `color` variable
`message` | Message that was sent to chat
`emoteCount` | How many Twitch! emotes were found
`emotes` | Comma Separated list of Twitch! emotes found
`messageStripped` | The chat message with emotes stripped
`messageCheermotesStripped` | The chat message with cheer emotes stripped
`isHighlight` | Boolean for message highlight | `True`/`False`
`bits` | Number of bits the message has
`isAction` | Boolean value indicating the message is a `/me` action | `True`/`False`
`isReply`| Boolean value indicating the message is a reply to another message | `True`/`False` 
`replyTo`| if `isReply` is True, populates the username the message is replying to
`firstMessage` | Boolean value indicating the message is from a first time chatter in the channel | `True`/`False` <span style="color:blue">*(0.18+)*</span>

### [Announcement](/en/Twitch/Announcement)

| Value | Description | Notes
|   ---:|-------------|
| `announceColor` | The color of the announcement | `DEFAULT`, `BLUE`, `RED`, `ORANGE`, `PURPLE`
| `message` | The announcement message
| `messageStripped` | The announcement message without emotes
| `emoteCount` | The number of emotes in the message
| `emotes` | The emotes in the message, this is a List<> object
| `badgeCount` | The number of badges for the user making the announcement
| `badges` | The badges for the user making the announcement | This is a `List<>` object

> This also contains the user's picked color, and user's months subscribed
{.is-info}

### [Message Deleted](/en/Events/General)

| Value | Description | Notes
|   ---:|-------------|
| `message` | The message that was deleted from chat

### [User Timed Out](/en/Events/General)

| Value | Description | Notes
|   ---:|-------------|
| `duration` | The amount of time the user was timed out for
| `user` | The user that was timed out 

### [User Banned](/en/Events/General)

| Value | Description | Notes
|   ---:|-------------|
| `user` | The user that was banned | This will not be populated if the user has never been present in chat

### Ad Run

| Value | Description | Notes
|   ---:|-------------|


