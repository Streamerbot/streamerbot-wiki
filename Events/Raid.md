---
title: Raids
description: Events for Incoming and Outgoing Raids
published: true
date: 2022-06-27T01:07:32.136Z
tags: 
editor: markdown
dateCreated: 2022-01-03T14:40:22.386Z
---

# Raids

Streamer.bot can handle alerts for both an incoming and outgoing raid from the channel, the actions for both can be configured on the `Raid` tab

![raid.png](/raid.png)


## Incoming Raids

### Generic

The `Generic` action is run on any incoming raid that does not match a defined range

### Viewer Ranges

If you would like a special alert to override the generic action for incoming raids of specific sizes you can define the ranges and the Action to assign to them here.
> 
> You can add as many ranges as you like but there is no way to define an unlimited upper bound, so if you are using ranges make sure your largest one has a Max value that will be big enough for your needs, otherwise Streamer.bot will default back to the Generic action
{.is-info}


## Outgoing Raids

Streamer.bot can also perform actions when you are preparing to raid at the end of your stream and provides 3 events it can listen to: `Start`, `Cancel`, `Send`

### Start

This triggers when the Raid command is first sent either from a `/raid` command in chat or from the Twitch! dashboard. 
Streamer.bot will detect the destination username and populate the following [Variables](en/Variables#sending-a-raid) that can be used to drive on screen elements and chat messages

### Cancel

If for any reason the raid is cancelled, this action will trigger. It can be used to reset any elements initialised by the `Start` event or kick off something completely new

### Send

This event triggers after the raid has transferred your users to the new channel. This is useful for cleanup actions such as turning off lights, stopping streaming state etc.