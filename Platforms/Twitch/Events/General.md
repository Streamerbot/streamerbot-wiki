---
title: General
description: Twitch Events Reference
published: true
date: 2023-03-16T13:03:11.836Z
tags: twitch, events
editor: markdown
dateCreated: 2021-08-25T21:31:30.022Z
---

The `General` tab covers 10 Simple events and a single action can be assigned to each; 

# Events

Name | Description
----:|:------------
`Follows` | When someone follows your channel
`Whispers` | When someone whispers your broadcaster account directly | If the whisper itself contains a command, the command action will trigger instead of this generic one
`Present Viewers` | Triggers automatically every 5 minutes | Populates a dictionary of special variables for each user in chat
`Chat Message` | When any chat message is recieved that does not contain a command | If the message contains a command, the command action will trigger instead of this generic one
`Announcement` | When an announcement is made is chat
`First Words` | The first message a particular user sends to chat within the `Auto Reset` window | This runs alongside the `Chat Message` event so if you have actions set for both, they will both run
`Message Deleted` | When a message gets deleted from chat | When this event is triggered, the `message` argument will be populated with the message being deleted
`User Timed Out` | When a user present in chat gets timed out | This event will populate the `duration` argument with the time-out length
`User Banned` | When a user is banned from the channel | This action will trigger on any user being banned, however if the user has never been present in chat while Streamer.bot is running there will be no username data
`Ad Run` | When a commercial is triggered on your channel by any source
{.vars-table}

# Variables 
## Follows
Name | Description
----:|:------------
`isTest` | Boolean value indicating if the follow event came from the internal Test button <br> `True`/`False`
{.vars-table}

## Chat Message / Whispers & First Words
Name | Description
----:|:------------
`msgId` | Twitch's message ID 
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`isSubscribed` | Boolean value indicating the user's subscription status <br> `True`/`False`
`color` | Hex value of user's chat color <br> a random value will be selected if the user has not set one
`colorR` | Hex value for Red component of the `color` variable
`colorG` | Hex value for Green component of the `color` variable
`colorB` | Hex value for Blue component of the `color` variable
`message` | Message that was sent to chat
`emoteCount` | How many Twitch emotes were found
`emotes` | Comma Separated list of Twitch emotes found
`messageStripped` | The chat message with emotes stripped
`messageCheermotesStripped` | The chat message with cheer emotes stripped
`isHighlight` | Boolean for message highlight property <br> `True`/`False`
`bits` | Number of bits the message has
`isAction` | Boolean value indicating the message is a `/me` action <br> `True`/`False`
`isReply`| Boolean value indicating the message is a reply to another message <br> `True`/`False` 
`replyTo`| The username the message is replying to <br> Only populated is `isReply` is `True` 
`firstMessage` | Boolean value indicating the message is from a first time chatter in the channel <br> `True`/`False` *v0.1.8*{.version-badge}
{.vars-table}

## Present Viewers
Name | Description
----:|:------------
`isLive` | Boolean for current streaming status <br> `True`/`False` 
`isTest` | Boolean for if this is demo data or not <br> `True`/`False` 
`users` | A Dictionary list of usernames present in IRC chat <br> Each user present will get the following data
{.vars-table}

### User Dictionary
Name | Description
----:|:------------
`id` | The Numeric ID of this user
`userName` | The user name of this user
`display` | The display name of this user
`role` | The role of the user <br> 1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
`isSubscribed` | Boolean for this users subscription status <br> `True`/`False` 
{.vars-table}

### Live Variables 

If `isLive` is `True` the following variables will also be populated on each tick of the event:

Name | Description
----:|:------------
`title` | The current stream title
`gameID` | The ID of the category you are streaming
`gameName` | The name of the category you are streaming
`viewerCount` | Viewer count at the time of the tick
`startedAt` | The time stamp when you started streaming
{.vars-table}

***

## Announcement

| Value | Description | Notes |
|------:|:-----------:|:------|
`announceColor` | The color of the announcement <br> `DEFAULT`, `BLUE`, `RED`, `ORANGE`, `PURPLE`
`message` | The announcement message
`messageStripped` | The announcement message without emotes
`emoteCount` | The number of emotes in the message
`emotes` | The emotes in the message, this is a List<> object
`badgeCount` | The number of badges for the user making the announcement
`badges` | The badges for the user making the announcement <br> This is a `List<>` object
{.vars-table}

> This also contains the user's picked color, and user's months subscribed
{.is-info}

***

## Message Deleted
Name | Description
----:|:------------
`message` | The message that was deleted from chat
{.vars-table}

## User Timed Out
Name | Description
----:|:------------
`duration` | The amount of time the user was timed out for
`user` | The user that was timed out 
{.vars-table}

## User Banned
Name | Description
----:|:------------
`user` | The user that was banned <br> This will not be populated if the user has never been present in chat
{.vars-table}

## Ad Run

Name | Description
----:|:------------
`adLength` | The length of the ad in seconds
`adScheduled` | If this ad was a scheduled ad <br> `True`/`False`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}