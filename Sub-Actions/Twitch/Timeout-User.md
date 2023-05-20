---
title: Timeout User
description: Twitch Sub-Actions Reference
published: true
date: 2022-11-03T19:33:25.816Z
tags: twitch, subactions, timeout
editor: markdown
dateCreated: 2021-08-25T21:34:21.886Z
---

## Overview
Timeout a specified chat user for a period of time.

![overview.png](/Sub-Actions/Twitch/timeout-user/overview.png =400x)

## Configuration
### Type
Name | Description
----:|:------------
`Redeemer` | Timeout the user who redeemed a connected channel point reward
`Random` | Automatically select a random user from your chat
`Specific User` | Select a user from the known user list
`From Input` | Use a value contained in the `%rawInput%` variable

### Duration
Time in seconds to enact the timeout

### Exclude Moderators
If checked, channel moderators will be immune to this [sub-action](Sub-Actions)

### Reason
Enter any text to give as the reason for this timeout.

## Variables
Name | Description
----:|:------------
`createdAt` | The time the timeout was created.
`createdById` | User id of the timeout creator.
`createdByUsername` | User's login name of the timeout creator.
`createdByDisplayName` | Display name of the timeout creator.
`duration` | The duration of the timeout.
`reason` | The reason of the timeout
{.vars-table}

> This includes default variables e.g. %user% and [broadcaster variables](/Sub-Actions/Twitch/Add-Broadcaster-Information)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}