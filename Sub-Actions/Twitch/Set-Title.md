---
title: Set Channel Title 
description: Twitch Sub-Actions Reference
published: true
date: 2022-07-11T23:25:51.212Z
tags: twitch, subactions
editor: markdown
dateCreated: 2022-01-26T06:09:10.831Z
---

## Overview

This sub-action can modify the title of your Twitch stream.

![settitle-1.png](/settitle-1.png)

## Configuration

In the title box on this window you will need to use the variable `%rawInput%` to use the data that is contained in this variable to set as a title. Now click ok and you're done for this part. Note: The data in this variable is pulled from the user executing the command in your twitch chat.  (Optional) you can send a message to your twitch chat to notify the user that triggered the command. that the title has been successfully updated. To add this in your sub action window navigate through the right click menu to the `Twitch` group now select `Send Message To Channel` a new window will appear where you can enter a message to send to your twitch channel you can use the example in the image below if you choose too.

![message_out_put_.png](/message_out_put_.png)

Last part is you need to make a command for the moderators only to use to execute this action for you. How to do this can be found on the [Commands](/en/Commands) section of the wiki. 

> **WARNING**
> Moderator privileges are required on your bot account for this sub-action to work!
{.is-warning}

<section class="btn-grid my-5">
    
  [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/en/Sub-Actions/Twitch)
  
  [<i class="mdi mdi-twitch text--twitch"></i>**Send Message To Channel *Up Next***](/en/Sub-Actions/Twitch/Send-Message-To-Channel)
  
</section>