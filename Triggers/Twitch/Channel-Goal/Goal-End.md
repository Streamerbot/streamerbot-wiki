---
title: Goal End
description: Twitch Triggers Reference
published: true
date: 2023-06-13T10:55:25.036Z
tags: 
editor: markdown
dateCreated: 2023-06-13T10:55:25.036Z
---

## Overview
When a channel goal ends.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `EventSub`
Added in: | *v0.1.15*{.version-badge}

## Variables
Name | Description
----:|:------------
`goal.id` | The UUID of this channel goal
`goal.type` | The type of this channel goal
`goal.description` | The description of this channel goal
`goal.currentAmount` | The current amount of this channel goal
`goal.targetAmount` | The target of this channel goal
`goal.startedAt` | The timestamp that this channel goal started
`goal.endedAt` | The timestamp that this channel goal ended
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}