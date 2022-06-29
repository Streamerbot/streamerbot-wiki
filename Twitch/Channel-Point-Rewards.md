---
title: Channel Point Rewards
description: 
published: true
date: 2022-06-29T15:12:03.048Z
tags: twitch, channel-points
editor: markdown
dateCreated: 2021-08-25T21:31:18.137Z
---

# Overview

![Channel Point Rewards](/119644643-00af2100-be15-11eb-87c8-a271f08e41b8.png)

**Streamer.bot** can automatically execute [Actions](/Actions) when a Channel Point Reward is redeemed

When the `Broadcaster` account is connected, **Streamer.bot** will automatically pull a list of available rewards from the Twitch profile and actions can be assigned to them immediately. 

You can also `Add` and `Delete` rewards directly from the application. 

If a reward is created through **Streamer.bot**, the application will also have the ability to fully control that reward, otherwise most options will be unavailable.  This is a limitation of twitch and there is nothing **Streamer.bot** is able to do, to get around this.

# Guide

To create a new reward Right-Click in the empty space and click `Add`

![New Channel Point Reward](/119646229-d4949f80-be16-11eb-806f-8dca85bdce45.png)

### Title

The name of the reward

`Enabled` The reward is visible to the channel

`Paused` The reward can not be redeemed but can be seen if `Enabled` is also checked

### Cost

The number of channel points needed to redeem this reward

`User Input Required` This will show a text box to the user to allow them to enter a message. This can be read by [sub-actions](/Sub-Actions#main) with the `%rawInput%` variable

### Prompt

This is the text that will be displayed to the user before they confirm redemption to explain what will happen

`Background Colour` Sets the colour of the button

`Redemption Skips Queue` Tells the [action](/Actions) to ignore the `Blocking` flag on the [action queue](/Settings/General#action-queues) assigned to that action

`Max per stream` & `Max per User per Stream` Defines limits on how many times this reward can be redeemed in any one stream

`Global Cooldown` Defines the miniimum time in seconds before this reward can be redeemed again by anyone

### Counters

Actions in **Streamer.bot** have per-session and per-command variables `%counter%`, and `%userCounter%` that records how many times that channel reward has been used. 

By default this clears when the application is closed but the following options will save the counts to a file so they will persist between sessions

`Persist Counter` Will save the total number of executions for this command

`Persist per User Counter` Will save details of how often each user has executed this command

### Action

`Action` Defines the action that will be executed when the reward is redeemed
