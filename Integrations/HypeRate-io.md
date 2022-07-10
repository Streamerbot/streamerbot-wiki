---
title: HypeRate.io
description: 
published: true
date: 2022-07-10T20:45:47.365Z
tags: 
editor: markdown
dateCreated: 2022-06-01T04:20:14.642Z
---

![HypeRate-logo.png](https://streamer.bot/img/integrations/hyperate.png){.align-abstopright}


# HypeRate

No longer an extension written in C#, HypeRate.io support is now a native part of **Streamer.bot**

![hyperate.io-integration.png](/hyperate.io-integration.png)

To connect to HypeRate.io, provide your ID in the `ID` field, and click on Connect.  Once HypeRate is receiving heart rate data, it will begin triggering the `Heart Rate` event

> You can also use `internal-testing` as your ID, to have fake data sent to the `Heart Rate` event.
{.is-info}

> When HypeRate.io is broadcasting your heart rate, this event can fire once every second, so be sure whatever action you use runs fast enough so it won't cause a backlog in an action queue.  It is also recommended that whatever action you are running be placed in a blocking queue.
{.is-warning}

## Available Variables

| Variable | Description |
|   ---:|-------------|
| `%heartRate%` | Heart Rate value |


<div class="btn-grid">

  [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)

</div>