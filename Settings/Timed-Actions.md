---
title: Timed Actions
description: 
published: true
date: 2022-07-09T19:59:24.019Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:26.506Z
---

Actions to be performed either repeatedly or for a duration can be defined here. 

When a timer becomes enabled its action will execute on the next occurence. 

Unless manually overridden by another [action](/Actions), the `Timed action` will only execute again if both the `Interval` and `Lines` criteria have been met


![timed action](/122174618-c4eb0280-ce7a-11eb-9ee4-89ed58957788.png)


`Enabled` states this timer is currently running

`Repeat` defines if the `Timed Action` should automatically run again once the limiting criteria are met

`Interval` Time in minutes that must elapse before the action will run again. 

If `Random` is checked this becomes a lower and upper bound in seconds 

`Lines` Any non-zero value will pause the action from running again until that many lines have been entered in chat

`Action` Choose the [action](Actions) to execute when the timer state becomes `Enabled` 

