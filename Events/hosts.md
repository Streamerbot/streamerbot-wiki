---
title: Hosts
description: Alerts for a user hosting the stream
published: true
date: 2022-06-30T20:42:37.602Z
tags: 
editor: markdown
dateCreated: 2022-01-03T14:45:31.132Z
---

# Hosts

Streamer.bot monitor for both a user starting a host of your channel. The actions for this can be configured on the `Host` tab

![image.png](/image.png)

### Generic

The `Generic` action is run on any incoming host that does not match a defined range

## Viewer Ranges

If you would like a special alert to override the generic action for incoming hosts of specific sizes you can define the ranges and the Action to assign to them here.
> 
> You can add as many ranges as you like but there is no way to define an unlimited upper bound, so if you are using ranges make sure your largest one has a Max value that will be big enough for your needs, otherwise Streamer.bot will default back to the Generic action
{.is-info}


# Variables

> Mileage may vary, Twitch API documentation does not match real life results
{.is-warning}

Variable | Description
---------:|------------
`user` | The user who is hosting the channel
`viewers` | Provides an estimate of live viewers watching a hosted stream


