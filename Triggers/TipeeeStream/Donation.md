---
title: Donation
description: TipeeeStream Triggers Reference
published: true
date: 2023-03-15T21:36:47.478Z
tags: 
editor: markdown
dateCreated: 2023-03-15T21:36:45.632Z
---

## Overview
This triggers when you get a donation via TipeeeStream.

For a detailed guide about TipeeeStream see [this page](/Integrations/TipeeeStream).

## Configuration
### Ranges
You can select ranges if you want to filter between two values.

## Variables
Name | Description
----:|:------------
`tipeeStreamId` | The id from TipeeeStream
`timestamp` | The timestamp of this event
`username` | Who the donation was from, as the user filled out
`avatar` | Avatar of the user
`amount` | The amount of the tip (decimal value)
`fees` | The fees that will be taken from the tip
`currency` | The 3 letter curency code
`message` | Any donation message the user may have included
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**TipeeeStream Triggers Reference *Go Back***](/Triggers/TipeeeStream)
{.btn-grid .my-5}