---
title: Chat Messages, Whispers, and First Words Events
description: Twitch Events Reference
published: true
date: 2022-08-23T21:29:37.884Z
tags: 
editor: markdown
dateCreated: 2022-08-23T21:28:11.564Z
---

## Variables
| Name | Description | Notes |
|-----:|:------------|:------|
`msgId` | Twitch's message ID 
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`isSubscribed` | Boolean value indicating the user's subscription status |  `True`/`False`
`color` | Hex value of user's chat color | a random value will be selected if the user has not set one
`colorR` | Hex value for Red component of the `color` variable
`colorG` | Hex value for Green component of the `color` variable
`colorB` | Hex value for Blue component of the `color` variable
`message` | Message that was sent to chat
`emoteCount` | How many Twitch emotes were found
`emotes` | Comma Separated list of Twitch emotes found
`messageStripped` | The chat message with emotes stripped
`messageCheermotesStripped` | The chat message with cheer emotes stripped
`isHighlight` | Boolean for message highlight property | `True`/`False`
`bits` | Number of bits the message has
`isAction` | Boolean value indicating the message is a `/me` action | `True`/`False`
`isReply`| Boolean value indicating the message is a reply to another message | `True`/`False` 
`replyTo`| The username the message is replying to | Only populated is `isReply` is `True` 
`firstMessage` | Boolean value indicating the message is from a first time chatter in the channel | `True`/`False` <span style="color:blue">*(0.18+)*</span>
{.vars-table}



| Name | Description |
|-----:|:------------|
`user` | The user that followed the broadcaster
`userName` | The login name of the user that followed the broadcaster
`userId` | Unique user identifier
`userType` | pecifies which streaming service the triggering user is coming from *v0.1.8+*{.version-badge} <br> `twitch` or `youtube`
`isSubscribed` | Boolean value indicating the sender's subscription status <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
`eventSource` | pecifies which streaming service the triggering event is coming from *v0.1.8+*{.version-badge} <br> `twitch` or `youtube`
{.vars-table}

> This will also include all the [Broadcaster Variables](/en/Variables/Broadcaster)
{.is-success}