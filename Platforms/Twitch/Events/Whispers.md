---
title: Whispers
description: Twitch Events Reference
published: true
date: 2023-03-16T12:59:56.222Z
tags: 
editor: markdown
dateCreated: 2022-12-18T18:39:26.021Z
---

## Variables
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

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}