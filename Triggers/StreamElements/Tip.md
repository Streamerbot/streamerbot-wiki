---
title: Tip
description: StreamElements Triggers Reference
published: true
date: 2023-03-16T11:14:04.935Z
tags: 
editor: markdown
dateCreated: 2023-03-15T20:22:17.119Z
---

## Overview
This triggers when you get a tip via StreamElements.

For a detailed guide about StreamElements see [this page](/Integrations/StreamElements).

## Configuration
### Ranges
You can select ranges if you want to filter between two values.

## Variables
Name | Description
----:|:------------
`tipUsername` | Username of the user as provided by StreamElements (may not be from Twitch)
`tipAvatar` | The URL of the user's avatar
`tipAmount` | The amount of the tip
`tipCurrency` | The 3 letter payment currency code
`tipMessage` | The tip message that the user may has included
`isTest` | Boolean value indicating if the tip was a test `True`/`False`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**StreamElements Triggers Reference *Go Back***](/Triggers/StreamElements)
- [<i class="mdi mdi-account primary--text"></i> **Merch *Next Up***](/Triggers/StreamElements/Merch)
{.btn-grid .my-5}