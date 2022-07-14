---
title: Create Clip
description: Twitch Sub-Actions Reference
published: true
date: 2022-07-14T16:34:45.369Z
tags: twitch, subactions
editor: markdown
dateCreated: 2021-11-02T04:15:59.794Z
---

## Overview

Create a 30 second [Twitch Clip](https://help.twitch.tv/s/article/how-to-use-clips?language=en_US).

An example usage of this sub-action could be creation of a `!clipit` command so your users can quickly create clips directly from chat.

> Due to Twitch API restrictions, the generated clip will always be 30 seconds long and will be titled to match your current stream title. 
> To make your own changes to the clip duration or title, you must manually edit the clip later.
{.is-info}

![image.png](/create-clip/image.png =700x)


## Configuration
No configuration required.

## Variables
The following variables will be available after execution of this sub-action:

| Variable | Description |
| -------------:|:------|
| `createClipSuccess` | Boolean result of the request <br> `True`/`False`
| `createClipId` | String identifier of the created clip <br> `StormyAttractiveMouseThunBeast-TEfUhBnJpajsSHShD`
| `createClipCreatedAt` | Timestamp of clip creation <br> `7/11/2022 3:01:53 AM`
| `createClipUrl` | Full URL to the created clip <br>  `https://clips.twitch.tv/embed?clip=StormyAttractiveMouseThunBeast-TEfUhBnJpajsSHShD`

    
- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/en/Sub-Actions/Twitch)
- [<i class="mdi mdi-twitch text--twitch"></i>**Create Stream Marker *Up Next***](/en/Sub-Actions/Twitch/Create-Stream-Marker)
{.btn-grid .mt-10}