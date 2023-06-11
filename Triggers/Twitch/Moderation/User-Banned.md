---
title: User Banned
description: Twitch Triggers Reference
published: true
date: 2023-06-11T11:43:27.953Z
tags: 
editor: markdown
dateCreated: 2023-06-11T11:41:10.260Z
---

## Overview
When a user gets banned in chat.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `PubSub`
Added in: | *N/A*{.version-badge}

## Variables
Name | Description
----:|:------------
`user` | The user who was banned <br> <small>*This will only be populated if the user has been present in chat*</small>
`createdAt` | The timestamp when the ban was created
`createdById` | The Twitch user id from who created the ban 
`createdByUsername` | The user name from who created the ban
`createdByDisplayName` | The display name from who created the ban
`reason` | The reason for the ban
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}