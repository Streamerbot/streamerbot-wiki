---
title: General
description: 
published: true
date: 2022-01-19T21:52:55.224Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:31:30.022Z
---

The `General` tab covers 8 Simple events and a single action can be assigned to each; `Follows` `Whispers` `Present Viewers` `Chat Message`, `First Words`, `Message Deleted`, `User Timed Out` and `User Banned`

![settings-events-general.png](/settings-events-general.png)

## Follows

When someone follows your channel, perform this [action](Actions)

## Whispers

If someone whispers you directly perform this action (unless the whisper itself contains a command)

## Present Viewers

This triggers every 5 minutes and populates a dictionary of [variables](/en/Variables#present-viewers) for each user in chat. These can be then be passed to this action

## Chat Message

Trigger this action for every message sent to chat

## First Words

Trigger this action for the first message a particular user sends to chat within the `Auto Reset` window

## Message Deleted

Trigger this action when a message gets deleted from chat

> When this event is triggered, the `message` argument will be populated with the message being deleted
{.is-info}


## User Timed Out

Trigger this action when a user present in chat gets timed out

This event will populate the `duration` argument with the time-out length

## User Banned

Trigger this action when a user is banned from the channel

> This action will trigger on any user being banned, however if the user has never been present in chat while Streamer.bot is running there will be no username data
{.is-warning}

