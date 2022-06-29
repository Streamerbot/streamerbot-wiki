---
title: Set Channel Title 
description: Change the stream title 
published: true
date: 2022-01-26T23:52:32.223Z
tags: twitch, title
editor: markdown
dateCreated: 2022-01-26T06:09:10.831Z
---

# Set Channel Title 

This Sub-Action within the bot can be used to set the title that is displayed on your Twitch channel. 

To do this you will need to create an action for this to be attached to a command to be triggered. But first you need to build out the action with the required sub actions - in the sub actions sections you will first need to grab the raw input from the moderator command. This Raw Input is used to create and set the title on your twitch channel. To do this in the sub actions window you need to right click for the menu of actions to appear. Navigate to the following  `Add action` then go down to `Twitch` now in this menu you will need to click the `Get User Info For Target` in this menu. A window will now appear like the one below. 

![get_target_info.png](/get_target_info.png)


In this window on the source type drop down you need to select the `From Input` now click `OK`. Next, we need to go back in the sub action right click menu and navigate back to the `Twitch` sub menu except this time click the `Set Channel Title` option a window like this will appear.

![settitle-1.png](/settitle-1.png)

In the title box on this window you will need to use the variable `%rawInput%` to use the data that is contained in this variable to set as a title. Now click ok and you're done for this part. Note: The data in this variable is pulled from the user executing the command in your twitch chat.  (Optional) you can send a message to your twitch chat to notify the user that triggered the command. that the title has been successfully updated. To add this in your sub action window navigate through the right click menu to the `Twitch` group now select `Send Message To Channel` a new window will appear where you can enter a message to send to your twitch channel you can use the example in the image below if you choose too.

![message_out_put_.png](/message_out_put_.png)

Last part is you need to make a command for the moderators only to use to execute this action for you. How to do this can be found on the [Commands](/en/Commands) section of the wiki. 

*Note: The bot account must be a moderator in your Twitch channel for this to work!*


