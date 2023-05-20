---
title: Stream Online
description: Twitch Triggers Reference
published: true
date: 2023-05-10T08:33:03.728Z
tags: 
editor: markdown
dateCreated: 2023-05-10T08:33:00.953Z
---

## Overview
This triggers when the stream has started on your broadcaster account.

For a detailed guide about Twitch see [this page](/Platforms/Twitch).

## Event Data
:----|:------------:
Twitch Service: | `EventSub`
Added in: | *v0.1.17*{.version-badge}

## Variables
Name | Description
----:|:------------
`startedAt` | The date and time that the stream went online
`game` | The category name
`gameId` | The category id
`tagCount` | The number of tags
`tag#` | Each individual tag
`tags` | A `List<string>()` object for use in C#
`tagsDelimited` | A comma delimited string of the tags
{.vars-table}

> Change the `#` to a number from 0 to the end of the tags. So e.g. `%tag0%`, `%tag1%`, `%tag2%`
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Triggers Reference *Go Back***](/Triggers/Twitch)
{.btn-grid .my-5}