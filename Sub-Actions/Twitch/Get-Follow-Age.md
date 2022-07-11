---
title: Get Follow Age Info for Target
description: Twitch Sub-Actions Reference
published: true
date: 2022-07-11T22:55:59.055Z
tags: twitch, subactions, follow age
editor: markdown
dateCreated: 2022-02-20T04:01:00.028Z
---

## Overview

This sub-action collects various data for a specified Twitch user and populates a set of [variables](#variables) that other [Sub-Actions](/Sub-Actions) can use.

![follow_age_info_from_user.png](/follow_age_info_from_user.png)

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

> **NOTE** 
> These variables cannot be tested from the Broadcaster account, since you cannot follow yourself.
> You may test them from the bot account or any other Twitch account.
{.is-info}

The following variables will be available after execution of this sub-action:

| Variable | Description |
|---------:|:------------|
`followDate`| The date the user followed
`followAgeLong` | How long the user has been following in a long format, 1 year, 10 months, 5 days, etc
`followAgeShort` | How long the user has been following in a short format, 1y, 10m, 5d, 22h, 3m, 25s
`followAgeDays` | The total number of days the user has been following
`followAgeMinutes` | The total number of minutes the user has been following
`followAgeSeconds` | The total number of seconds the user has been following
`followUser` | The users display name
`followUserName` | The user's login name
`followUserId` | The user's twitch id


<section class="btn-grid my-5">
    
  [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/en/Sub-Actions/Twitch)
  
  [<i class="mdi mdi-twitch text--twitch"></i>**Get User Info for Target *Up Next***](/en/Sub-Actions/Twitch/Get-User-Info-for-Target)
  
</section>