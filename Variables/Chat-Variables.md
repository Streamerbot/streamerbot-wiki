---
title: Chat Variables
description: Variables reference
published: true
date: 2023-04-25T21:28:21.634Z
tags: 
editor: markdown
dateCreated: 2023-04-25T21:28:21.634Z
---

## Twitch
All user variables for Twitch{.subtitle}

Name | Description
----:|:------------
`msgId` | Twitch's message id.
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`.
`isSubscribed` | Boolean value indicating the user's subscription status. This variable can be be `True` or `False`.
`color` | Hex value of user's chat color <br> a random value will be selected if the user has not set one.
`colorR` | Hex value for Red component of the `color` variable.
`colorG` | Hex value for Green component of the `color` variable.
`colorB` | Hex value for Blue component of the `color` variable.
`message` | Message that was sent to chat.
`emoteCount` | How many Twitch emotes were found.
`emotes` | Comma Separated list of Twitch emotes found.
`messageStripped` | The chat message with emotes stripped.
`messageCheermotesStripped` | The chat message with cheer emotes stripped.
`isHighlight` | Boolean for message highlight property. This variable can be be `True` or `False`.
`isAction` | Boolean value indicating the message is a `/me` action. This variable can be be `True` or `False`.
`isReply`| Boolean value indicating the message is a reply to another message. This variable can be be `True` or `False`.
`replyTo`| The username the message is replying to. This variable is only populated is `isReply` is `True` 
`firstMessage` | Boolean value indicating the message is from a first time chatter in the channel. This variable can be be `True` or `False`.
{.vars-table}