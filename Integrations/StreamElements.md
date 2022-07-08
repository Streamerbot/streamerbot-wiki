---
title: StreamElements
description: Streamer.bot integration with StreamElements
published: true
date: 2022-07-08T18:50:43.205Z
tags: integrations, streamelements
editor: markdown
dateCreated: 2022-05-13T04:07:00.154Z
---

# Overview

The StreamElements integration allows you to connect Streamer.bot with your StreamElements account to receive tip and merch events.

![integrations-streamelements-events-018.png](/integrations-streamelements-events-018.png =800x)

# Settings

You can find the configuration for this integration at `Integrations -> StreamElements -> Settings`

## Authentication
**The StreamElements integration now uses OAuth for authorizing against your account**

To connect Streamer.bot with your StreamElements account: 
1. Navigate to the settings tab within the StreamElements integration
2. Click `Connect` and authorize **Streamer.bot** to connect to your account

# Events
The following StreamElements events are monitored by Streamer.bot and will allow you to execute actions with their content:

## Tips
**Streamer.bot** can monitor your StreamElements account for tips (donations) and perform different actions based on the value.

`Tips` have access to a number of text [variables](/Variables) that can be passed to your [sub-actions](/Sub-Actions)

![SE Tip](/130134906-db4e10d9-5fd9-4b17-a99f-2e860a526825.png)

## Merch
*v0.1.8*{.version-badge}

With version 0.1.8, the ability to attach an action to a Merch Event was introduced, information for this event will be filled out soon.
