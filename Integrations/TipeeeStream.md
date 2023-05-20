---
title: TipeeeStream
description: Integrate Streamer.bot with TipeeeStream
published: true
date: 2023-01-20T17:03:31.152Z
tags: tipeeestream, donations, v0.1.8
editor: markdown
dateCreated: 2022-06-26T23:38:57.275Z
---

## Overview
Integrate with [TipeeeStream](https://www.tipeeestream.com) to receive donation events!

## Events
### Donation
Name | Description
----:|:------------
`tipeeStreamId` | The id from TipeeeStream
`timestamp` | The timestamp of this event
`username` | Who the donation was from, as the user filled out
`avatar` | Avatar of the user
`amount` | The amount of the tip (decimal value)
`fees` | The fees that will be taken from the tip
`currency` | 3 letter curency code
`message` | Any donation message the user may have included

---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/Integrations)
{.btn-grid .my-5}