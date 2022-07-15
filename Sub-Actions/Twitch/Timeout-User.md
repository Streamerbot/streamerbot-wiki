---
title: Timeout User
description: Twitch Sub-Actions Reference
published: true
date: 2022-07-11T23:43:45.026Z
tags: twitch, subactions, timeout
editor: markdown
dateCreated: 2021-08-25T21:34:21.886Z
---

## Overview

Timeout a specified chat user for a period of time.

![Timeout](/122118974-96403e00-ce20-11eb-8524-df840ff35a73.png)

## Configuration

### Type

| Value | Description |
|------:|:------------|
`Redeemer` | Timeout the user who redeemed a connected channel point reward
`Random` | Automatically select a random user from your chat
`Specific User` | Select a user from the known user list
`From Input` | Use a value contained in the `%rawInput%` variable <br>For example, with a `!timeout` command used by your moderators

### Duration
Time in seconds to enact the timeout

### Exclude Moderators
If checked, channel moderators will be immune to this [sub-action](Sub-Actions)

### Reason
Enter any text to give as the reason for this timeout.

## Variables
No variables generated.


<section class="btn-grid my-5">
    
  [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/en/Sub-Actions/Twitch)
  
  [<i class="mdi mdi-twitch text--twitch"></i>**Run Commercial *Up Next***](/en/Sub-Actions/Twitch/Run-Commercial)
  
</section>