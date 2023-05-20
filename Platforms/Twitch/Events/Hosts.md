---
title: Hosts
description: Twitch Events Reference
published: false
date: 2023-03-16T13:02:39.249Z
tags: twitch, events
editor: markdown
dateCreated: 2022-01-03T14:45:31.132Z
---

## Overview
Streamer.bot monitor for both a user starting a host of your channel. The actions for this can be configured on the `Host` tab

### Generic
The `Generic` action is run on any incoming host that does not match a defined range

## Viewer Ranges
If you would like a special alert to override the generic action for incoming hosts of specific sizes you can define the ranges and the Action to assign to them here.
> 
> You can add as many ranges as you like but there is no way to define an unlimited upper bound, so if you are using ranges make sure your largest one has a Max value that will be big enough for your needs, otherwise Streamer.bot will default back to the Generic action
{.is-info}


## Variables
> Mileage may vary, Twitch API documentation does not match real life results
{.is-warning}

Name | Description
----:|:------------
`user` | The user who is hosting the channel
`viewers` | Provides an estimate of live viewers watching a hosted stream
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}