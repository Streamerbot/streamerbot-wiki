---
title: Bot Whispers
description: Twitch Triggers Reference
published: true
date: 2023-06-10T18:19:13.111Z
tags: 
editor: markdown
dateCreated: 2023-06-10T18:18:58.718Z
---

## Overview
When someone sends the bot account a whisper.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Notes
The user sending the whisper must have a **verified phone number** (see the **Phone Number setting** in your **Security and Privacy settings**).

The API may silently drop whispers that it suspects of violating Twitch policies, it will still indicate success even if the message is dropped.

Rate Limits: You may whisper to a maximum of **40 unique recipients per day**. Within the per day limit, you may whisper a maximum of 3 whispers per second and a maximum of 100 whispers per minute.

The maximum message lengths are:
* 500 characters if the user you're sending the message to hasn't whispered you before.
* 10,000 characters if the user you're sending the message to has whispered you before.

Messages that exceed the maximum length are truncated.

## Event Data
:----|:------------:
Twitch Service: | `Chat Client`
Added in: | *v0.1.14*{.version-badge}

## Variables
This includes the [User](/Variables/User-Variables) variables and the [Chat](/Variables/Chat-Variables) variables.

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}