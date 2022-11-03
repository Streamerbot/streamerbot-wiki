---
title: Create Clip
description: Twitch Sub-Actions Reference
published: true
date: 2022-11-03T19:21:40.739Z
tags: twitch, subactions
editor: markdown
dateCreated: 2021-11-02T04:15:59.794Z
---

## Overview
Creates a 30 second Twitch Clip.

> Due to Twitch API restrictions, the generated clip will always be 30 seconds long and will be titled to match your current stream title. 
> To make your own changes to the clip duration or title, you must manually edit the clip later.
{.is-info}

![overview.png](/Sub-Actions/Twitch/create-clip/overview.png =400x)

## Variables
Name | Description
----:|:------------
`createClipSuccess` | Boolean result of the request <br> `True/False`
`createClipId` | String identifier of the created clip
`createClipCreatedAt` | Timestamp of clip creation <br> `7/11/2022 3:01:53 AM`
`createClipUrl` | Full URL to the created clip
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}