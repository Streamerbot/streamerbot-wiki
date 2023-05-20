---
title: IFTTT Notification (Advanced)
description: IFTTT Sub-Action Reference
published: true
date: 2023-03-16T11:55:40.975Z
tags: 
editor: markdown
dateCreated: 2023-01-10T18:10:28.578Z
---

## Overview
Send a notification trigger to IFTTT from Streamer.bot with additional arguments.

![overview.png](/Sub-Actions/IFTTT/notification-advanced/overview.png =400x)

## Setup Guide
1. Create a new applet in your IFTTT app
2. For `If This,` select the `Streamer.bot` service
3. Select the `IFTTT Advanced Notification Sub-Action` as your trigger
4. If you have not already, you will be asked to authenticate with your Streamer.bot account
5. Enter a matching event name in both your IFTTT applet and your Streamer.bot sub-action to trigger on specific events

## Configuration
### Event Name
The event name will be sent to IFTTT as a part of the trigger and can be used to filter requests.

### Arguments
You can configure any number of arguments to be sent with the trigger to IFTTT.

The first **five** arguments will be parsed into IFTTT ingredients available in your applet in the following format:
`Argument1Name`
`Argument1Value`

Additionally, all arguments will be made available as JSON in the `ArgumentsJson` ingredient.

---

- [<i class="mdi mdi-chevron-left"></i> **IFTTT Sub-Actions *Go Back***](/Sub-Actions/IFTTT)
- [<i class="mdi mdi-android-messages"></i> **IFTTT Notification (Basic) *Up Next***](/Sub-Actions/IFTTT/Notification)
{.btn-grid .my-5}