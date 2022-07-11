---
title: Get User Info for Target
description: 
published: true
date: 2022-07-11T21:44:55.802Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:33:30.189Z
---

## Overview

![User Info](/122114131-d8ff1780-ce1a-11eb-85c5-bdea50941d8c.png)

This sub-action collates various data from a speciified Twitch! user and passes it to a number of [variables](/Variables) that other [Sub-Actions](/Sub-Actions) can use.

## Configuration

### Source Type
| Value | Description |
|------:|:------------|
User | User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
From Input | This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
Variable | Use the content of an existing [variable](Variables) as the target

### Variable

If you selected `Variable` as your **Source Type**, enter the name of the [variable](Variables) you would like to read in.
This can be any variable defined in a previous [sub-action](Sub-Actions) or could be an inherent function such as `randomUserName()`

## Variables
The following variables will be available after execution of this sub-action:

| Variable | Description |
|---------:|:------------|
`targetUser` | Display name of the target user
`targetUserName` | User name of the target user
`targetUserId` | User Id of the target user
`targetDescription` | The user's channel description
`targetDescriptionEscaped` | The user's channel description but URL encoded
`targetUserProfileImageUrl` | link to the 300x300 px PNG version of a user's twitch profile image
`targetUserProfileImageUrlEscaped` | The url to the user's profile image URL encoded
`targetUserType` | The type of user, `affiliate`, `partner` or empty for regular user
`targetIsAffiliate` | A boolean value indicating if the user is an affiliate
`targetIsPartner` | A boolean value indicating if the user is a partner
`targetIsSubscribed` | A boolean value indicating if the user is currently subscribed
`targetIsModerator` | A boolean value indicating if the user is a moderator
`targetIsVip` | A boolean value indicating if the user is a VIP
`game` | The user's current game category
`gameId` | The numeric id of the game category
`createdAt` | Datetime of when the account was created (v0.1.4+)
`accountAge` | Age of the account in seconds (v0.1.4+)