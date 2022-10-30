---
title: Present Viewers Event
description: Twitch Events Reference
published: true
date: 2022-10-30T13:05:32.508Z
tags: 
editor: markdown
dateCreated: 2022-08-23T21:35:31.605Z
---

## Overview
The present viewer tick will always happen, but you have the ability to have it "live update" from twitch, or artificially mark someone as present.

Under the Present Viewer action selector, there are 2 setttings, a `Live Update` check box, and a slider bar.

When Live Update is checked, the slider next to it is how often this update will occur, between 1 and 10 minutes, this will also still execute the action at this interval.

When Live Update is not checked, the slider next to it behaves as a threshold. The timer runs every minute, and checks the current time minus the user's last active time, if this is less then the threshold, they are marked as present, otherwise they are marked as not present.  The action will still be executed, but, it will occur every minute.

The default setting is `Live Update` not checked, and the slider set to `5` minutes.  To have the same functionality as *v0.1.12*{.version-badge} and earlier, enable `Live Update` and make sure the slider is set to `5` minutes.

## Variables
Name | Description
----:|:------------
`isLive` |Boolean for current streaming status <br> `True`/`False` 
`isTest` |Boolean for if this is demo data or not <br> `True`/`False` 
`users` | A Dictionary list of usernames present in IRC chat <br> Each user present will get the following data
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/en/Platforms/Twitch/Events)
{.btn-grid .my-5}