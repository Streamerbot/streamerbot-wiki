---
title: Get User Info for Target
description: Twitch Sub-Action Reference
published: true
date: 2022-11-03T19:32:06.202Z
tags: twitch, subactions
editor: markdown
dateCreated: 2021-08-25T21:33:30.189Z
---

## Overview
Collects various data for a Twitch user and populates a set of variables.

![overview.png](/Sub-Actions/Twitch/get-user-info-for-target/overview.png =400x)

## Configuration
### Source Type
Name | Description
----:|:------------
`User` | User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
`From Input` | This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
`Variable` | Use the content of an existing variable as the target

### Variable
If you selected `Variable` as your `Source Type`, enter the name of the variable you would like to read in.

## Variables
Name | Description
----:|:------------
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
`createdAt` | Datetime of when the account was created
`accountAge` | Age of the account in seconds
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}