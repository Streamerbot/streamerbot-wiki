---
title: Shoutout Created
description: Twitch Triggers Reference
published: true
date: 2023-05-28T13:25:11.169Z
tags: 
editor: markdown
dateCreated: 2023-05-28T13:25:11.169Z
---

## Overview
This triggers when a shoutout gets created in your chat.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `Chat Client`
Added in: | *v0.1.14*{.version-badge}

## Variables
This includes the [User](/Variables/User-Variables) variables and the [Target](/Sub-Actions/Twitch/Get-User-Info-for-Target#variables) variables.

User: Who created the shoutout
Target: Who reveived the shoutout

Name | Description
----:|:------------
`shoutoutId` | Twitch's internal ID for the shoutout
`targetUserId` | The user's id
`targetUserLogin` | The user's login name
`targetUserDisplayName` | The user's display name
`targetUserPrimaryColorHex` | The user's primary color in hex
`targetUserProfileImageURL` | The user's profile image
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}