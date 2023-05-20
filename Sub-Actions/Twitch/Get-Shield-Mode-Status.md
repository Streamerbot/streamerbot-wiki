---
title: Get Shield Mode Status
description: Twitch Sub-Actions Reference
published: true
date: 2023-03-16T13:37:22.327Z
tags: 
editor: markdown
dateCreated: 2022-12-05T09:35:30.752Z
---

## Overview
Fetches your shield mode status and adds the information as variables.

![overview.png](/Sub-Actions/Twitch/get-shield-mode-status/overview.png =400x)

## Variables
Name | Description
----:|:------------
`is_active` | If shield mode is active or not <br> `True`/`False`
`lastActivatedAt`| When this was last activated e.g. 12/31/2000 0:00:00 AM
`moderatorId` | The moderator's id
`moderatorName` | The moderator's display name
`moderatorLogin` | The moderator's login name
{.vars-table}

> This will include [Broadcaster Variables](/Sub-Actions/Twitch/Add-Broadcaster-Information)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}