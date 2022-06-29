---
title: Get User Info for Target
description: 
published: true
date: 2021-08-28T01:56:27.430Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:33:30.189Z
---

![User Info](/122114131-d8ff1780-ce1a-11eb-85c5-bdea50941d8c.png)

This sub-action collates various data from a speciified Twitch! user and passes it to a number of [variables](/Variables) that other [Sub-Actions](/Sub-Actions) can use.

The target of the data fetch can be `User` `From Input` or `Variable`

### User

The actual user that invoked the action e.g. a raid leader, subscriber, point redeemer etc.

### From input

This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel

### Variable

This will use the content of an existing [variable](Variables) as the target. This can be defined in a previous [sub-action](Sub-Actions) or could be an inherent function e.g. `randomUserName0`