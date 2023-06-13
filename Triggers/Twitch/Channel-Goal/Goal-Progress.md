---
title: Goal Progress
description: Twitch Triggers Reference
published: true
date: 2023-06-13T10:56:58.732Z
tags: 
editor: markdown
dateCreated: 2023-06-13T10:56:58.732Z
---

## Overview
When a channel goal progresses.

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
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}