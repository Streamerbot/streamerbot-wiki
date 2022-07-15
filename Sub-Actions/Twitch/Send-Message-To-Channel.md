---
title: Send Message To Channel 
description: Twitch Sub-Action Reference
published: true
date: 2022-07-11T23:09:07.203Z
tags: twitch, message, subactions, chat
editor: markdown
dateCreated: 2021-11-20T04:07:37.131Z
---

## Overview

This sub-action can send a formatted message to your Twitch chat.

![send_message_to_channel_.png](/send_message_to_channel_.png)

## Configuration

### Preferred Account

| Value | Description |
|------:|:------------|
`Bot` | Send the message from your **bot account**
`Broadcaster` | Send the message from your **broadcaster account**

### Message

Enter the message you would like to send.

This input supports all variables currently on your argument stack. 

For example, `%user%, you have %points% %pointsName%` could be sent to Twitch chat as `Steve69, you have 420 cupcakes`

> **NOTE**
> If you are having trouble sending chat messages with your **bot account**, make sure that the account is verified by completing Twitch chat [verification requirements](https://help.twitch.tv/s/article/chat-verification-settings) for your respective channel.
{.is-info}

## Variables
No variables generated.


<section class="btn-grid my-5">
    
  [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/en/Sub-Actions/Twitch)
  
  [<i class="mdi mdi-twitch text--twitch"></i>**Set Channel Game *Up Next***](/en/Sub-Actions/Twitch/Set-Channel-Game)
  
</section>