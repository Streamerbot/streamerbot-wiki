---
title: Sub Counter
description: 
published: true
date: 2021-11-14T21:08:22.551Z
tags: 
editor: markdown
dateCreated: 2021-11-14T21:08:19.940Z
---

# Sub Counter
![sub-counter2.png](/sub-counter2.png)

The Sub-counter will increment a persisted variable every time a sub is recieved and save the result to a specified file.

When `subCounter` equals the `rollover` target a celebration action can be triggered
Reaching `rollover` goal will reset the counter and increment the `rolloverCount` variable

> Setting the `rollover` goal to 0 will disable the rollover function and just count subs indefinately
{.is-info}