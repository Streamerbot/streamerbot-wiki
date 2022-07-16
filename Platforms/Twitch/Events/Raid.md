---
title: Raids
description: Twitch Events Reference
published: true
date: 2022-07-16T15:42:38.732Z
tags: twitch, events
editor: markdown
dateCreated: 2022-01-03T14:40:22.386Z
---

# Overview

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
Streamer.bot will detect the destination username and populate the following [Variables](/en/Variables#sending-a-raid) that can be used to drive on screen elements and chat messages

### Cancel

If for any reason the raid is cancelled, this action will trigger. It can be used to reset any elements initialised by the `Start` event or kick off something completely new

### Send

This event triggers after the raid has transferred your users to the new channel. This is useful for cleanup actions such as turning off lights, stopping streaming state etc.

# Variables

## Incoming

Variable | Description
---------:|------------
`user` | The user who is raiding the channel
`viewers` | Number of viewers in the raid as reported by Twitch
`raiderNames` | A comma separated list of display names of users in the raid, any names in groups that have been marked as bots will be excluded.

> **%raiderNames%** is a best guess effort in determining who came along in the raid, there is currently no mechanism from Twitch that provides this information during a raid, so a few extra API calls are made to "guess" at this list
{.is-info}


## Sending a Raid

Variable | Description
---------:|------------
`raidUser` | Target user's display name
`raidUserName` | Target user's Twitch! login name
`raidUserId` | Target user's Twitch! ID
`raidUserProfileImageURL` | Target user's Twitch! profile image
`raidUserProfileImageEscaped` | Target user's Twitch! profile imagewith escaped characters

> This event relies on a Twitch PubSub message, and it seems the profile image can sometimes be 70x70, or 300x300.  This has been updated with `0.1.4` to replace the 70x70 with 300x300, so you can get the full size profile image.  The test button, defaults to a 300x300 size profile image, as it makes another call to get this information.
{.is-info}