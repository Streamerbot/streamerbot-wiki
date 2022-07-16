---
title: Cheers
description: Twitch Events Reference
published: true
date: 2022-07-16T15:51:43.934Z
tags: twitch, events
editor: markdown
dateCreated: 2021-08-26T02:31:57.116Z
---

# Overview

In this tab you can assign actions to your twitch cheer events so every time you get bits cheered on your twitch channel, the action will run but here is the fun part you can have variations for a specified ranges. 

So to do this open your Streamer.bot and navigate to the `Cheers` tab. You will find this in `Settings` the click `Events` now click the `Cheers` it should now look like the screenshot displayed below. 

![twitch_cheers.png](/twitch_cheers.png)

You can test this event out with the test button displayed in the tab 

As mentioned above you can set a specific action to run when a specified range is set. To do this on the right of this tab window you will see a section called `Add New Range`. Here you will need to specify the range you want with a Min value and a Max value and you will also need to set the state for this range. (more information on the types/states below) once you have done this click the `Add` button. Streamer bot now as a record of this range which can now be selected in cheer ranges section here you need to select your new range and assign and action to this. Once you have done this you just repeat for all the other ranges. 

![twitch_cheers_range.png](/twitch_cheers_range.png)


## Cheer Types / States

There are 3 cheer types. Generic (Either), Generic (Anon) for Anonymous Cheers and Generic (Non-Anon) is for those public cheerers.

#### Generic (Either) Type / State 

Any action assigned to this type will be triggered for both anonymous and non-anonymous cheerers and those that have not been set up for a specific range. 

> This event is triggered if the bits hit the max value in the Cheer range. So it's suggested to have max range + 1 set. i.e 100 + 1 = max value (101) 
{.is-info}


#### Generic (Anon) Type / State 

Any action you have assign to this type is for the anonymous cheerers only. This action will not run if the cheerer has NOT selected the option to be anonymous.

#### Generic (Non-Anon) Type / State

Any action you assign to this type will be triggered when a non-anonymous cheer is given. This action will not run if the cheerer is anonymous.


# Variables

| Name | Description |
|-----:|:------------|
`msgId` | Twitch's message ID 
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`isSubscribed` | Boolean value indicating the user's subscription status <br>  `True`/`False`
`color` | User's color (if they have chosen one or a random one if not)
`colorR` | Red value of the `color` variable
`colorG` | Green value of the `color` variable
`colorB` | Blue value of the `color` variable
`message` | Message that was sent to chat
`emoteCount` | How many Twitch! emotes were found
`emotes` | Comma Separated list of Twitch! emotes found
`messageStripped` | The chat message with emotes stripped
`messageCheermotesStripped` | The chat message with cheer emotes stripped
`isHighlight` | Boolean for message highlight <br> `True`/`False`
`bits` | Number of bits the message has
`isAction` | Boolean value indicating the message is a `/me` action <br> `True`/`False`
`isReply`| Boolean value indicating the message is a reply to another message <br> `True`/`False` 
`replyTo`| if `isReply` is True, populates the username the message is replying to
`firstMessage` | Boolean value indicating the message is from a first time chatter in the channel <br> `True`/`False` *v0.1.8+*{.version-badge}
`cheerEmotes` | List of cheermotes found in the message
`anonymous` | Boolean value indicating if the cheer was anonymous <br> `True`/`False`
`cheerEmoteCount` | How many Twitch! cheer emotes were found
{.vars-table}

