---
title: User Timed Out
description: Twitch Triggers Reference
published: true
date: 2023-06-11T11:43:39.115Z
tags: 
editor: markdown
dateCreated: 2023-06-11T11:43:28.955Z
---

## Overview
When a user gets timed out in chat.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `PubSub`
Added in: | *N/A*{.version-badge}

## Variables
Name | Description
----:|:------------
`user` | The user who was timed out
`createdAt` | The timestamp when the timeout was created
`createdById` | The Twitch user id from who created the timeout 
`createdByUsername` | The user name from who created the timeout
`createdByDisplayName` | The display name from who created the timeout
`reason` | The reason for the timeout
`duration` | The duration of this timeout in seconds
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}