---
title: Generic Variables
description: Variables Reference
published: true
date: 2022-07-15T19:13:22.082Z
tags: variables, reference
editor: markdown
dateCreated: 2022-06-30T19:57:33.363Z
---

## Overview

Generic variables are available to most event sources, so consider these the minimum you can use. Other sources will expand on these with variables specific to that event or sub-action

## Variables

### General
Useful general purpose variables{.subtitle}

| Name | Description |
|-----:|:------------|
| `date` | Current system date <br> *Accepts any standard formatting notation eg. `%date:yyyy/MM/dd%` or `%date:dddd, dd MMMM yyyy%`*{.small}
| `time` | Current system time <br> *Accepts any standard formtting notation eg. `HH-mm`*{.small}
{.vars-table}

### Event User
Variables related to the user that triggered an event{.subtitle}

| Name | Description |
|-----:|:------------|
`userId` | Unique user identifier
`userName` | User login name <br> *e.g. on Twitch this is the username in all lowercase, useful for comparison*{.small}

`user` | User display name <br> *Case sensitive for comparison*{.small}
`userType` | Specifies which streaming service the triggering user is coming from *v0.1.8+*{.version-badge} <br> `twitch` or `youtube`

`isSubscribed` | Twitch subscription status of triggering user <br> `True / False`
`isVip` | Twitch VIP status of triggering user <br> `True / False`
`isModerator` | Twitch moderator status of triggering user <br> `True / False`
{.vars-table}

### Event Source
Variables related to the triggering event source{.subtitle}

| Name | Description |
|-----:|:------------|
| `__source` | The name of the event triggering the action
| `eventSource` | String value to specify which platform generated the event *v0.1.8+*{.version-badge} <br> `twitch` or `youtube`
{.vars-table}

### Action
Variables related to the action being called{.subtitle}

| Name | Description |
|-----:|:------------|
| `actionId` | The unique ID number of the first action called *v0.1.8+*{.version-badge} 
| `runningActionId` | The instance ID number of the action in the queue *v0.1.8+*{.version-badge}
{.vars-table}

### Random User
Fetch variables for a random user currently in your chat{.subtitle}

> **WARNING**
> As of Streamer.bot *v0.1.8*{.version-badge} this functionality requires usage of the [Add Random Users](/en/Sub-Actions/Twitch/) sub-action
{.is-warning}

| Name | Description |
|-----:|:------------|
| `randomUser0` | The `username` of a random user present in chat
| `randomUserName0` | The Display name of a random user present in chat
{.vars-table}




{.vars-table}