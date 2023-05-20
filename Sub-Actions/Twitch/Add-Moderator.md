---
title: Add Moderator
description: Twitch Sub-Action Reference
published: true
date: 2023-02-25T06:30:48.225Z
tags: 
editor: markdown
dateCreated: 2023-02-04T10:05:38.924Z
---

## Overview
Add a moderator to your Twitch channel.

![overview.png](/Sub-Actions/Twitch/add-moderator/overview.png =400x)

## Configuration
### Source Type
Name | Description
----:|:------------
`User` | User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
`From Input` | This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
`Variable` | Use the content of an existing variable as the target
{.vars-table}

### Variable
If you selected `Variable` as your `Source Type`, enter the name of the variable you would like to read in.

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}